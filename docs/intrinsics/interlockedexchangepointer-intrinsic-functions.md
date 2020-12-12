---
description: 'Дополнительные сведения: _InterlockedExchangePointer встроенных функций'
title: Встроенные функции _InterlockedExchangePointer
ms.date: 09/02/2019
f1_keywords:
- _InterlockedExchangePointer_cpp
- _InterlockedExchangePointer_rel
- _InterlockedExchangePointer_nf
- _InterlockedExchangePointer_HLERelease
- _InterlockedExchangePointer_acq
- _InterlockedExchangePointer
- _InterlockedExchangePointer_acq_cpp
- _InterlockedExchangePointer_HLEAcquire
helpviewer_keywords:
- _InterlockedExchangePointer_rel intrinsic
- _InterlockedExchangePointer_HLERelease intrinsic
- _InterlockedExchangePointer intrinsic
- _InterlockedExchangePointer_nf intrinsic
- _InterlockedExchangePointer_acq intrinsic
- _InterlockedExchangePointer_HLEAcquire intrinsic
- InterlockedExchangePointer_acq intrinsic
- InterlockedExchangePointer intrinsic
ms.assetid: 0eaca0b0-d79e-406b-892d-b3b462c50bbb
ms.openlocfilehash: 0bb6080b9bca38c67b12b28976b49eb84f74e6c7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167998"
---
# <a name="_interlockedexchangepointer-intrinsic-functions"></a>Встроенные функции _InterlockedExchangePointer

**Блок, относящийся только к системам Microsoft**

Выполняет атомарную операцию Exchange, которая копирует адрес, переданный в качестве второго аргумента, в первый аргумент и возвращает исходный адрес первого объекта.

## <a name="syntax"></a>Синтаксис

```C
void * _InterlockedExchangePointer(
   void * volatile * Target,
   void * Value
);
void * _InterlockedExchangePointer_acq(
   void * volatile * Target,
   void * Value
);
void * _InterlockedExchangePointer_rel(
   void * volatile * Target,
   void * Value
);
void * _InterlockedExchangePointer_nf(
   void * volatile * Target,
   void * Value
);
void * _InterlockedExchangePointer_HLEAcquire(
   void * volatile * Target,
   void * Value
);
void * _InterlockedExchangePointer_HLERelease(
   void * volatile * Target,
   void * Value
);
```

### <a name="parameters"></a>Параметры

*Мишень*\
[вход, выход] Указатель на указатель на значение для обмена. Функция устанавливает значение в *значение* и возвращает свое предыдущее значение.

*Значение*\
окне Значение для обмена со значением, на которое указывает *целевой объект*.

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает начальное значение, на которое указывает *целевой объект*.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|Заголовок|
|---------------|------------------|------------|
|`_InterlockedExchangePointer`|x86, ARM, x64, ARM64|\<intrin.h>|
|`_InterlockedExchangePointer_acq`, `_InterlockedExchangePointer_rel`, `_InterlockedExchangePointer_nf`|ARM, ARM64|\<intrin.h>|
|`_InterlockedExchangePointer_HLEAcquire`, `_InterlockedExchangePointer_HLERelease`|X64|\<immintrin.h>|

В архитектуре x86, `_InterlockedExchangePointer` есть макрос, вызывающий `_InterlockedExchange`.

## <a name="remarks"></a>Комментарии

В 64-разрядной системе параметры имеют значение 64 бит и должны быть согласованы по отношению к 64-разрядным границам. В противном случае произойдет сбой функции. Для 32-разрядной системы параметры 32-разрядные и должны быть выровнены по 32-разрядням границам. Дополнительные сведения см. в разделе [выровняйте](../cpp/align-cpp.md).

На платформах ARM используйте встроенные функции с суффиксами `_acq` и `_rel`, если нужно получить и освободить семантику, например в начале и конце критической секции. Встроенная функция с `_nf` суффиксом ("без ограждения") не выступает в качестве барьера памяти.

На платформах Intel ®, поддерживающих инструкции Hardware Lock Elision (HLE), встроенные функции с суффиксами `_HLEAcquire` и `_HLERelease` включают подсказку процессору, как можно повысить производительность, устраняя шаг записи с блокировкой оборудования. Если эти встроенные функции вызываются на платформах, не поддерживающих HLE, подсказка игнорируется.

Эти процедуры доступны только как встроенные объекты.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[Конфликтует с компилятором x86](../build/x64-software-conventions.md#conflicts-with-the-x86-compiler)
