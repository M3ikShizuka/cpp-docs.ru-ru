---
description: 'Дополнительные сведения: _interlockedbittestandset встроенных функций'
title: встроенные функции _interlockedbittestandset
ms.date: 09/02/2019
f1_keywords:
- _interlockedbittestandset_cpp
- _interlockedbittestandset_HLEAcquire
- _interlockedbittestandset64
- _interlockedbittestandset64_acq
- _interlockedbittestandset64_nf
- _interlockedbittestandset64_rel
- _interlockedbittestandset
- _interlockedbittestandset_rel
- _interlockedbittestandset64_HLEAcquire
- _interlockedbittestandset_HLERelease
- _interlockedbittestandset_acq
- _interlockedbittestandset_nf
- _interlockedbittestandset64_cpp
- _interlockedbittestandset64_HLERelease
helpviewer_keywords:
- _interlockedbittestandset intrinsic
- _interlockedbittestandset64 intrinsic
- lock_bts instruction
ms.assetid: b1b7e334-53ea-48cf-ba60-5fa3ef51a1fc
ms.openlocfilehash: bc1ee5e70c5b892b7c98bb9cb03f75b3baeda268
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97168206"
---
# <a name="_interlockedbittestandset-intrinsic-functions"></a>встроенные функции _interlockedbittestandset

**Блок, относящийся только к системам Microsoft**

Создайте инструкцию, чтобы проверить бит `b` адреса `a` и вернуть его текущее значение перед заданием значения 1.

## <a name="syntax"></a>Синтаксис

```C
unsigned char _interlockedbittestandset(
   long *a,
   long b
);
unsigned char _interlockedbittestandset_acq(
   long *a,
   long b
);
unsigned char _interlockedbittestandset_HLEAcquire(
   long *a,
   long b
);
unsigned char _interlockedbittestandset_HLERelease(
   long *a,
   long b
);
unsigned char _interlockedbittestandset_nf(
   long *a,
   long b
);
unsigned char _interlockedbittestandset_rel(
   long *a,
   long b
);
unsigned char _interlockedbittestandset64(
   __int64 *a,
   __int64 b
);
unsigned char _interlockedbittestandset64_acq(
   __int64 *a,
   __int64 b
);
unsigned char _interlockedbittestandset64_nf(
   __int64 *a,
   __int64 b
);
unsigned char _interlockedbittestandset64_rel(
   __int64 *a,
   __int64 b
);
unsigned char _interlockedbittestandset64_HLEAcquire(
   __int64 *a,
   __int64 b
);
unsigned char _interlockedbittestandset64_HLERelease(
   __int64 *a,
   __int64 b
);
```

### <a name="parameters"></a>Параметры

*конкретного*\
окне Указатель на память для проверки.

*&*\
окне Битовое расположение для проверки.

## <a name="return-value"></a>Возвращаемое значение

Значение бита в позиции `b` до его установки.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|Заголовок|
|---------------|------------------|------------|
|`_interlockedbittestandset`|x86, ARM, x64, ARM64|\<intrin.h>|
|`_interlockedbittestandset_acq`, `_interlockedbittestandset_nf`, `_interlockedbittestandset_rel`|ARM, ARM64|\<intrin.h>|
|`_interlockedbittestandset64_acq`, `_interlockedbittestandset64_nf`, `_interlockedbittestandset64_rel`|ARM64|\<intrin.h>|
|`_interlockedbittestandset_HLEAcquire`, `_interlockedbittestandset_HLERelease`|x86, x64|\<immintrin.h>|
|`_interlockedbittestandset64`|x64, ARM64|\<intrin.h>|
|`_interlockedbittestandset64_HLEAcquire`, `_interlockedbittestandset64_HLERelease`|X64|\<immintrin.h>|

## <a name="remarks"></a>Комментарии

На процессорах x86 и x64 эти встроенные функции используют `lock bts` инструкцию для чтения и установки указанного бита в значение 1. Эта операция является атомарной.

В процессорах ARM и ARM64 используйте встроенные функции с `_acq` `_rel` суффиксами и для семантики получения и освобождения, например в начале и в конце критической секции. Встроенные функции ARM с `_nf` суффиксом ("без ограждения") не действуют как барьер памяти.

Для процессоров Intel, поддерживающих инструкции Hardware Lock Elision (HLE), встроенные функции с суффиксами`_HLEAcquire` и `_HLERelease` включают подсказку процессору, как можно повысить производительность, устраняя шаг записи с блокировкой оборудования. Если эти встроенные функции вызываются для процессоров, не поддерживающих HLE, подсказка игнорируется.

Эти процедуры доступны только как встроенные объекты.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[Конфликтует с компилятором x86](../build/x64-software-conventions.md#conflicts-with-the-x86-compiler)
