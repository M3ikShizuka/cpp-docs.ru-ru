---
description: 'Дополнительные сведения: _udiv64'
title: _udiv64
ms.date: 09/02/2019
f1_keywords:
- _udiv64
helpviewer_keywords:
- _udiv64 intrinsic
ms.openlocfilehash: 21f383cd78885ab8d3d8bb66a87623a73b59ff95
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333638"
---
# <a name="_udiv64"></a>_udiv64

`_udiv64`Функция делит 64-разрядное целое число без знака на 32-разрядное целое число без знака. Возвращаемое значение содержит частное, а внутренний возвращает остаток через параметр указателя. `_udiv64` зависит **от корпорации Майкрософт**.

## <a name="syntax"></a>Синтаксис

```C
unsigned int _udiv64(
   unsigned __int64 dividend,
   unsigned int divisor,
   unsigned int* remainder
);
```

### <a name="parameters"></a>Параметры

*дивиденд*\
окне 64-битовое целое число без знака для деления.

*равн*\
окне 32-битовое целое число без знака для деления на.

*дальнейшем*\
заполняет Остаток от 32-разрядного целого числа без знака.

## <a name="return-value"></a>Возвращаемое значение

32 бит частного.

## <a name="remarks"></a>Комментарии

`_udiv64`Внутренние деления, *делимые* на *делитель*. Он сохраняет остаток в 32-битовом целом число без знака, на который указывает *остаток*, и возвращает биты числа 32.

`_udiv64`Встроенная функция доступна начиная с Visual Studio 2019 RTM.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|Заголовок|
|---------------|------------------|------------|
|`_udiv64`|x86, x64|\<immintrin.h>|

## <a name="see-also"></a>См. также раздел

[_div64](div64.md) \
[Встроенные объекты компилятора](compiler-intrinsics.md)
