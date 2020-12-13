---
description: 'Дополнительные сведения о: Ккомобжектнолокк Class'
title: Класс Ккомобжектнолокк
ms.date: 11/04/2016
f1_keywords:
- CComObjectNoLock
- ATLCOM/ATL::CComObjectNoLock
- ATLCOM/ATL::CComObjectNoLock::CComObjectNoLock
- ATLCOM/ATL::CComObjectNoLock::AddRef
- ATLCOM/ATL::CComObjectNoLock::QueryInterface
- ATLCOM/ATL::CComObjectNoLock::Release
helpviewer_keywords:
- CComObjectNoLock class
ms.assetid: 288c6506-7da8-4127-8d58-7f4bd779539a
ms.openlocfilehash: 97708250ecd9637c52daf5db82f39d1a12565399
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142497"
---
# <a name="ccomobjectnolock-class"></a>Класс Ккомобжектнолокк

Этот класс реализует `IUnknown` для неагрегированного объекта, но не увеличивает счетчик блокировок модуля в конструкторе.

## <a name="syntax"></a>Синтаксис

```
template<class Base>
class CComObjectNoLock : public Base
```

#### <a name="parameters"></a>Параметры

*Из*<br/>
Класс, производный от [CComObjectRoot](../../atl/reference/ccomobjectroot-class.md) или [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md), а также от любого другого интерфейса, который требуется поддерживать для объекта.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккомобжектнолокк:: Ккомобжектнолокк](#ccomobjectnolock)|Конструктор.|
|[Ккомобжектнолокк:: ~ Ккомобжектнолокк](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомобжектнолокк:: AddRef](#addref)|Увеличивает значение счетчика ссылок на объект.|
|[Ккомобжектнолокк:: QueryInterface](#queryinterface)|Возвращает указатель на запрошенный интерфейс.|
|[Ккомобжектнолокк:: Release](#release)|Уменьшает значение счетчика ссылок на объект.|

## <a name="remarks"></a>Комментарии

`CComObjectNoLock` аналогичен [CComObject](../../atl/reference/ccomobject-class.md) в том, что он реализует [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) для неагрегированного объекта. Однако не `CComObjectNoLock` увеличивает счетчик блокировок модуля в конструкторе.

В библиотеке ATL используются `CComObjectNoLock` внутренние фабрики классов. В общем случае этот класс не будет использоваться напрямую.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`Base`

`CComObjectNoLock`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ccomobjectnolockaddref"></a><a name="addref"></a> Ккомобжектнолокк:: AddRef

Увеличивает значение счетчика ссылок на объект.

```
STDMETHOD_(ULONG, AddRef)();
```

### <a name="return-value"></a>Возвращаемое значение

Значение, которое может быть полезно для диагностики или тестирования.

## <a name="ccomobjectnolockccomobjectnolock"></a><a name="ccomobjectnolock"></a> Ккомобжектнолокк:: Ккомобжектнолокк

Конструктор. В отличие от [CComObject](../../atl/reference/ccomobject-class.md), не увеличивает счетчик блокировок модуля.

```
CComObjectNoLock(void* = NULL);
```

### <a name="parameters"></a>Параметры

<em>void\*</em><br/>
окне Этот неименованный параметр не используется. Он существует для симметрии с другими `CComXXXObjectXXX` конструкторами.

## <a name="ccomobjectnolockccomobjectnolock"></a><a name="dtor"></a> Ккомобжектнолокк:: ~ Ккомобжектнолокк

Деструктор

```
~CComObjectNoLock();
```

### <a name="remarks"></a>Комментарии

Освобождает все выделенные ресурсы и вызывает [финалрелеасе](ccomobjectrootex-class.md#finalrelease).

## <a name="ccomobjectnolockqueryinterface"></a><a name="queryinterface"></a> Ккомобжектнолокк:: QueryInterface

Извлекает указатель на запрошенный интерфейс.

```
STDMETHOD(QueryInterface)(REFIID iid, void** ppvObject);
```

### <a name="parameters"></a>Параметры

*IID*<br/>
окне Идентификатор запрашиваемого интерфейса.

*ппвобжект*<br/>
заполняет Указатель на указатель интерфейса, идентифицируемый по *IID*. Если объект не поддерживает этот интерфейс, *ппвобжект* имеет значение null.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

## <a name="ccomobjectnolockrelease"></a><a name="release"></a> Ккомобжектнолокк:: Release

Уменьшает значение счетчика ссылок на объект.

```
STDMETHOD_(ULONG, Release)();
```

### <a name="return-value"></a>Возвращаемое значение

В отладочных сборках `Release` возвращает значение, которое может быть полезно для диагностики или тестирования. В сборках, не относящихся к отладке, `Release` всегда возвращает 0.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
