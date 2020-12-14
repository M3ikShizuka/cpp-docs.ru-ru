---
description: 'Дополнительные сведения о: структура FactoryCache'
title: FactoryCache - структура
ms.date: 09/21/2018
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::FactoryCache
- module/Microsoft::WRL::Details::FactoryCache::cookie
- module/Microsoft::WRL::Details::FactoryCache::factory
helpviewer_keywords:
- Microsoft::WRL::Details::FactoryCache structure
- Microsoft::WRL::Details::FactoryCache::cookie data member
- Microsoft::WRL::Details::FactoryCache::factory data member
ms.assetid: 624544e6-0989-47f6-a3e9-edb60e1ee6d4
ms.openlocfilehash: 3e9ee084a063eb8094c309dee412a8793801921b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97198559"
---
# <a name="factorycache-structure"></a>FactoryCache - структура

Поддерживает среда выполнения Windows инфраструктуру библиотеки шаблонов C++ и не предназначена для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
struct FactoryCache;
```

## <a name="remarks"></a>Remarks

Содержит местоположение фабрики класса и значение, которое идентифицирует зарегистрированный объект класса Среды выполнения Windows или модели COM.

## <a name="members"></a>Элементы

### <a name="public-data-members"></a>Открытые члены данных

Имя                              | Описание
--------------------------------- | ------------------------------------------------------------------------------------------------------------------------------
[FactoryCache:: cookie](#cookie)   | Содержит значение, идентифицирующее зарегистрированный среда выполнения Windows или объект класса COM, который затем используется для отмены регистрации объекта.
[FactoryCache:: Factory](#factory) | Указывает на фабрику классов среда выполнения Windows или COM.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`FactoryCache`

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="factorycachecookie"></a><a name="cookie"></a> FactoryCache:: cookie

Поддерживает среда выполнения Windows инфраструктуру библиотеки шаблонов C++ и не предназначена для непосредственного использования в коде.

```cpp
union {
   WINRT_REGISTRATION_COOKIE winrt;
   DWORD com;
} cookie;
```

### <a name="remarks"></a>Комментарии

Содержит значение, идентифицирующее зарегистрированный среда выполнения Windows или объект класса COM, который затем используется для отмены регистрации объекта.

## <a name="factorycachefactory"></a><a name="factory"></a> FactoryCache:: Factory

Поддерживает среда выполнения Windows инфраструктуру библиотеки шаблонов C++ и не предназначена для непосредственного использования в коде.

```cpp
IUnknown* factory;
```

### <a name="remarks"></a>Комментарии

Указывает на фабрику классов среда выполнения Windows или COM.
