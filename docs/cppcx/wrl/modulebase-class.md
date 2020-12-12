---
description: 'Дополнительные сведения о: ModuleBase Class'
title: Класс ModuleBase
ms.date: 09/21/2018
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::ModuleBase
- implements/Microsoft::WRL::Details::ModuleBase::DecrementObjectCount
- implements/Microsoft::WRL::Details::ModuleBase::IncrementObjectCount
- implements/Microsoft::WRL::Details::ModuleBase::ModuleBase
- implements/Microsoft::WRL::Details::ModuleBase::~ModuleBase
helpviewer_keywords:
- ModuleBase class
- Microsoft::WRL::Details::ModuleBase::DecrementObjectCount method
- Microsoft::WRL::Details::ModuleBase::IncrementObjectCount method
- Microsoft::WRL::Details::ModuleBase::ModuleBase, constructor
- Microsoft::WRL::Details::ModuleBase::~ModuleBase, destructor
ms.assetid: edce7591-6893-46f7-94a7-382827775548
ms.openlocfilehash: 6540068cee62da5d1a9039a15bcb5bd53ff3aea2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97186250"
---
# <a name="modulebase-class"></a>Класс ModuleBase

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
class ModuleBase;
```

## <a name="remarks"></a>Remarks

Представляет базовый класс для классов [модулей](module-class.md) .

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

name                                         | Описание
-------------------------------------------- | ---------------------------------------------------------
[ModuleBase:: ModuleBase](#modulebase)        | Инициализирует экземпляр класса `Module`.
[ModuleBase:: ~ ModuleBase](#tilde-modulebase) | Выполняет деинициализацию текущего экземпляра `Module` класса.

### <a name="public-methods"></a>Открытые методы

name                                                      | Описание
--------------------------------------------------------- | -------------------------------------------------------------------------
[ModuleBase::D Екрементобжекткаунт](#decrementobjectcount) | При реализации уменьшает число объектов, отслеживаемых модулем.
[ModuleBase:: IncrementObjectCount](#incrementobjectcount) | При реализации увеличивает число объектов, отслеживаемых модулем.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`ModuleBase`

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="modulebasemodulebase"></a><a name="tilde-modulebase"></a> ModuleBase:: ~ ModuleBase

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
virtual ~ModuleBase();
```

### <a name="remarks"></a>Комментарии

Выполняет деинициализацию текущего экземпляра `ModuleBase` класса.

## <a name="modulebasedecrementobjectcount"></a><a name="decrementobjectcount"></a> ModuleBase::D Екрементобжекткаунт

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
virtual long DecrementObjectCount() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Число до операции декремента.

### <a name="remarks"></a>Комментарии

При реализации уменьшает число объектов, отслеживаемых модулем.

## <a name="modulebaseincrementobjectcount"></a><a name="incrementobjectcount"></a> ModuleBase:: IncrementObjectCount

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
virtual long IncrementObjectCount() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Число до операции приращения.

### <a name="remarks"></a>Комментарии

При реализации увеличивает число объектов, отслеживаемых модулем.

## <a name="modulebasemodulebase"></a><a name="modulebase"></a> ModuleBase:: ModuleBase

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
ModuleBase();
```

### <a name="remarks"></a>Комментарии

Инициализирует экземпляр класса `Module`.
