---
description: 'Дополнительные сведения: __shiftleft128'
title: __shiftleft128
ms.date: 09/02/2019
f1_keywords:
- __shiftleft128
helpviewer_keywords:
- __shiftleft128 intrinsic
ms.assetid: 557b846a-8fb0-469d-91ac-1b1fad80dc2a
ms.openlocfilehash: e0e1402660c2ddb6f5993e5186302ff489ed864f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97306993"
---
# <a name="__shiftleft128"></a>__shiftleft128

**Блок, относящийся только к системам Microsoft**

Сдвигает 128-разрядную величину, представленную в виде двух величин по 64-разряда `LowPart` и `HighPart`, влево на количество разрядов, указанное в `Shift` и возвращает старшие 64 разряда результата.

## <a name="syntax"></a>Синтаксис

```C
unsigned __int64 __shiftleft128(
   unsigned __int64 LowPart,
   unsigned __int64 HighPart,
   unsigned char Shift
);
```

### <a name="parameters"></a>Параметры

*ловпарт*\
окне Младший 64 бит 128-разрядного количества для сдвига.

*хигхпарт*\
окне Старшие 64 бит 128-разрядного количества для сдвига.

*Мести*\
окне Число битов для сдвига.

## <a name="return-value"></a>Возвращаемое значение

Старшие 64 разряда результата.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__shiftleft128`|X64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Значение *сдвига* всегда равно модулю 64, поэтому, например, при вызове функция переместит `__shiftleft128(1, 0, 64)` младшие `0` биты влево и возвратит большую часть `0` , а не `1` так, как может быть в противном случае.

## <a name="example"></a>Пример

```C
// shiftleft128.c
// processor: IPF, x64
#include <stdio.h>
#include <intrin.h>

#pragma intrinsic (__shiftleft128, __shiftright128)

int main()
{
    unsigned __int64 i = 0x1I64;
    unsigned __int64 j = 0x10I64;
    unsigned __int64 ResultLowPart;
    unsigned __int64 ResultHighPart;

    ResultLowPart = i << 1;
    ResultHighPart = __shiftleft128(i, j, 1);

    // concatenate the low and high parts padded with 0's
    // to display correct hexadecimal 128 bit values
    printf_s("0x%02I64x%016I64x << 1 = 0x%02I64x%016I64x\n",
             j, i, ResultHighPart, ResultLowPart);

    ResultHighPart = j >> 1;
    ResultLowPart = __shiftright128(i, j, 1);

    printf_s("0x%02I64x%016I64x >> 1 = 0x%02I64x%016I64x\n",
             j, i, ResultHighPart, ResultLowPart);
}
```

```Output
0x100000000000000001 << 1 = 0x200000000000000002
0x100000000000000001 >> 1 = 0x080000000000000000
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[__shiftright128](../intrinsics/shiftright128.md)\
[Встроенные объекты компилятора](../intrinsics/compiler-intrinsics.md)
