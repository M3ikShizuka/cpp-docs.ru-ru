---
description: 'Дополнительные сведения о: Катлбасемодуле Class'
title: Класс Катлбасемодуле
ms.date: 11/04/2016
f1_keywords:
- CAtlBaseModule
- ATLCORE/ATL::CAtlBaseModule
- ATLCORE/ATL::CAtlBaseModule::CAtlBaseModule
- ATLCORE/ATL::CAtlBaseModule::AddResourceInstance
- ATLCORE/ATL::CAtlBaseModule::GetHInstanceAt
- ATLCORE/ATL::CAtlBaseModule::GetModuleInstance
- ATLCORE/ATL::CAtlBaseModule::GetResourceInstance
- ATLCORE/ATL::CAtlBaseModule::RemoveResourceInstance
- ATLCORE/ATL::CAtlBaseModule::SetResourceInstance
- ATLCORE/ATL::CAtlBaseModule::m_bInitFailed
helpviewer_keywords:
- CAtlBaseModule class
ms.assetid: 55ade80c-9b0c-4c51-933e-2158436c1096
ms.openlocfilehash: 249b2ad2d133ba0f407e9c5fabcf716b09605972
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97147541"
---
# <a name="catlbasemodule-class"></a>Класс Катлбасемодуле

Этот класс создается в каждом проекте ATL.

## <a name="syntax"></a>Синтаксис

```cpp
class CAtlBaseModule : public _ATL_BASE_MODULE
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Катлбасемодуле:: Катлбасемодуле](#catlbasemodule)|Конструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Катлбасемодуле:: Аддресаурцеинстанце](#addresourceinstance)|Добавляет экземпляр ресурса в список хранимых дескрипторов.|
|[Катлбасемодуле:: Жесинстанцеат](#gethinstanceat)|Возвращает маркер указанного экземпляра ресурса.|
|[Катлбасемодуле:: Жетмодулеинстанце](#getmoduleinstance)|Возвращает экземпляр модуля из `CAtlBaseModule` объекта.|
|[Катлбасемодуле:: Жетресаурцеинстанце](#getresourceinstance)|Возвращает экземпляр ресурса из `CAtlBaseModule` объекта.|
|[Катлбасемодуле:: Ремовересаурцеинстанце](#removeresourceinstance)|Удаляет экземпляр ресурса из списка хранимых дескрипторов.|
|[Катлбасемодуле:: Сетресаурцеинстанце](#setresourceinstance)|Задает экземпляр ресурса для `CAtlBaseModule` объекта.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Катлбасемодуле:: m_bInitFailed](#m_binitfailed)|Переменная, указывающая, завершилась ли инициализация модуля неудачей.|

## <a name="remarks"></a>Комментарии

Экземпляр `CAtlBaseModule` с именем _AtlBaseModule содержится в каждом проекте ATL, который содержит дескриптор для экземпляра модуля, дескриптор модуля, содержащего ресурсы (которые по умолчанию являются одним и тем же), и массив дескрипторов для модулей, предоставляющих первичные ресурсы. `CAtlBaseModule` можно безопасно получить из нескольких потоков.

Этот класс заменяет устаревший класс [CComModule](../../atl/reference/ccommodule-class.md) , используемый в более ранних версиях ATL.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[_ATL_BASE_MODULE](atl-typedefs.md#_atl_base_module)

`CAtlBaseModule`

## <a name="requirements"></a>Требования

**Заголовок:** атлкоре. h

## <a name="catlbasemoduleaddresourceinstance"></a><a name="addresourceinstance"></a> Катлбасемодуле:: Аддресаурцеинстанце

Добавляет экземпляр ресурса в список хранимых дескрипторов.

```cpp
bool AddResourceInstance(HINSTANCE hInst) throw();
```

### <a name="parameters"></a>Параметры

*хинст*<br/>
Добавляемый экземпляр ресурса.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если ресурс был успешно добавлен; в противном случае — значение false.

## <a name="catlbasemodulecatlbasemodule"></a><a name="catlbasemodule"></a> Катлбасемодуле:: Катлбасемодуле

Конструктор.

```cpp
CAtlBaseModule() throw();
```

### <a name="remarks"></a>Комментарии

Создает объект `CAtlBaseModule`.

## <a name="catlbasemodulegethinstanceat"></a><a name="gethinstanceat"></a> Катлбасемодуле:: Жесинстанцеат

Возвращает маркер указанного экземпляра ресурса.

```cpp
HINSTANCE GetHInstanceAt(int i) throw();
```

### <a name="parameters"></a>Параметры

*i*<br/>
Номер экземпляра ресурса.

### <a name="return-value"></a>Возвращаемое значение

Возвращает обработчик для экземпляра ресурса или значение NULL, если соответствующий экземпляр ресурса не существует.

## <a name="catlbasemodulegetmoduleinstance"></a><a name="getmoduleinstance"></a> Катлбасемодуле:: Жетмодулеинстанце

Возвращает экземпляр модуля из `CAtlBaseModule` объекта.

```cpp
HINSTANCE GetModuleInstance() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает экземпляр модуля.

## <a name="catlbasemodulegetresourceinstance"></a><a name="getresourceinstance"></a> Катлбасемодуле:: Жетресаурцеинстанце

Возвращает экземпляр ресурса.

```cpp
HINSTANCE GetResourceInstance() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает экземпляр ресурса.

## <a name="catlbasemodulem_binitfailed"></a><a name="m_binitfailed"></a> Катлбасемодуле:: m_bInitFailed

Переменная, указывающая, завершилась ли инициализация модуля неудачей.

```cpp
static bool m_bInitFailed;
```

### <a name="remarks"></a>Комментарии

Значение true, если модуль инициализирован, и значение false, если не удалось выполнить инициализацию.

## <a name="catlbasemoduleremoveresourceinstance"></a><a name="removeresourceinstance"></a> Катлбасемодуле:: Ремовересаурцеинстанце

Удаляет экземпляр ресурса из списка хранимых дескрипторов.

```cpp
bool RemoveResourceInstance(HINSTANCE hInst) throw();
```

### <a name="parameters"></a>Параметры

*хинст*<br/>
Удаляемый экземпляр ресурса.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если ресурс был успешно удален; в противном случае — значение false.

## <a name="catlbasemodulesetresourceinstance"></a><a name="setresourceinstance"></a> Катлбасемодуле:: Сетресаурцеинстанце

Задает экземпляр ресурса для `CAtlBaseModule` объекта.

```cpp
HINSTANCE SetResourceInstance(HINSTANCE hInst) throw();
```

### <a name="parameters"></a>Параметры

*хинст*<br/>
Новый экземпляр ресурса.

### <a name="return-value"></a>Возвращаемое значение

Возвращает обновленный экземпляр ресурса.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Классы модулей](../../atl/atl-module-classes.md)
