---
description: 'Дополнительные сведения: _InterlockedAddLargeStatistic'
title: _InterlockedAddLargeStatistic
ms.date: 09/02/2019
f1_keywords:
- _InterlockedAddLargeStatistic
- _InterlockedAddLargeStatistic_cpp
helpviewer_keywords:
- _InterlockedAddLargeStatistic intrinsic
- InterlockedAddLargeStatistic intrinsic
ms.assetid: 2802e74b-bcee-46e4-b562-894908d44409
ms.openlocfilehash: 52ca32d0f9b08d638a66923f8f0204eb515b447e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336878"
---
# <a name="_interlockedaddlargestatistic"></a>_InterlockedAddLargeStatistic

**Блок, относящийся только к системам Microsoft**

Выполняет сложение с блокировкой, в котором первый операнд является 64-битным значением.

## <a name="syntax"></a>Синтаксис

```C
long _InterlockedAddLargeStatistic(
   __int64 volatile * Addend,
   long Value
);
```

### <a name="parameters"></a>Параметры

*Слагаемое*\
[вход, выход] Указатель на первый операнд операции добавления. Значение, на которое указывает, заменяется результатом сложения.

*Значение*\
окне Второй операнд; значение, добавляемое к первому операнду.

## <a name="return-value"></a>Возвращаемое значение

Значение второго операнда.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`_InterlockedAddLargeStatistic`|x86|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

`_InterlockedAddLargeStatistic`Встроенная функция не является атомарной, поскольку реализуется как две отдельные инструкции блокировки. Атомарный 64-разрядный Read, происходящий в другом потоке во время выполнения встроенного параметра, может привести к считыванию несогласованного значения.

`_InterlockedAddLargeStatistic` ведет себя как барьер для чтения и записи. Дополнительные сведения см. в разделе [_ReadWriteBarrier](../intrinsics/readwritebarrier.md).

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[Конфликтует с компилятором x86](../build/x64-software-conventions.md#conflicts-with-the-x86-compiler)
