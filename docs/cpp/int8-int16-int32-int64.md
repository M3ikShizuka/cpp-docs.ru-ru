---
description: 'Дополнительные сведения: __int8, __int16, __int32, __int64'
title: __int8, __int16, __int32, __int64
ms.date: 10/09/2018
f1_keywords:
- __int8_cpp
- __int16_cpp
- __int32_cpp
- __int64_cpp
- __int8
- __int16
- __int32
- __int64
- _int8
- _int16
- _int32
- _int64
helpviewer_keywords:
- __int16 keyword [C++]
- integer data type [C++], integer types in C++
- __int32 keyword [C++]
- integer types [C++]
- __int8 keyword [C++]
- __int64 keyword [C++]
ms.assetid: 8e384602-2578-4980-8cc8-da63842356b2
ms.openlocfilehash: 8dddb8dc63b8aa9898b78ee02ea2dc904b362442
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332519"
---
# <a name="__int8-__int16-__int32-__int64"></a>__int8, __int16, __int32, __int64

**Только для систем Майкрософт**

В Microsoft C/C++ поддерживаются целочисленные типы с указанием размера. Можно объявить 8-, 16-, 32-или 64-разрядные целочисленные переменные с помощью **`__intN`** спецификатора типа, где * *_`N`_* _ имеет значение 8, 16, 32 или 64.

В следующем примере объявляется по одной переменной каждого из этих целочисленных типов с указанием размера:

```cpp
__int8 nSmall;      // Declares 8-bit integer
__int16 nMedium;    // Declares 16-bit integer
__int32 nLarge;     // Declares 32-bit integer
__int64 nHuge;      // Declares 64-bit integer
```

Типы _ * `__int8` * *, **`__int16`** и **`__int32`** являются синонимами для типов ANSI, имеющих одинаковый размер, и полезны для написания переносимого кода, который ведет себя одинаково на нескольких платформах. **`__int8`** Тип данных является синонимом типа **`char`** , **`__int16`** является синонимом типа **`short`** и **`__int32`** является синонимом типа **`int`** . **`__int64`** Тип является синонимом типа **`long long`** .

Для совместимости с предыдущими версиями,,, **`_int8`** **`_int16`** **`_int32`** и **`_int64`** являются синонимами для **`__int8`** , **`__int16`** , **`__int32`** и, **`__int64`** если не указан параметр компилятора, не [ `/Za` \( отключающий расширения языка)](../build/reference/za-ze-disable-language-extensions.md) .

## <a name="example"></a>Пример

В следующем примере показано, что `__intN` параметр будет выдвинут на **`int`** :

```cpp
// sized_int_types.cpp

#include <stdio.h>

void func(int i) {
    printf_s("%s\n", __FUNCTION__);
}

int main()
{
    __int8 i8 = 100;
    func(i8);   // no void func(__int8 i8) function
                // __int8 will be promoted to int
}
```

```Output
func
```

## <a name="see-also"></a>См. также раздел

[Ключевые слова](../cpp/keywords-cpp.md)<br/>
[Встроенные типы](../cpp/fundamental-types-cpp.md)<br/>
[Диапазоны типов данных](../cpp/data-type-ranges.md)<br/>
