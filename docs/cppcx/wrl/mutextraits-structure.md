---
description: 'Дополнительные сведения о: структура метод mutextraits'
title: MutexTraits - структура
ms.date: 09/27/2018
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::MutexTraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::MutexTraits::Unlock
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::MutexTraits structure
- Microsoft::WRL::Wrappers::HandleTraits::MutexTraits::Unlock method
ms.assetid: 6582df80-b9ba-4892-948f-d572a3b23d54
ms.openlocfilehash: e3dfcee1251794734ed5cf787096361403d80c7f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330810"
---
# <a name="mutextraits-structure"></a>MutexTraits - структура

Определяет общие характеристики класса [мьютекса](mutex-class.md) .

## <a name="syntax"></a>Синтаксис

```cpp
struct MutexTraits : HANDLENullTraits;
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

name                           | Описание
------------------------------ | ------------------------------------------------
[Метод mutextraits:: Unlock](#unlock) | Освобождает монопольный контроль над общим ресурсом.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`HANDLENullTraits`

`MutexTraits`

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Microsoft:: WRL:: оболочки:: метод HandleTraits

## <a name="mutextraitsunlock-method"></a><a name="unlock"></a> Метод метод mutextraits:: Unlock

Освобождает монопольный контроль над общим ресурсом.

```cpp
inline static void Unlock(
   _In_ Type h
);
```

### <a name="parameters"></a>Параметры

*h*<br/>
Обработчик объекта мьютекса.
