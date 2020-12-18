---
title: Выравнивание (C11)
description: Описание выравнивания типов Microsoft Visual C.
ms.date: 12/10/2020
helpviewer_keywords:
- _Alignof keyword [C]
- _Alignas keyword [C]
- memory, alignment
ms.openlocfilehash: 051987ae705f84d7d4972398f742143f14b53e2b
ms.sourcegitcommit: be469dd87453255b0e35e333712c8207b09b3dd4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "97438896"
---
# <a name="alignment-c11"></a>Выравнивание (C11)

Одной из низкоуровневых особенностей C является возможность указать точное выравнивание объектов в памяти, чтобы использовать все возможности аппаратной архитектуры.

Процессоры считывают и записывают память более эффективно, если данные хранятся по адресу, который кратен размеру данных. Например, доступ к 4-байтовому целому числу осуществляется более эффективно, если он хранится по адресу, кратному 4. Если данные не выровнены, ЦП приходится выполнять больше работы для обращения к данным.

По умолчанию компилятор выравнивает данные по размеру: **`char`** по 1-байтовой границе, **`short`** по 2-байтовой границе, **`int`** , **`long`** и **`float`** по 4-байтовой границе, **`double`** по 8-байтовой границе и т. д.

Кроме того, выравнивание часто используемых данных в соответствии с размером строки кэш-памяти процессора может повысить производительность кэша. Например, при определении структуры, размер которой меньше 32 байтов, может потребоваться выполнить ее выравнивание до 32 байтов, чтобы обеспечить эффективное кэширование экземпляров этой структуры.

Как правило, вам не нужно беспокоиться о выравнивании. Компилятор обычно выравнивает данные по естественным границам с учетом характеристик целевого процессора и размера данных. Данные выравниваются по 4-байтовым границам на 32-разрядных процессорах и по 8-байтовым границам на 64-разрядных процессорах. Но в некоторых случаях можно повысить производительность или обеспечить экономное расходование памяти, настроив настраиваемое выравнивание для структур данных.

Используйте ключевое слово C11 **`_Alignof`** , чтобы получить предпочтительное выравнивание типа или переменной, и **`_Alignas`** , чтобы указать пользовательское выравнивание для переменной или определяемого пользователем типа.

Удобные макросы **`alignof`** и **`alignas`** , определенные в `<stdalign.h>`, напрямую сопоставляются с **`_Alignof`** и **`_Alignas`** соответственно. Эти макросы соответствуют ключевым словам, используемым в C++. Поэтому использование макросов вместо ключевых слов C может оказаться полезным для переноса кода, если в вашем коде используется два языка.

## <a name="alignas-and-_alignas-c11"></a>`alignas` и `_Alignas` (C11)

Чтобы указать пользовательское выравнивание для переменной или определяемого пользователем типа, используйте **`alignas`** или **`_Alignas`** . Их можно применить к структуре, объединению, перечислению или переменной.

### <a name="alignas-syntax"></a>Синтаксис `alignas`

```c
alignas(type)
alignas(constant-expression)
_Alignas(type)
_Alignas(constant-expression)
```

### <a name="remarks"></a>Remarks

`_Alignas` нельзя использовать в объявлении typedef, битового поля, функции, параметра функции или объекта, объявленного с описателем `register`.

Укажите выравнивание, которое является степенью двух, например 1, 2, 4, 8, 16 и т. д. Не используйте значение меньше размера типа.

Структуры и объединения имеют выравнивание, равное значению самого крупного выравнивания любого элемента. В структуры добавляются байты заполнения, чтобы обеспечить соблюдение требований к выравниванию отдельных элементов.

Если в объявлении есть несколько описателей **`alignas`** (например, структура с несколькими элементами, которые включают разные описатели **`alignas`** ), к структуре будет применяться выравнивание самого крупного элемента.

### <a name="alignas-example"></a>Пример `alignas`

В этом примере используется удобный макрос **`alignof`** , так как его можно перенести в C++. Если вы используете `_Alignof`, поведение будет аналогичным.

```c
// Compile with /std:c11

#include <stdio.h>
#include <stdalign.h>

typedef struct 
{
    int value; // aligns on a 4-byte boundary. There will be 28 bytes of padding between value and alignas
    alignas(32) char alignedMemory[32]; // assuming a 32 byte friendly cache alignment
} cacheFriendly; // this struct will be 32-byte aligned because alignedMemory is 32-byte alligned and is the largest alignment specified in the struct

int main()
{
    printf("sizeof(cacheFriendly): %d\n", sizeof(cacheFriendly)); // 4 bytes for int value + 32 bytes for alignedMemory[] + padding to ensure  alignment
    printf("alignof(cacheFriendly): %d\n", alignof(cacheFriendly)); // 32 because alignedMemory[] is aligned on a 32-byte boundary

    /* output
        sizeof(cacheFriendly): 64
        alignof(cacheFriendly): 32
    */
}
```

## <a name="alignof-and-_alignof-c11"></a>`alignof` и `_Alignof` (C11)

`_Alignof` возвращает выравнивание в байтах для указанного типа. Возвращает значение типа `size_t`.

### <a name="alignof-syntax"></a>Синтаксис `alignof`

```cpp
alignof(type)
_Alignof(type)
```

### <a name="alignof-example"></a>Пример `alignof`

В этом примере используется удобный макрос **`alignof`** , так как его можно перенести в C++. Если вы используете `_Alignof`, поведение будет аналогичным.

```c
// Compile with /std:c11

#include <stdalign.h>
#include <stdio.h>

int main()
{
    size_t alignment = alignof(short);
    printf("alignof(short) = %d\n", alignment); // 2
    printf("alignof(int) = %d\n", alignof(int)); // 4
    printf("alignof(long) = %d\n", alignof(long)); // 4
    printf("alignof(float) = %d\n", alignof(float)); // 4
    printf("alignof(double) = %d\n", alignof(double)); // 8

    typedef struct
    {
        int a;
        double b;
    } test;

    printf("alignof(test) = %d\n", alignof(test)); // 8 because that is the alignment of the largest element in the structure

    /* output
        
       alignof(short) = 2
       alignof(int) = 4
       alignof(long) = 4
       alignof(float) = 4
       alignof(double) = 8
       alignof(test) = 8
    */
}
```

## <a name="requirements"></a>Требования

Требуется [std:c++11](../build/reference/std-specify-language-standard-version.md) или более поздней версии.

Пакет Windows SDK версии 10.0.20201.0 или более поздней. В настоящее время эта версия является сборкой для участников программы предварительной оценки Windows, которую можно скачать [здесь](https://www.microsoft.com/software-download/windowsinsiderpreviewSDK). Инструкции по установке и использованию этого пакета SDK см. в разделе [C11 и C17. Начало работы](https://devblogs.microsoft.com/cppblog/c11-and-c17-standard-support-arriving-in-msvc/#c11-and-c17-getting-started).

## <a name="see-also"></a>См. также раздел

[`/std` (определение стандартной версии языка)](../build/reference/std-specify-language-standard-version.md)\
[C++ `alignof` и `alignas`](../cpp/alignment-cpp-declarations.md#alignof-and-alignas)\
[Обработка выравнивания данных компилятором](../cpp/alignment-cpp-declarations.md#compiler-handling-of-data-alignment)