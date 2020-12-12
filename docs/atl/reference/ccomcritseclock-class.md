---
description: 'Дополнительные сведения о: Ккомкритсеклокк Class'
title: Класс Ккомкритсеклокк
ms.date: 11/04/2016
f1_keywords:
- CComCritSecLock
- ATLBASE/ATL::CComCritSecLock
- ATLBASE/ATL::CComCritSecLock::CComCritSecLock
- ATLBASE/ATL::CComCritSecLock::Lock
- ATLBASE/ATL::CComCritSecLock::Unlock
helpviewer_keywords:
- CComCritSecLock class
ms.assetid: 223152a1-86c3-4ef9-89a7-f455fe791b0e
ms.openlocfilehash: 7cad44f062fe75418da1f948c5f180283142779b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152104"
---
# <a name="ccomcritseclock-class"></a>Класс Ккомкритсеклокк

Этот класс предоставляет методы для блокировки и разблокировки объекта критической секции.

## <a name="syntax"></a>Синтаксис

```
template<class TLock> class CComCritSecLock
```

#### <a name="parameters"></a>Параметры

*тлокк*<br/>
Объект, который должен быть заблокирован и разблокирован.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккомкритсеклокк:: Ккомкритсеклокк](#ctor)|Конструктор.|
|[Ккомкритсеклокк:: ~ Ккомкритсеклокк](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомкритсеклокк:: Lock](#lock)|Вызовите этот метод, чтобы заблокировать объект критической секции.|
|[Ккомкритсеклокк:: Unlock](#unlock)|Вызовите этот метод, чтобы разблокировать объект критической секции.|

## <a name="remarks"></a>Комментарии

Используйте этот класс для блокировки и разблокирования объектов в более безопасном виде, чем класс [ккомкритикалсектион](../../atl/reference/ccomcriticalsection-class.md) или [класс ккомаутокритикалсектион](../../atl/reference/ccomautocriticalsection-class.md).

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="ccomcritseclockccomcritseclock"></a><a name="ctor"></a> Ккомкритсеклокк:: Ккомкритсеклокк

Конструктор.

```
CComCritSecLock(TLock& cs, bool bInitialLock = true);
```

### <a name="parameters"></a>Параметры

*сложных*<br/>
Объект критического раздела.

*бинитиаллокк*<br/>
Начальное состояние блокировки: **`true`** означает, что заблокировано.

### <a name="remarks"></a>Комментарии

Инициализирует объект критической секции.

## <a name="ccomcritseclockccomcritseclock"></a><a name="dtor"></a> Ккомкритсеклокк:: ~ Ккомкритсеклокк

Деструктор

```
~CComCritSecLock() throw();
```

### <a name="remarks"></a>Комментарии

Разблокирует объект критической секции.

## <a name="ccomcritseclocklock"></a><a name="lock"></a> Ккомкритсеклокк:: Lock

Вызовите этот метод, чтобы заблокировать объект критической секции.

```
HRESULT Lock() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK, если объект был успешно заблокирован, или ошибка HRESULT при сбое.

### <a name="remarks"></a>Комментарии

Если объект уже заблокирован, в отладочных сборках произойдет ошибка ASSERT.

## <a name="ccomcritseclockunlock"></a><a name="unlock"></a> Ккомкритсеклокк:: Unlock

Вызовите этот метод, чтобы разблокировать объект критической секции.

```cpp
void Unlock() throw();
```

### <a name="remarks"></a>Комментарии

Если объект уже разблокирован, в отладочных сборках произойдет ошибка ASSERT.

## <a name="see-also"></a>См. также раздел

[Класс Ккомкритикалсектион](../../atl/reference/ccomcriticalsection-class.md)<br/>
[Класс Ккомаутокритикалсектион](../../atl/reference/ccomautocriticalsection-class.md)
