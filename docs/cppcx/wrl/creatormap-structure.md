---
description: 'Дополнительные сведения о: структура CreatorMap'
title: CreatorMap - структура
ms.date: 09/21/2018
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::CreatorMap
- implements/Microsoft::WRL::Details::CreatorMap
- module/Microsoft::WRL::Details::CreatorMap::activationId
- module/Microsoft::WRL::Details::CreatorMap::factoryCache
- module/Microsoft::WRL::Details::CreatorMap::factoryCreator
- module/Microsoft::WRL::Details::CreatorMap::serverName
helpviewer_keywords:
- Microsoft::WRL::Details::CreatorMap structure
- Microsoft::WRL::Details::CreatorMap::activationId data member
- Microsoft::WRL::Details::CreatorMap::factoryCache data member
- Microsoft::WRL::Details::CreatorMap::factoryCreator data member
- Microsoft::WRL::Details::CreatorMap::serverName data member
ms.assetid: 94e40927-90c3-4107-bca3-3ad2dc4beda9
ms.openlocfilehash: 0ef3b441390a22a6c4b35f274857ccb58de030d9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97273050"
---
# <a name="creatormap-structure"></a>CreatorMap - структура

Поддерживает среда выполнения Windows инфраструктуру библиотеки шаблонов C++ и не предназначена для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
struct CreatorMap;
```

## <a name="remarks"></a>Remarks

Содержит сведения о том, как выполнять инициализацию, регистрацию и отмену регистрации объектов.

`CreatorMap` содержит следующие сведения:

- Инициализация, регистрация и Отмена регистрации объектов.

- Сравнение данных активации в зависимости от классической фабрики COM или среда выполнения Windows.

- Сведения о кэше фабрики и имени сервера для интерфейса.

## <a name="members"></a>Элементы

### <a name="public-data-members"></a>Открытые члены данных

Имя                                          | Описание
--------------------------------------------- | ------------------------------------------------------------------------------------------------------
[CreatorMap:: activationId](#activationid)     | Представляет идентификатор объекта, идентифицируемый с помощью классического COM-класса или имени среда выполнения Windows.
[CreatorMap:: factoryCache](#factorycache)     | Хранит указатель на кэш фабрики для `CreatorMap` .
[CreatorMap:: factoryCreator](#factorycreator) | Создает фабрику для указанного `CreatorMap` .
[CreatorMap:: serverName](#servername)         | Хранит имя сервера для `CreatorMap` .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CreatorMap`

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="creatormapactivationid"></a><a name="activationid"></a> CreatorMap:: activationId

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
union {
   const IID* clsid;
   const wchar_t* (*getRuntimeName)();
} activationId;
```

### <a name="parameters"></a>Параметры

*этому*<br/>
Идентификатор интерфейса.

*жетрунтименаме*<br/>
Функция, которая извлекает имя объекта в среде выполнения Windows.

### <a name="remarks"></a>Комментарии

Представляет идентификатор объекта, который определен идентификатором класса классической модели COM или именем в среде выполнения Windows.

## <a name="creatormapfactorycache"></a><a name="factorycache"></a> CreatorMap:: factoryCache

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
FactoryCache* factoryCache;
```

### <a name="remarks"></a>Комментарии

Хранит указатель на кэш фабрики для `CreatorMap` .

## <a name="creatormapfactorycreator"></a><a name="factorycreator"></a> CreatorMap:: factoryCreator

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
HRESULT (*factoryCreator)(
   unsigned int* currentflags,
   const CreatorMap* entry,
   REFIID iidClassFactory,
IUnknown** factory);
```

### <a name="parameters"></a>Параметры

*куррентфлагс*<br/>
Один из перечислителей [RuntimeClassType](runtimeclasstype-enumeration.md) .

*операции*<br/>
CreatorMap.

*иидклассфактори*<br/>
Идентификатор интерфейса фабрики класса.

*фабрика*<br/>
По завершении операции это адрес фабрики класса.

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

### <a name="remarks"></a>Комментарии

Создает фабрику для указанного CreatorMap.

## <a name="creatormapservername"></a><a name="servername"></a> CreatorMap:: serverName

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
const wchar_t* serverName;
```

### <a name="remarks"></a>Комментарии

Хранит имя сервера для объекта CreatorMap.
