---
description: 'Дополнительные сведения: использование взаимодействия C++ (неявный PInvoke)'
title: Использование взаимодействия языка C++ (неявный PInvoke)
ms.date: 11/04/2016
helpviewer_keywords:
- blittable types [C++]
- platform invoke [C++], implicit
- interop [C++], features
- data marshaling [C++], C++ Interop features
- porting [C++], C++ native to .NET
- COM interfaces [C++]
- implicit platform invoke
- examples [C++], interoperability
- types [C++], blittable
- marshaling [C++], C++ Interop features
- platform invoke [C++], examples
- interoperability [C++]
- C++ Interop
- interoperability [C++], Implicit PInvoke
- C++, interop
- C++ COM Interop
- .NET [C++], porting C++ native to
ms.assetid: 5f710bf1-88ae-4c4e-8326-b3f0b7c4c68a
ms.openlocfilehash: e2b1f1aeef68fd6329ef04a53249d7dce627f2c5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97255552"
---
# <a name="using-c-interop-implicit-pinvoke"></a>Использование взаимодействия языка C++ (неявный PInvoke)

В отличие от других языков .NET, Visual C++ имеет поддержку взаимодействия, которая позволяет управляемому и неуправляемому коду существовать в одном и том же приложении и даже в одном файле (с [управляемыми неуправляемыми](../preprocessor/managed-unmanaged.md) директивами pragma). Это позволяет Visual C++ разработчикам интегрировать функциональность .NET в существующие приложения Visual C++, не нарушая остальную часть приложения.

Вы также можете вызывать неуправляемые функции из управляемого компилируемого объекта с помощью [dllexport, dllimport](../cpp/dllexport-dllimport.md).

Неявный PInvoke полезен, если не нужно указывать способ маршалирования параметров функции или какие-либо другие сведения, которые можно указать при явном вызове DllImportAttribute.

Visual C++ предоставляет два способа взаимодействия управляемых и неуправляемых функций:

- [Использование явного вызова PInvoke в C++ (атрибут DllImport)](../dotnet/using-explicit-pinvoke-in-cpp-dllimport-attribute.md)

Явный вызов PInvoke поддерживается .NET Framework и доступен в большинстве языков .NET. Но, как и предполагает его имя, взаимодействие C++ характерно для Visual C++.

## <a name="c-interop"></a>взаимодействие C++

Взаимодействие C++ обеспечивает лучшую безопасность типов, и его реализация обычно менее утомительна. Однако взаимодействие C++ не является вариантом, если неуправляемый исходный код недоступен или для межплатформенных проектов.

## <a name="c-com-interop"></a>COM-взаимодействие в C++

Функции взаимодействия, поддерживаемые Visual C++, предлагают определенные преимущества по сравнению с другими языками .NET, когда речь идет о взаимодействии с COM-компонентами. Вместо того чтобы ограничиваться ограничениями .NET Framework [Tlbimp.exe (программа импорта библиотек типов)](/dotnet/framework/tools/tlbimp-exe-type-library-importer), например Ограниченная поддержка типов данных и обязательное предоставление каждого члена каждого COM-интерфейса, взаимодействие C++ позволяет обращаться к COM-компонентам в службах и не требует отдельных сборок взаимодействия. В отличие от Visual Basic и C#, Visual C++ может использовать COM-объекты непосредственно с помощью обычных механизмов COM (таких как **CoCreateInstance** и **QueryInterface**). Это возможно из-за функций взаимодействия C++, которые приводят к тому, что компилятор автоматически вставляет код перехода из управляемой в неуправляемую функцию и обратно.

С помощью взаимодействия C++ можно использовать COM-компоненты, так как они обычно используются или могут быть заключены в классы C++. Эти классы-оболочки называются пользовательскими вызываемыми оболочками времени выполнения или Крквс. они имеют два преимущества по сравнению с использованием COM непосредственно в коде приложения:

- Полученный класс можно использовать на языках, отличных от Visual C++.

- Сведения о COM-интерфейсе могут быть скрыты из управляемого кода клиента. Типы данных .NET могут использоваться вместо собственных типов, а сведения о маршалировании данных могут быть прозрачно выполнены внутри КРКВ.

Независимо от того, используется ли COM напрямую или через КРКВ, необходимо маршалировать типы аргументов, Кроме простых, преобразуемых типов.

## <a name="blittable-types"></a>Непреобразуемые типы

Для неуправляемых интерфейсов API, использующих простые встроенные типы (см. раздел непреобразуемые [и непреобразуемые типы](/dotnet/framework/interop/blittable-and-non-blittable-types)), специальное кодирование не требуется, так как эти типы данных имеют одинаковое представление в памяти, но более сложные типы данных требуют явного маршалирования данных. Пример см. в разделе [как вызывать собственные библиотеки DLL из управляемого кода с помощью PInvoke](../dotnet/how-to-call-native-dlls-from-managed-code-using-pinvoke.md).

## <a name="example"></a>Пример

```cpp
// vcmcppv2_impl_dllimp.cpp
// compile with: /clr:pure user32.lib
using namespace System::Runtime::InteropServices;

// Implicit DLLImport specifying calling convention
extern "C" int __stdcall MessageBeep(int);

// explicit DLLImport needed here to use P/Invoke marshalling because
// System::String ^ is not the type of the first parameter to printf
[DllImport("msvcrt.dll", EntryPoint = "printf", CallingConvention = CallingConvention::Cdecl,  CharSet = CharSet::Ansi)]
// or just
// [DllImport("msvcrt.dll")]
int printf(System::String ^, ...);

int main() {
   // (string literals are System::String by default)
   printf("Begin beep\n");
   MessageBeep(100000);
   printf("Done\n");
}
```

```Output
Begin beep
Done
```

## <a name="in-this-section"></a>в этом разделе

- [Инструкции. маршалинг строк ANSI с помощью взаимодействия C++](../dotnet/how-to-marshal-ansi-strings-using-cpp-interop.md)

- [Инструкции. маршалинг строк Юникода с помощью взаимодействия C++](../dotnet/how-to-marshal-unicode-strings-using-cpp-interop.md)

- [Инструкции. маршалинг строк COM с помощью взаимодействия C++](../dotnet/how-to-marshal-com-strings-using-cpp-interop.md)

- [Инструкции. маршалинг структур с помощью взаимодействия C++](../dotnet/how-to-marshal-structures-using-cpp-interop.md)

- [Инструкции. маршалинг массивов с помощью взаимодействия C++](../dotnet/how-to-marshal-arrays-using-cpp-interop.md)

- [Инструкции. маршалирование обратных вызовов и делегатов с помощью взаимодействия C++](../dotnet/how-to-marshal-callbacks-and-delegates-by-using-cpp-interop.md)

- [Инструкции. Маршалинг внедренных указателей с использованием взаимодействия C++](../dotnet/how-to-marshal-embedded-pointers-using-cpp-interop.md)

- [Как получить доступ к символам в системе:: String](../dotnet/how-to-access-characters-in-a-system-string.md)

- [Как преобразовать строку char * в массив System:: Byte](../dotnet/how-to-convert-char-star-string-to-system-byte-array.md)

- [Как преобразовать строку System:: String в wchar_t * или char\*](../dotnet/how-to-convert-system-string-to-wchar-t-star-or-char-star.md)

- [Как преобразовать System.: String в стандартную строку](../dotnet/how-to-convert-system-string-to-standard-string.md)

- [Как преобразовать стандартную строку в System:: String](../dotnet/how-to-convert-standard-string-to-system-string.md)

- [Как получить указатель на массив байтов](../dotnet/how-to-obtain-a-pointer-to-byte-array.md)

- [Как загрузить неуправляемые ресурсы в массив байтов](../dotnet/how-to-load-unmanaged-resources-into-a-byte-array.md)

- [Как изменить ссылочный класс в собственной функции](../dotnet/how-to-modify-reference-class-in-a-native-function.md)

- [Как определить, является ли изображение машинным или средой CLR](../dotnet/how-to-determine-if-an-image-is-native-or-clr.md)

- [Как добавить собственную библиотеку DLL в глобальный кэш сборок](../dotnet/how-to-add-native-dll-to-global-assembly-cache.md)

- [Как удержать ссылку на тип значения в собственном типе](../dotnet/how-to-hold-reference-to-value-type-in-native-type.md)

- [Как хранить ссылку на объект в неуправляемой памяти](../dotnet/how-to-hold-object-reference-in-unmanaged-memory.md)

- [Как обнаруживать компиляцию/CLR](../dotnet/how-to-detect-clr-compilation.md)

- [Практические руководства. преобразование между System:: GUID и _GUID](../dotnet/how-to-convert-between-system-guid-and-guid.md)

- [Как указать выходной параметр](../dotnet/how-to-specify-an-out-parameter.md)

- [Как использовать машинный тип в компиляции/clr](../dotnet/how-to-use-a-native-type-in-a-clr-compilation.md)

- [Инструкции. объявление дескрипторов в собственных типах](../dotnet/how-to-declare-handles-in-native-types.md)

- [Пошаговое руководство. Перенос собственного класса для использования в C #](../dotnet/how-to-wrap-native-class-for-use-by-csharp.md)

Сведения об использовании делегатов в сценарии взаимодействия см. в разделе [Delegate (расширения компонентов C++)](../extensions/delegate-cpp-component-extensions.md).

## <a name="see-also"></a>См. также раздел

- [Вызов собственных функций из управляемого кода](../dotnet/calling-native-functions-from-managed-code.md)
