---
description: 'Дополнительные сведения о: структура метод srwlockexclusivetraits'
title: SRWLockExclusiveTraits - структура
ms.date: 09/27/2018
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::GetInvalidValue
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::Unlock
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits structure
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::GetInvalidValue method
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::Unlock method
ms.assetid: 38a996ef-c2d7-4886-b413-a426ecee8f05
ms.openlocfilehash: 135d4f866d1ca32ee9170ef9844cb0bf8d38c29a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97186211"
---
# <a name="srwlockexclusivetraits-structure"></a>SRWLockExclusiveTraits - структура

Описывает общие характеристики `SRWLock` класса в режиме монопольной блокировки.

## <a name="syntax"></a>Синтаксис

```cpp
struct SRWLockExclusiveTraits;
```

## <a name="members"></a>Члены

### <a name="public-typedefs"></a>Общедоступные определения типов

Имя   | Описание
------ | --------------------------------------------------------------------------
`Type` | Синоним для указателя на класс [SRWLock](srwlock-class.md) .

### <a name="public-methods"></a>Открытые методы

name                                                        | Описание
----------------------------------------------------------- | --------------------------------------------------------------------
[Метод srwlockexclusivetraits:: GetInvalidValue](#getinvalidvalue) | Извлекает `SRWLockExclusiveTraits` объект, который всегда является недопустимым.
[Метод srwlockexclusivetraits:: Unlock](#unlock)                   | Освобождает монопольный доступ к указанному `SRWLock` объекту.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`SRWLockExclusiveTraits`

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Microsoft:: WRL:: оболочки:: метод HandleTraits

## <a name="srwlockexclusivetraitsgetinvalidvalue"></a><a name="getinvalidvalue"></a> Метод srwlockexclusivetraits:: GetInvalidValue

Извлекает `SRWLockExclusiveTraits` объект, который всегда является недопустимым.

```cpp
inline static Type GetInvalidValue();
```

### <a name="return-value"></a>Возвращаемое значение

Пустой объект `SRWLockExclusiveTraits`.

## <a name="srwlockexclusivetraitsunlock"></a><a name="unlock"></a> Метод srwlockexclusivetraits:: Unlock

Освобождает монопольный доступ к указанному `SRWLock` объекту.

```cpp
inline static void Unlock(
   _In_ Type srwlock
);
```

### <a name="parameters"></a>Параметры

*SRWLock*<br/>
Обработчик `SRWLock` объекта.
