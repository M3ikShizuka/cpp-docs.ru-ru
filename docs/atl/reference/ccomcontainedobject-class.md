---
description: 'Дополнительные сведения о: Ккомконтаинедобжект Class'
title: Класс Ккомконтаинедобжект
ms.date: 11/04/2016
f1_keywords:
- CComContainedObject
- ATLCOM/ATL::CComContainedObject
- ATLCOM/ATL::CComContainedObject::CComContainedObject
- ATLCOM/ATL::CComContainedObject::AddRef
- ATLCOM/ATL::CComContainedObject::GetControllingUnknown
- ATLCOM/ATL::CComContainedObject::QueryInterface
- ATLCOM/ATL::CComContainedObject::Release
helpviewer_keywords:
- aggregate objects [C++], in ATL
- aggregation [C++], ATL objects
- CComContainedObject class
ms.assetid: e8616b41-c200-47b8-bf2c-fb9f713ebdad
ms.openlocfilehash: 9c0993d5ce71a557b71939f60a7019d3c062bac3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152208"
---
# <a name="ccomcontainedobject-class"></a>Класс Ккомконтаинедобжект

Этот класс реализует [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) , делегируя его объекту Owner `IUnknown` .

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class Base>
class CComContainedObject : public Base
```

#### <a name="parameters"></a>Параметры

*Из*<br/>
Класс, производный от [CComObjectRoot](../../atl/reference/ccomobjectroot-class.md) или [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md).

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккомконтаинедобжект:: Ккомконтаинедобжект](#ccomcontainedobject)|Конструктор. Инициализирует указатель элемента для объекта владельца `IUnknown` .|
|[Ккомконтаинедобжект:: ~ Ккомконтаинедобжект](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомконтаинедобжект:: AddRef](#addref)|Увеличивает значение счетчика ссылок на объекте Owner.|
|[Ккомконтаинедобжект:: Жетконтроллингункновн](#getcontrollingunknown)|Получает объект владельца `IUnknown` .|
|[Ккомконтаинедобжект:: QueryInterface](#queryinterface)|Извлекает указатель на интерфейс, запрошенный для объекта-владельца.|
|[Ккомконтаинедобжект:: Release](#release)|Уменьшает значение счетчика ссылок на объекте Owner.|

## <a name="remarks"></a>Комментарии

ATL использует `CComContainedObject` в классах [CComAggObject](../../atl/reference/ccomaggobject-class.md), [CComPolyObject](../../atl/reference/ccompolyobject-class.md)и [ккомкачедтеароффобжект](../../atl/reference/ccomcachedtearoffobject-class.md). `CComContainedObject` реализует [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) , делегируя его объекту Owner `IUnknown` . (Владельцем является либо внешний объект агрегата, либо объект, для которого создается интерфейс разрыва.) `CComContainedObject` вызовы `CComObjectRootEx` `OuterQueryInterface` , `OuterAddRef` и `OuterRelease` , все наследуются через `Base` .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`Base`

`CComContainedObject`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ccomcontainedobjectaddref"></a><a name="addref"></a> Ккомконтаинедобжект:: AddRef

Увеличивает значение счетчика ссылок на объекте Owner.

```
STDMETHOD_(ULONG, AddRef)();
```

### <a name="return-value"></a>Возвращаемое значение

Значение, которое может быть полезно для диагностики или тестирования.

## <a name="ccomcontainedobjectccomcontainedobject"></a><a name="ccomcontainedobject"></a> Ккомконтаинедобжект:: Ккомконтаинедобжект

Конструктор.

```
CComContainedObject(void* pv);
```

### <a name="parameters"></a>Параметры

*PV*<br/>
окне Объект Owner `IUnknown` .

### <a name="remarks"></a>Комментарии

Устанавливает `m_pOuterUnknown` для указателя на член (наследуется через `Base` класс) значение *ПС*.

## <a name="ccomcontainedobjectccomcontainedobject"></a><a name="dtor"></a> Ккомконтаинедобжект:: ~ Ккомконтаинедобжект

Деструктор

```
~CComContainedObject();
```

### <a name="remarks"></a>Комментарии

Освобождает все выделенные ресурсы.

## <a name="ccomcontainedobjectgetcontrollingunknown"></a><a name="getcontrollingunknown"></a> Ккомконтаинедобжект:: Жетконтроллингункновн

Возвращает `m_pOuterUnknown` указатель на элемент (наследуется через *базовый* класс), который содержит объект-владелец `IUnknown` .

```
IUnknown* GetControllingUnknown();
```

### <a name="return-value"></a>Возвращаемое значение

Объект Owner `IUnknown` .

### <a name="remarks"></a>Комментарии

Этот метод может быть виртуальным `Base` , если объявлен [DECLARE_GET_CONTROLLING_UNKNOWNный](aggregation-and-class-factory-macros.md#declare_get_controlling_unknown) макрос.

## <a name="ccomcontainedobjectqueryinterface"></a><a name="queryinterface"></a> Ккомконтаинедобжект:: QueryInterface

Извлекает указатель на интерфейс, запрошенный для объекта-владельца.

```
STDMETHOD(QueryInterface)(REFIID iid, void** ppvObject);
template <class Q>
HRESULT STDMETHODCALLTYPE QueryInterface(Q** pp);
```

### <a name="parameters"></a>Параметры

*IID*<br/>
окне Идентификатор запрашиваемого интерфейса.

*ппвобжект*<br/>
заполняет Указатель на указатель интерфейса, идентифицируемый по *IID*. Если объект не поддерживает этот интерфейс, *ппвобжект* имеет значение null.

*PP*<br/>
заполняет Указатель на указатель интерфейса, идентифицируемый по типу `Q` . Если объект не поддерживает этот интерфейс, *PP* имеет значение null.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

## <a name="ccomcontainedobjectrelease"></a><a name="release"></a> Ккомконтаинедобжект:: Release

Уменьшает значение счетчика ссылок на объекте Owner.

```
STDMETHOD_(ULONG, Release)();
```

### <a name="return-value"></a>Возвращаемое значение

В отладочных сборках `Release` возвращает значение, которое может быть полезно для диагностики или тестирования. В сборках, не относящихся к отладке, `Release` всегда возвращает 0.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
