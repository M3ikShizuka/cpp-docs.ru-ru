---
description: 'Дополнительные сведения о: Ккомобжектглобал Class'
title: Класс Ккомобжектглобал
ms.date: 11/04/2016
f1_keywords:
- CComObjectGlobal
- ATLCOM/ATL::CComObjectGlobal
- ATLCOM/ATL::CComObjectGlobal::CComObjectGlobal
- ATLCOM/ATL::CComObjectGlobal::AddRef
- ATLCOM/ATL::CComObjectGlobal::QueryInterface
- ATLCOM/ATL::CComObjectGlobal::Release
- ATLCOM/ATL::CComObjectGlobal::m_hResFinalConstruct
helpviewer_keywords:
- CComObjectGlobal class
ms.assetid: 79bdee55-66e4-4536-b5b3-bdf09f78b9a6
ms.openlocfilehash: 0f79acb0fdbb43f9456e08f26875d45eec9904c2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97151987"
---
# <a name="ccomobjectglobal-class"></a>Класс Ккомобжектглобал

Этот класс управляет счетчиком ссылок для модуля, содержащего ваш `Base` объект.

## <a name="syntax"></a>Синтаксис

```
template<class Base>
class CComObjectGlobal : public Base
```

#### <a name="parameters"></a>Параметры

*Из*<br/>
Класс, производный от [CComObjectRoot](../../atl/reference/ccomobjectroot-class.md) или [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md), а также от любого другого интерфейса, который требуется поддерживать для объекта.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккомобжектглобал:: Ккомобжектглобал](#ccomobjectglobal)|Конструктор.|
|[Ккомобжектглобал:: ~ Ккомобжектглобал](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомобжектглобал:: AddRef](#addref)|Реализует глобальную `AddRef` .|
|[Ккомобжектглобал:: QueryInterface](#queryinterface)|Реализует глобальную `QueryInterface` .|
|[Ккомобжектглобал:: Release](#release)|Реализует глобальную `Release` .|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Ккомобжектглобал:: m_hResFinalConstruct](#m_hresfinalconstruct)|Содержит значение HRESULT, возвращаемое во время создания `CComObjectGlobal` объекта.|

## <a name="remarks"></a>Комментарии

`CComObjectGlobal` управляет счетчиком ссылок на модуль, содержащий `Base` объект. `CComObjectGlobal` гарантирует, что объект не будет удален при условии, что модуль не был освобожден. Объект будет удален только в том случае, если счетчик ссылок во всем модуле становится нулевым.

Например, `CComObjectGlobal` фабрика класса может содержать общий глобальный объект, совместно используемый всеми его клиентами.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`Base`

`CComObjectGlobal`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ccomobjectglobaladdref"></a><a name="addref"></a> Ккомобжектглобал:: AddRef

Увеличивает значение счетчика ссылок объекта на 1.

```
STDMETHOD_(ULONG, AddRef)();
```

### <a name="return-value"></a>Возвращаемое значение

Значение, которое может быть полезно для диагностики и тестирования.

### <a name="remarks"></a>Комментарии

По умолчанию `AddRef` вызывает `_Module::Lock` , где `_Module` — это глобальный экземпляр [CComModule](../../atl/reference/ccommodule-class.md) или производный от него класс.

## <a name="ccomobjectglobalccomobjectglobal"></a><a name="ccomobjectglobal"></a> Ккомобжектглобал:: Ккомобжектглобал

Конструктор. Вызывает, `FinalConstruct` а затем задает [m_hResFinalConstruct](#m_hresfinalconstruct) , `HRESULT` возвращаемое методом `FinalConstruct` .

```
CComObjectGlobal(void* = NULL));
```

### <a name="remarks"></a>Комментарии

Если базовый класс не был производным от [CComObjectRoot](../../atl/reference/ccomobjectroot-class.md), необходимо указать собственный `FinalConstruct` метод. Деструктор вызывает `FinalRelease`.

## <a name="ccomobjectglobalccomobjectglobal"></a><a name="dtor"></a> Ккомобжектглобал:: ~ Ккомобжектглобал

Деструктор

```
CComObjectGlobal();
```

### <a name="remarks"></a>Комментарии

Освобождает все выделенные ресурсы и вызывает [финалрелеасе](ccomobjectrootex-class.md#finalrelease).

## <a name="ccomobjectglobalm_hresfinalconstruct"></a><a name="m_hresfinalconstruct"></a> Ккомобжектглобал:: m_hResFinalConstruct

Содержит значение HRESULT из вызова `FinalConstruct` во время создания `CComObjectGlobal` объекта.

```
HRESULT m_hResFinalConstruct;
```

## <a name="ccomobjectglobalqueryinterface"></a><a name="queryinterface"></a> Ккомобжектглобал:: QueryInterface

Извлекает указатель на запрошенный указатель интерфейса.

```
STDMETHOD(QueryInterface)(REFIID iid, void** ppvObject);
```

### <a name="parameters"></a>Параметры

*IID*<br/>
окне Идентификатор GUID запрашиваемого интерфейса.

*ппвобжект*<br/>
заполняет Указатель на указатель интерфейса, идентифицируемый по IID, или значение NULL, если интерфейс не найден.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

### <a name="remarks"></a>Комментарии

`QueryInterface` обрабатывает интерфейсы только в таблице сопоставлений COM.

## <a name="ccomobjectglobalrelease"></a><a name="release"></a> Ккомобжектглобал:: Release

Уменьшает значение счетчика ссылок объекта на 1.

```
STDMETHOD_(ULONG, Release)();
```

### <a name="return-value"></a>Возвращаемое значение

В отладочных сборках `Release` возвращает значение, которое может быть полезно для диагностики и тестирования. В сборках, не относящихся к отладке, `Release` всегда возвращает 0.

### <a name="remarks"></a>Комментарии

По умолчанию `Release` вызывает `_Module::Unlock` , где `_Module` — это глобальный экземпляр [CComModule](../../atl/reference/ccommodule-class.md) или производный от него класс.

## <a name="see-also"></a>См. также раздел

[Класс Ккомобжектстакк](../../atl/reference/ccomobjectstack-class.md)<br/>
[Класс CComAggObject](../../atl/reference/ccomaggobject-class.md)<br/>
[Класс CComObject](../../atl/reference/ccomobject-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
