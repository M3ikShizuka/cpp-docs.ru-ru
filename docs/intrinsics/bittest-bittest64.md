---
description: 'Дополнительные сведения: _bittest, _bittest64'
title: _bittest, _bittest64
ms.date: 09/02/2019
f1_keywords:
- _bittest64
- _bittest_cpp
- _bittest64_cpp
- _bittest
helpviewer_keywords:
- _bittest intrinsic
- _bittest64 intrinsic
- bt instruction
ms.assetid: 15e62afb-abea-4ee7-a6b1-13efa2034937
ms.openlocfilehash: 50c0f1637fefab9bd39fcbca2cd18571c7769bd8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337206"
---
# <a name="_bittest-_bittest64"></a>_bittest, _bittest64

**Блок, относящийся только к системам Microsoft**

Создает инструкцию `bt`, которая проверяет разряд в позиции `b` адреса `a` и возвращает значение разряда.

## <a name="syntax"></a>Синтаксис

```C
unsigned char _bittest(
   long const *a,
   long b
);
unsigned char _bittest64(
   __int64 const *a,
   __int64 b
);
```

### <a name="parameters"></a>Параметры

*конкретного*\
окне Указатель на память для проверки.

*&*\
окне Битовое расположение для проверки.

### <a name="return-value"></a>Возвращаемое значение

Разряд на указанной позиции.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|Заголовок|
|---------------|------------------|------------|
|`_bittest`|x86, ARM, x64, ARM64|\<intrin.h>|
|`_bittest64`|ARM64, x64|\<intrin.h>|

## <a name="remarks"></a>Комментарии

Эта процедура доступна только как встроенная функция.

## <a name="example"></a>Пример

```cpp
// bittest.cpp
// processor: x86, ARM, x64

#include <stdio.h>
#include <intrin.h>

long num = 78002;

int main()
{
    unsigned char bits[32];
    long nBit;

    printf_s("Number: %d\n", num);

    for (nBit = 0; nBit < 31; nBit++)
    {
        bits[nBit] = _bittest(&num, nBit);
    }

    printf_s("Binary representation:\n");
    while (nBit--)
    {
        if (bits[nBit])
            printf_s("1");
        else
            printf_s("0");
    }
}
```

```Output
Number: 78002
Binary representation:
0000000000000010011000010110010
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
