---
description: 'Дополнительные сведения: __rdtsc'
title: __rdtsc
ms.date: 09/02/2019
f1_keywords:
- __rdtsc
helpviewer_keywords:
- __rdtsc intrinsic
- rdtsc instruction
- Read Time Stamp Counter instruction
ms.assetid: e31d0e51-c9bb-42ca-bbe9-a81ffe662387
ms.openlocfilehash: 930c8fbd0ae762c8674a85e379899bc4fe4d3394
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257515"
---
# <a name="__rdtsc"></a>__rdtsc

**Блок, относящийся только к системам Microsoft**

Формирует `rdtsc` инструкцию, которая возвращает метку времени процессора. В метке времени процессора записывается число циклов часов с момента последнего сброса.

## <a name="syntax"></a>Синтаксис

```C
unsigned __int64 __rdtsc();
```

## <a name="return-value"></a>Возвращаемое значение

64-битовое целое число без знака, представляющее число тактов.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__rdtsc`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта подпрограммы доступна только в качестве встроенной функции.

Интерпретация значения TSC в последующих поколениях оборудования отличается от интерпретации в более ранних версиях x64. Дополнительные сведения см. в руководстве по оборудованию.

## <a name="example"></a>Пример

```cpp
// rdtsc.cpp
// processor: x86, x64
#include <stdio.h>
#include <intrin.h>

#pragma intrinsic(__rdtsc)

int main()
{
    unsigned __int64 i;
    i = __rdtsc();
    printf_s("%I64d ticks\n", i);
}
```

```Output
3363423610155519 ticks
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
