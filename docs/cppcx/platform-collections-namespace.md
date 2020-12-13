---
description: 'Дополнительные сведения о пространстве имен Platform:: Collections.'
title: Пространство имен Platform::Collections
ms.date: 01/18/2018
ms.topic: reference
f1_keywords:
- collection/Platform::Collections
helpviewer_keywords:
- Platform::Collections Namespace
ms.assetid: b5042864-5f22-40b7-b7a5-c0691f65cc47
ms.openlocfilehash: d80479ed73183450dedd86119dda2da1fab800e0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340415"
---
# <a name="platformcollections-namespace"></a>Пространство имен Platform::Collections

Пространство имен Platform:: Collections содержит `Map` `MapView` классы,, `Vector` и `VectorView` . Эти классы являются конкретными реализациями соответствующих интерфейсов, которые определены в пространстве имен [Windows::Foundation::Collections](/uwp/api/windows.foundation.collections) . Конкретные типы коллекций не могут переноситься через интерфейс ABI (например, когда программа JavaScript или C# вызывает компонент C++), но они могут неявно преобразоваться в соответствующие типы интерфейсов. Например, если вы реализуете открытый метод, который заполняет и возвращает коллекцию, используйте [Platform::Collections::Vector](../cppcx/platform-collections-vector-class.md) для внутренней реализации коллекции и [Windows::Foundation::Collections::IVector](/uwp/api/windows.foundation.collections.ivector-1) в качестве возвращаемого типа. Дополнительные сведения см. в разделе [коллекции](../cppcx/collections-c-cx.md) и [Создание среда выполнения Windows компонентов в C++](/windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp).

Можно создать Platform::Collections::Vector из [std::vector](../standard-library/vector-class.md) и [Platform::Collections::Map](../cppcx/platform-collections-map-class.md) из [std::map](../standard-library/map-class.md).

Кроме того, пространство имен Platform:: Collections обеспечивает поддержку обратных итераторов вставки и ввода, а `Vector` также `VectorView` итераторов и.

`#include`Для использования типов в пространстве имен Platform:: Collections необходимо включить () заголовок Collection. h.

## <a name="syntax"></a>Синтаксис

```cpp
#include <collection.h>
using namespace Platform::Collections;
```

### <a name="members"></a>Члены

Это пространство имен содержит следующие члены.

|Имя|Описание|
|----------|-----------------|
|[Класс Platform:: Collections:: BackInsertIterator](../cppcx/platform-collections-backinsertiterator-class.md)|Представляет итератор, который вставляет элемент в конец коллекции.|
|[Класс Platform:: Collections:: InputIterator](../cppcx/platform-collections-inputiterator-class.md)|Представляет итератор, который вставляет элемент в начало коллекции.|
|[Класс Platform:: Collections:: Map](../cppcx/platform-collections-map-class.md)|Представляет изменяемую коллекцию пар "ключ-значение", доступ к которым можно получить по ключу. Аналогично [std::map](../standard-library/map-class.md).|
|[Класс Platform:: Collections:: MapView](../cppcx/platform-collections-mapview-class.md)|Представляет доступную только для чтения коллекцию пар "ключ-значение", доступ к которым можно получить по ключу.|
|[Класс Platform:: Collections:: Vector](../cppcx/platform-collections-vector-class.md)|Представляет изменяемую последовательность элементов. Аналогично [std::vector](../standard-library/vector-class.md).|
|[Класс Platform:: Collections:: VectorIterator](../cppcx/platform-collections-vectoriterator-class.md)|Представляет итератор, который обходит коллекцию `Vector` .|
|[Класс Platform:: Collections:: VectorView](../cppcx/platform-collections-vectorview-class.md)|Представляет доступную только для чтения последовательность элементов.|
|[Класс Platform:: Collections:: VectorViewIterator](../cppcx/platform-collections-vectorviewiterator-class.md)|Представляет итератор, который обходит коллекцию `VectorView` .|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[Пространство имен Platform](../cppcx/platform-namespace-c-cx.md)

### <a name="requirements"></a>Требования

**Метаданные:** Platform. winmd

**Пространство имен:** Platform::Collections

**Параметр компилятора:** /ZW

## <a name="see-also"></a>См. также раздел

[Пространство имен платформы](../cppcx/platform-namespace-c-cx.md)
