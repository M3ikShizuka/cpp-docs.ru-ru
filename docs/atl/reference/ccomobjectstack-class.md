---
description: 'Дополнительные сведения о: Ккомобжектстакк Class'
title: Класс Ккомобжектстакк
ms.date: 11/04/2016
f1_keywords:
- CComObjectStack
- ATLCOM/ATL::CComObjectStack
- ATLCOM/ATL::CComObjectStack::CComObjectStack
- ATLCOM/ATL::CComObjectStack::AddRef
- ATLCOM/ATL::CComObjectStack::QueryInterface
- ATLCOM/ATL::CComObjectStack::Release
- ATLCOM/ATL::CComObjectStack::m_hResFinalConstruct
helpviewer_keywords:
- CComObjectStack class
ms.assetid: 3da72c40-c834-45f6-bb76-6ac204028d80
ms.openlocfilehash: 5713601a765ad9ff1c32992d1f9c517dd86affca
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142419"
---
# <a name="ccomobjectstack-class"></a>Класс Ккомобжектстакк

Этот класс создает временный COM-объект и предоставляет его с реализацией скелетообразных `IUnknown` .

## <a name="syntax"></a>Синтаксис

```
template <class  Base>
class CComObjectStack : public Base
```

#### <a name="parameters"></a>Параметры

*Из*<br/>
Класс, производный от [CComObjectRoot](../../atl/reference/ccomobjectroot-class.md) или [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md), а также от любого другого интерфейса, который требуется поддерживать для объекта.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккомобжектстакк:: Ккомобжектстакк](#ccomobjectstack)|Конструктор.|
|[Ккомобжектстакк:: ~ Ккомобжектстакк](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомобжектстакк:: AddRef](#addref)|Возвращает ноль. В режиме отладки вызывает `_ASSERTE` .|
|[Ккомобжектстакк:: QueryInterface](#queryinterface)|Возвращает E_NOINTERFACE. В режиме отладки вызывает `_ASSERTE` .|
|[Ккомобжектстакк:: Release](#release)|Возвращает ноль. В режиме отладки вызывает `_ASSERTE` . ~|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Ккомобжектстакк:: m_hResFinalConstruct](#m_hresfinalconstruct)|Содержит значение HRESULT, возвращаемое во время создания `CComObjectStack` объекта.|

## <a name="remarks"></a>Комментарии

`CComObjectStack` используется для создания временного COM-объекта и предоставления объекта реализации скелетообразных `IUnknown` . Как правило, объект используется в качестве локальной переменной в одной функции (т. е. помещается в стек). Поскольку объект уничтожается после завершения функции, подсчет ссылок не выполняется для повышения эффективности.

В следующем примере показано, как создать COM-объект, используемый внутри функции:

[!code-cpp[NVC_ATL_COM#42](../../atl/codesnippet/cpp/ccomobjectstack-class_1.cpp)]

Временный объект `Tempobj` помещается в стек и автоматически исчезает после завершения функции.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`Base`

`CComObjectStack`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ccomobjectstackaddref"></a><a name="addref"></a> Ккомобжектстакк:: AddRef

Возвращает ноль.

```
STDMETHOD_(ULONG, AddRef)();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает ноль.

### <a name="remarks"></a>Комментарии

В режиме отладки вызывает `_ASSERTE` .

## <a name="ccomobjectstackccomobjectstack"></a><a name="ccomobjectstack"></a> Ккомобжектстакк:: Ккомобжектстакк

Конструктор.

```
CComObjectStack(void* = NULL);
```

### <a name="remarks"></a>Комментарии

Вызывает `FinalConstruct` , а затем устанавливает [m_hResFinalConstruct](#m_hresfinalconstruct) в значение HRESULT, возвращаемое `FinalConstruct` . Если базовый класс не был производным от [CComObjectRoot](../../atl/reference/ccomobjectroot-class.md), необходимо указать собственный `FinalConstruct` метод. Деструктор вызывает `FinalRelease`.

## <a name="ccomobjectstackccomobjectstack"></a><a name="dtor"></a> Ккомобжектстакк:: ~ Ккомобжектстакк

Деструктор

```
CComObjectStack();
```

### <a name="remarks"></a>Комментарии

Освобождает все выделенные ресурсы и вызывает [финалрелеасе](ccomobjectrootex-class.md#finalrelease).

## <a name="ccomobjectstackm_hresfinalconstruct"></a><a name="m_hresfinalconstruct"></a> Ккомобжектстакк:: m_hResFinalConstruct

Содержит значение HRESULT, возвращаемое `FinalConstruct` при вызове во время создания `CComObjectStack` объекта.

```
HRESULT    m_hResFinalConstruct;
```

## <a name="ccomobjectstackqueryinterface"></a><a name="queryinterface"></a> Ккомобжектстакк:: QueryInterface

Возвращает E_NOINTERFACE.

```
HRESULT    QueryInterface(REFIID, void**);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает E_NOINTERFACE.

### <a name="remarks"></a>Комментарии

В режиме отладки вызывает `_ASSERTE` .

## <a name="ccomobjectstackrelease"></a><a name="release"></a> Ккомобжектстакк:: Release

Возвращает ноль.

```
STDMETHOD_(ULONG, Release)();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает ноль.

### <a name="remarks"></a>Комментарии

В режиме отладки вызывает `_ASSERTE` .

## <a name="see-also"></a>См. также раздел

[Класс CComAggObject](../../atl/reference/ccomaggobject-class.md)<br/>
[Класс CComObject](../../atl/reference/ccomobject-class.md)<br/>
[Класс Ккомобжектглобал](../../atl/reference/ccomobjectglobal-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
