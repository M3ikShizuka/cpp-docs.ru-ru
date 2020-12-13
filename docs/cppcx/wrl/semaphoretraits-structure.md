---
description: 'Дополнительные сведения о: структура метод semaphoretraits'
title: SemaphoreTraits - структура
ms.date: 09/27/2018
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SemaphoreTraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SemaphoreTraits::Unlock
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::SemaphoreTraits structure
- Microsoft::WRL::Wrappers::HandleTraits::SemaphoreTraits::Unlock method
ms.assetid: eddb8576-d063-409b-9201-cc87ca5d111e
ms.openlocfilehash: 5779a30d22fd2d32e57f96f752bb52e2bf469cd8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97135230"
---
# <a name="semaphoretraits-structure"></a>SemaphoreTraits - структура

Определяет общие характеристики `Semaphore` объекта.

## <a name="syntax"></a>Синтаксис

```cpp
struct SemaphoreTraits : HANDLENullTraits;
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

name                               | Описание
---------------------------------- | --------------------------------------
[Метод semaphoretraits:: Unlock](#unlock) | Выпускают управление общим ресурсом.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`HANDLENullTraits`

`SemaphoreTraits`

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Microsoft:: WRL:: оболочки:: метод HandleTraits

## <a name="semaphoretraitsunlock"></a><a name="unlock"></a> Метод semaphoretraits:: Unlock

Выпускают управление общим ресурсом.

```cpp
inline static void Unlock(
   _In_ Type h
);
```

### <a name="parameters"></a>Параметры

*h*<br/>
Обработчик для `Semaphore` объекта.

### <a name="remarks"></a>Комментарии

Если операция разблокировки завершилась неудачно, `Unlock()` выдает ошибку, которая указывает на причину сбоя.
