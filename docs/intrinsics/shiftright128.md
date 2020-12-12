---
description: 'Дополнительные сведения: __shiftright128'
title: __shiftright128
ms.date: 09/02/2019
f1_keywords:
- __shiftright128
helpviewer_keywords:
- __shiftright128 intrinsic
ms.assetid: 5419a6c4-0de1-43fb-b314-4faa5b2d051f
ms.openlocfilehash: 71f8a0d9b740ebfef5e930715e07d1ec31950269
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97306980"
---
# <a name="__shiftright128"></a>__shiftright128

**Блок, относящийся только к системам Microsoft**

Сдвигает 128-разрядную величину, представленную в виде двух 64-разрядныхвеличин и ,  вправо на количество разрядов, указанное в  и возвращает младшие 64 разряда результата.

## <a name="syntax"></a>Синтаксис

```C
unsigned __int64 __shiftright128(
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

Младшие 64 разряда результата.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__shiftright128`|X64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Это значение `Shift` всегда берется по модулю 64, и, например, при вызове `__shiftright128(0, 1, 64)`, функция будет сдвигать вправо старшую часть `0` разрядов и возвращать младшую часть `0`, а не `1`, как в противном случае можно было ожидать.

## <a name="example"></a>Пример

Пример см. в разделе [__shiftleft128](../intrinsics/shiftleft128.md).

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[__shiftleft128](../intrinsics/shiftleft128.md)\
[Встроенные объекты компилятора](../intrinsics/compiler-intrinsics.md)
