---
description: 'Дополнительные сведения о: использование C++ AMP в приложениях UWP'
title: Использование C++ AMP в приложениях UWP
ms.date: 11/04/2016
ms.assetid: 85577298-2c28-4209-9470-eb21048615db
ms.openlocfilehash: 91c7b147ff89a1fe19ebe1b18e465533053542d0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97314481"
---
# <a name="using-c-amp-in-uwp-apps"></a>Использование C++ AMP в приложениях UWP

В приложении универсальная платформа Windows (UWP) можно использовать C++ AMP (C++ Accelerated Massive Parallelism) для выполнения вычислений на GPU (графический процессор) или других вычислительных ускорителях. Однако C++ AMP не предоставляет интерфейсы API для работы непосредственно с типами среды выполнения Windows, а в среде выполнения Windows нет программы-оболочки для C++ AMP. При использовании в коде типов среды выполнения Windows, включая созданные самостоятельно, необходимо преобразовать их в совместимые с С++ AMP типы.

## <a name="performance-considerations"></a>Вопросы производительности

Если вы Visual C++ используете расширения компонентов C++/CX для создания приложения универсальная платформа Windows (UWP), для данных, которые будут использоваться с C++ AMP, рекомендуется использовать типы данных с обычным старыми данными (POD) вместе с непрерывным хранилищем (например, `std::vector` или массивы в стиле C). Это может помочь добиться более высокой производительности, чем при использовании типов, отличных от POD, или контейнеров Windows RT, так как упаковка не выполняется.

В C++ AMPном ядре для доступа к данным, хранящимся таким образом, просто заключите `std::vector` хранилище массива или в, `concurrency::array_view` а затем используйте представление массива в `concurrency::parallel_for_each` цикле:

```cpp
// simple vector addition example
std::vector<int> data0(1024, 1);
std::vector<int> data1(1024, 2);
std::vector<int> data_out(data0.size(), 0);

concurrency::array_view<int, 1> av0(data0.size(), data0);
concurrency::array_view<int, 1> av1(data1.size(), data1);
concurrency::array_view<int, 1> av2(data_out.size(), data2);

av2.discard_data();

concurrency::parallel_for_each(av0.extent, [=](concurrency::index<1> idx) restrict(amp)
    {
        av2[idx] = av0[idx] + av1[idx];
    });
```

## <a name="marshaling-windows-runtime-types"></a>Маршалинг типов среды выполнения Windows

При работе с среда выполнения Windows API можно использовать C++ AMP данных, которые хранятся в контейнере среда выполнения Windows, например, `Platform::Array<T>^` или в сложных типах данных, таких как классы или структуры, объявленные с помощью ключевого слова **ref** или ключевого слова **value** . В таких ситуациях необходимо выполнить некоторую дополнительную работу, чтобы сделать данные доступными для C++ AMP.

### <a name="platformarrayt-where-t-is-a-pod-type"></a>Platform:: array \<T> ^, где T — тип POD

При обнаружении `Platform::Array<T>^` и T является типом Pod, доступ к его базовому хранилищу можно получить только с помощью `get` функции-члена:

```cpp
Platform::Array<float>^ arr; // Assume that this was returned by a Windows Runtime API
concurrency::array_view<float, 1> av(arr->Length, &arr->get(0));
```

Если T не является типом POD, используйте метод, описанный в следующем разделе, для использования данных с C++ AMP.

### <a name="windows-runtime-types-ref-classes-and-value-classes"></a>Типы среды выполнения Windows: классы ссылки и классы значений

C++ AMP не поддерживает сложные типы данных. Сюда входят типы, не являющиеся типами POD, и типы, объявленные с помощью ключевого слова **ref** или ключевого слова **value** . Если в контексте используется неподдерживаемый тип `restrict(amp)` , возникает ошибка времени компиляции.

При обнаружении неподдерживаемого типа можно скопировать интересные части его данных в `concurrency::array` объект. Помимо того, что данные доступны для C++ AMP, этот подход вручную может повысить производительность, увеличивая локальность данных и гарантируя, что данные, которые не будут использоваться, не копируются в ускоритель. Вы можете повысить производительность с помощью *промежуточного массива*, который представляет собой специальную форму, которая `concurrency::array` предоставляет указание для среды выполнения amp, что массив должен быть оптимизирован для частого перемещения между ним и другими массивами в заданном ускорителе.

```cpp
// pixel_color.h
ref class pixel_color sealed
{
public:
    pixel_color(Platform::String^ color_name, int red, int green, int blue)
    {
        name = color_name;
        r = red;
        g = green;
        b = blue;
    }

    property Platform::String^ name;
    property int r;
    property int g;
    property int b;
};

// Some other file

std::vector<pixel_color^> pixels (256);

for (pixel_color ^pixel : pixels)
{
    pixels.push_back(ref new pixel_color("blue", 0, 0, 255));
}

// Create the accelerators
auto cpuAccelerator = concurrency::accelerator(concurrency::accelerator::cpu_accelerator);
auto devAccelerator = concurrency::accelerator(concurrency::accelerator::default_accelerator);

// Create the staging arrays
concurrency::array<float, 1> red_vec(256, cpuAccelerator.default_view, devAccelerator.default_view);
concurrency::array<float, 1>  blue_vec(256, cpuAccelerator.default_view, devAccelerator.default_view);

// Extract data from the complex array of structs into staging arrays.
concurrency::parallel_for(0, 256, [&](int i)
    {
        red_vec[i] = pixels[i]->r;
        blue_vec[i] = pixels[i]->b;
    });

// Array views are still used to copy data to the accelerator
concurrency::array_view<float, 1> av_red(red_vec);
concurrency::array_view<float, 1> av_blue(blue_vec);

// Change all pixels from blue to red.
concurrency::parallel_for_each(av_red.extent, [=](index<1> idx) restrict(amp)
    {
        av_red[idx] = 255;
        av_blue[idx] = 0;
    });
```

## <a name="see-also"></a>См. также раздел

[Создание первого приложения UWP с помощью C++](/windows/uwp/get-started/create-a-basic-windows-10-app-in-cpp)<br/>
[Создание компонентов среды выполнения Windows в C++](/windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp)
