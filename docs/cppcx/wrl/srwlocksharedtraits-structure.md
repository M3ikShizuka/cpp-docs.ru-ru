---
description: 'Дополнительные сведения о: структура метод srwlocksharedtraits'
title: SRWLockSharedTraits - структура
ms.date: 09/27/2018
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockSharedTraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockSharedTraits::GetInvalidValue
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockSharedTraits::Unlock
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockSharedTraits structure
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockSharedTraits::GetInvalidValue method
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockSharedTraits::Unlock method
ms.assetid: 709cb51e-d70c-40b6-bdb4-d8eacf3af495
ms.openlocfilehash: 2cdfbd584adeffc9dedd8504d9183d6c5d4c1a95
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97135126"
---
# <a name="srwlocksharedtraits-structure"></a>SRWLockSharedTraits - структура

Описывает общие характеристики `SRWLock` класса в режиме общей блокировки.

## <a name="syntax"></a>Синтаксис

```cpp
struct SRWLockSharedTraits;
```

## <a name="members"></a>Члены

### <a name="public-typedefs"></a>Общедоступные определения типов

Имя   | Описание
------ | --------------------------------------------------------------------------
`Type` | Синоним для указателя на класс [SRWLock](srwlock-class.md) .

### <a name="public-methods"></a>Открытые методы

name                                                     | Описание
-------------------------------------------------------- | -----------------------------------------------------------------
[Метод srwlocksharedtraits:: GetInvalidValue](#getinvalidvalue) | Извлекает `SRWLockSharedTraits` объект, который всегда является недопустимым.
[Метод srwlocksharedtraits:: Unlock](#unlock)                   | Освобождает монопольный доступ к указанному `SRWLock` объекту.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`SRWLockSharedTraits`

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Microsoft:: WRL:: оболочки:: метод HandleTraits

## <a name="srwlocksharedtraitsgetinvalidvalue"></a><a name="getinvalidvalue"></a> Метод srwlocksharedtraits:: GetInvalidValue

Извлекает `SRWLockSharedTraits` объект, который всегда является недопустимым.

```cpp
inline static Type GetInvalidValue();
```

### <a name="return-value"></a>Возвращаемое значение

Маркер `SRWLockSharedTraits` объекта.

## <a name="srwlocksharedtraitsunlock"></a><a name="unlock"></a> Метод srwlocksharedtraits:: Unlock

Освобождает монопольный доступ к указанному `SRWLock` объекту.

```cpp
inline static void Unlock(
   _In_ Type srwlock
);
```

### <a name="parameters"></a>Параметры

*SRWLock*<br/>
Маркер `SRWLock` объекта.
