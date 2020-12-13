---
description: 'Дополнительные сведения о: CComPolyObject Class'
title: Класс CComPolyObject
ms.date: 11/04/2016
f1_keywords:
- CComPolyObject
- ATLCOM/ATL::CComPolyObject
- ATLCOM/ATL::CComPolyObject::CComPolyObject
- ATLCOM/ATL::CComPolyObject::AddRef
- ATLCOM/ATL::CComPolyObject::CreateInstance
- ATLCOM/ATL::CComPolyObject::FinalConstruct
- ATLCOM/ATL::CComPolyObject::FinalRelease
- ATLCOM/ATL::CComPolyObject::QueryInterface
- ATLCOM/ATL::CComPolyObject::Release
- ATLCOM/ATL::CComPolyObject::m_contained
helpviewer_keywords:
- aggregate objects [C++], in ATL
- aggregation [C++], ATL objects
- CComPolyObject class
ms.assetid: eaf67c18-e855-48ca-9b15-f1df3106121b
ms.openlocfilehash: 1584fd03882b0eb0618bd20b54134317efd17ba8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142406"
---
# <a name="ccompolyobject-class"></a>Класс CComPolyObject

Этот класс реализует `IUnknown` для агрегированного или неагрегированного объекта.

## <a name="syntax"></a>Синтаксис

```
template<class contained>
class CComPolyObject : public IUnknown,
      public CComObjectRootEx<contained::_ThreadModel::ThreadModelNoCS>
```

#### <a name="parameters"></a>Параметры

*нем*<br/>
Класс, производный от [CComObjectRoot](../../atl/reference/ccomobjectroot-class.md) или [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md), а также от любых других интерфейсов, которые требуется поддерживать для объекта.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CComPolyObject:: CComPolyObject](#ccompolyobject)|Конструктор.|
|[CComPolyObject:: ~ CComPolyObject](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CComPolyObject:: AddRef](#addref)|Увеличивает значение счетчика ссылок объекта.|
|[CComPolyObject:: CreateInstance](#createinstance)|Статически Позволяет создать новый объект **<CComPolyObject** `contained` **>** без дополнительной нагрузки на [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).|
|[CComPolyObject:: Финалконструкт](#finalconstruct)|Выполняет окончательную инициализацию `m_contained` .|
|[CComPolyObject:: Финалрелеасе](#finalrelease)|Выполняет окончательное уничтожение `m_contained` .|
|[CComPolyObject:: QueryInterface](#queryinterface)|Извлекает указатель на запрошенный интерфейс.|
|[CComPolyObject:: Release](#release)|Уменьшает значение счетчика ссылок объекта.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[CComPolyObject:: m_contained](#m_contained)|Делегирует `IUnknown` вызовы внешнему неизвестному объекту, если объект является агрегатным, или с `IUnknown` объектом, если объект не является агрегированным.|

## <a name="remarks"></a>Комментарии

`CComPolyObject` реализует [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) для агрегированного или неагрегированного объекта.

При `CComPolyObject` создании экземпляра проверяется значение внешней неизвестной. Если он равен NULL, `IUnknown` реализуется для неагрегированного объекта. Если внешнее неизвестное значение не равно NULL, `IUnknown` реализуется для агрегированного объекта.

Преимущество использования `CComPolyObject` заключается в том, что не следует одновременно использовать [CComAggObject](../../atl/reference/ccomaggobject-class.md) и [CComObject](../../atl/reference/ccomobject-class.md) в модуле для обработки агрегированных и неагрегированных вариантов. В `CComPolyObject` обоих случаях обрабатывается один объект. Это означает, что в модуле существует только одна копия таблицы vtable и одна копия функций. Если таблица vtable велика, это может значительно снизить размер модуля. Однако если таблица vtable невелика, использование `CComPolyObject` может привести к тому, что размер модуля будет немного больше, поскольку он не оптимизирован для агрегированного или неагрегированного объекта, как `CComAggObject` и `CComObject` .

Если макрос DECLARE_POLY_AGGREGATABLE указан в определении класса объекта, `CComPolyObject` будет использоваться для создания объекта. DECLARE_POLY_AGGREGATABLE будут автоматически объявлены при использовании мастера проектов ATL для создания элемента управления "полный доступ" или "Internet Explorer".

При статистическом вычислении `CComPolyObject` объект имеет собственный `IUnknown` , отдельный от внешнего объекта `IUnknown` и сохраняет свой собственный счетчик ссылок. `CComPolyObject` использует [ккомконтаинедобжект](../../atl/reference/ccomcontainedobject-class.md) для делегирования внешней неизвестной.

Дополнительные сведения о статистической обработке см. в статье [основы COM-объектов ATL](../../atl/fundamentals-of-atl-com-objects.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CComObjectRootBase`

[CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)

`IUnknown`

`CComPolyObject`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ccompolyobjectaddref"></a><a name="addref"></a> CComPolyObject:: AddRef

Увеличивает значение счетчика ссылок на объект.

```
STDMETHOD_(ULONG, AddRef)();
```

### <a name="return-value"></a>Возвращаемое значение

Значение, которое может быть полезно для диагностики или тестирования.

## <a name="ccompolyobjectccompolyobject"></a><a name="ccompolyobject"></a> CComPolyObject:: CComPolyObject

Конструктор.

```
CComPolyObject(void* pv);
```

### <a name="parameters"></a>Параметры

*PV*<br/>
окне Указатель на внешнюю неизвестную функцию, если объект должен быть агрегирован, или значение NULL, если объект не является агрегированным.

### <a name="remarks"></a>Комментарии

Инициализирует `CComContainedObject`[элемент данных](#m_contained),m_containedиувеличиваетсчетчикблокировок модуля.

Деструктор уменьшает счетчик блокировок модуля.

## <a name="ccompolyobjectccompolyobject"></a><a name="dtor"></a> CComPolyObject:: ~ CComPolyObject

Деструктор

```
~CComPolyObject();
```

### <a name="remarks"></a>Комментарии

Освобождает все выделенные ресурсы, вызывает [финалрелеасе](#finalrelease)и уменьшает число блокировок модуля.

## <a name="ccompolyobjectcreateinstance"></a><a name="createinstance"></a> CComPolyObject:: CreateInstance

Позволяет создать новый объект **<CComPolyObject** `contained` **>** без дополнительной нагрузки на [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

```
static HRESULT WINAPI CreateInstance(
    LPUNKNOWN pUnkOuter,
    CComPolyObject<contained>** pp);
```

### <a name="parameters"></a>Параметры

*PP*<br/>
заполняет Указатель на указатель **<CComPolyObject** `contained` **>** . Если `CreateInstance` операция завершилась неудачно, *PP* имеет значение null.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

### <a name="remarks"></a>Комментарии

Возвращаемый объект имеет нулевое значение счетчика ссылок, поэтому вызовите `AddRef` его немедленно, а затем используйте `Release` для освобождения ссылки на указатель объекта по завершении.

Если прямой доступ к объекту не требуется, но по-прежнему требуется создать новый объект без дополнительной нагрузки `CoCreateInstance` , используйте [CComCoClass:: CreateInstance](../../atl/reference/ccomcoclass-class.md#createinstance) .

## <a name="ccompolyobjectfinalconstruct"></a><a name="finalconstruct"></a> CComPolyObject:: Финалконструкт

Метод, вызываемый на последних стадиях создания объекта, выполняет конечную инициализацию элемента данных [m_contained](#m_contained) .

```
HRESULT FinalConstruct();
```

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

## <a name="ccompolyobjectfinalrelease"></a><a name="finalrelease"></a> CComPolyObject:: Финалрелеасе

Этот метод вызывается при уничтожении объекта, освобождая элемент данных [m_contained](#m_contained) .

```cpp
void FinalRelease();
```

## <a name="ccompolyobjectm_contained"></a><a name="m_contained"></a> CComPolyObject:: m_contained

Объект [ккомконтаинедобжект](../../atl/reference/ccomcontainedobject-class.md) , производный от класса.

```
CComContainedObject<contained> m_contained;
```

### <a name="parameters"></a>Параметры

*нем*<br/>
окне Класс, производный от [CComObjectRoot](../../atl/reference/ccomobjectroot-class.md) или [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md), а также от любых других интерфейсов, которые требуется поддерживать для объекта.

### <a name="remarks"></a>Комментарии

`IUnknown` вызовы через `m_contained` вызываются внешней неизвестностью, если объект является агрегатным, или с `IUnknown` объектом этого объекта, если объект не является агрегированным.

## <a name="ccompolyobjectqueryinterface"></a><a name="queryinterface"></a> CComPolyObject:: QueryInterface

Извлекает указатель на запрошенный интерфейс.

```
STDMETHOD(QueryInterface)(REFIID iid, void** ppvObject);
template <class Q>
HRESULT QueryInterface(Q** pp);
```

### <a name="parameters"></a>Параметры

*Q*<br/>
COM-интерфейс.

*IID*<br/>
окне Идентификатор запрашиваемого интерфейса.

*ппвобжект*<br/>
заполняет Указатель на указатель интерфейса, идентифицируемый по *IID*. Если объект не поддерживает этот интерфейс, *ппвобжект* имеет значение null.

*PP*<br/>
заполняет Указатель на интерфейс, заданный параметром `__uuidof(Q)` .

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

### <a name="remarks"></a>Комментарии

Для агрегированного объекта, если запрошенный интерфейс имеет значение `IUnknown` , функция `QueryInterface` возвращает указатель на агрегатный объект `IUnknown` и увеличивает счетчик ссылок. В противном случае этот метод запрашивает интерфейс через `CComContainedObject` элемент данных, [m_contained](#m_contained).

## <a name="ccompolyobjectrelease"></a><a name="release"></a> CComPolyObject:: Release

Уменьшает значение счетчика ссылок на объект.

```
STDMETHOD_(ULONG, Release)();
```

### <a name="return-value"></a>Возвращаемое значение

В отладочных сборках `Release` возвращает значение, которое может быть полезно для диагностики или тестирования. В неотладочных сборках `Release` всегда возвращает 0.

## <a name="see-also"></a>См. также раздел

[Класс CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)<br/>
[DECLARE_POLY_AGGREGATABLE](aggregation-and-class-factory-macros.md#declare_poly_aggregatable)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
