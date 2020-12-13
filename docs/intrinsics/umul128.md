---
description: 'Дополнительные сведения: _umul128'
title: _umul128
ms.date: 09/02/2019
f1_keywords:
- __umul128
helpviewer_keywords:
- __umul128 intrinsic
ms.assetid: 13684df3-3ac7-467c-b258-a0e93bc490b5
ms.openlocfilehash: 7fd126b169bd01fc4d51d186879e019f8d86f008
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333597"
---
# <a name="_umul128"></a>_umul128

**Блок, относящийся только к системам Microsoft**

Умножает два 64-разрядных целых числа без знака, переданных в качестве первых двух аргументов, и помещает старшие 64 разряда произведения в 64-разрядное целое число без знака, на которое указывает `HighProduct` и возвращает младшие 64 разряда произведения.

## <a name="syntax"></a>Синтаксис

```C
unsigned __int64 _umul128(
   unsigned __int64 Multiplier,
   unsigned __int64 Multiplicand,
   unsigned __int64 *HighProduct
);
```

### <a name="parameters"></a>Параметры

*Множитель*\
окне Первое 64-разрядное целое число для умножения.

*Множимое*\
окне Второе 64-разрядное целое число для умножения.

*хигхпродукт*\
заполняет Старшие 64 разрядов продукта.

## <a name="return-value"></a>Возвращаемое значение

Младшие 64 разряда произведения.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|Заголовок|
|---------------|------------------|------------|
|`_umul128`|X64|\<intrin.h>|

## <a name="example"></a>Пример

```C
// umul128.c
// processor: x64

#include <stdio.h>
#include <intrin.h>

#pragma intrinsic(_umul128)

int main()
{
    unsigned __int64 a = 0x0fffffffffffffffI64;
    unsigned __int64 b = 0xf0000000I64;
    unsigned __int64 c, d;

    d = _umul128(a, b, &c);

    printf_s("%#I64x * %#I64x = %#I64x%I64x\n", a, b, c, d);
}
```

```Output
0xfffffffffffffff * 0xf0000000 = 0xeffffffffffffff10000000
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
