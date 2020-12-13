---
description: 'Дополнительные сведения о: CComQIPtr Class'
title: Класс CComQIPtr
ms.date: 11/04/2016
f1_keywords:
- CComQIPtr
- ATLCOMCLI/ATL::CComQIPtr
- ATLCOMCLI/ATL::CComQIPtr::CComQIPtr
helpviewer_keywords:
- CComQIPtr class
ms.assetid: 969cacb5-05b6-4af4-b683-24911d70242d
ms.openlocfilehash: e5af938cd7b2bbae3b091eac5323d3455ce1cf02
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142328"
---
# <a name="ccomqiptr-class"></a>Класс CComQIPtr

Класс интеллектуального указателя для управления указателями на интерфейс COM.

## <a name="syntax"></a>Синтаксис

```
template<class T, const IID* piid= &__uuidof(T)>
class CComQIPtr: public CComPtr<T>
```

#### <a name="parameters"></a>Параметры

*T*<br/>
COM-интерфейс, указывающий тип сохраняемого указателя.

*пиид*<br/>
Указатель на идентификатор IID объекта *T*.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CComQIPtr:: CComQIPtr](#ccomqiptr)|Конструктор.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CComQIPtr:: operator =](#operator_eq)|Присваивает указатель на указатель члена.|

## <a name="remarks"></a>Комментарии

ATL использует `CComQIPtr` и [CComPtr](../../atl/reference/ccomptr-class.md) для управления указателями на COM-интерфейс, оба из которых являются производными от [ккомптрбасе](../../atl/reference/ccomptrbase-class.md). Оба класса выполняют автоматический подсчет ссылок с помощью вызовов `AddRef` и `Release` . Перегруженные операторы обрабатывали операции с указателями.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[ккомптрбасе](../../atl/reference/ccomptrbase-class.md)

[CComPtr](../../atl/reference/ccomptr-class.md)

`CComQIPtr`

## <a name="requirements"></a>Требования

**Заголовок:** atlcomcli. h

## <a name="ccomqiptrccomqiptr"></a><a name="ccomqiptr"></a> CComQIPtr:: CComQIPtr

Конструктор.

```
CComQIPtr() throw();
CComQIPtr(T* lp) throw();
CComQIPtr(IUnknown* lp) throw();
CComQIPtr(const CComQIPtr<T, piid>& lp) throw();
```

### <a name="parameters"></a>Параметры

*LP*<br/>
Используется для инициализации указателя интерфейса.

*T*<br/>
COM-интерфейс.

*пиид*<br/>
Указатель на идентификатор IID объекта *T*.

## <a name="ccomqiptroperator-"></a><a name="operator_eq"></a> CComQIPtr:: operator =

Оператор присваивания.

```
T* operator= (T* lp) throw();
T* operator= (const CComQIPtr<T, piid>& lp) throw();
T* operator= (IUnknown* lp) throw();
```

### <a name="parameters"></a>Параметры

*LP*<br/>
Используется для инициализации указателя интерфейса.

*T*<br/>
COM-интерфейс.

*пиид*<br/>
Указатель на идентификатор IID объекта *T*.

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на обновленный `CComQIPtr` объект.

## <a name="see-also"></a>См. также раздел

[CComPtr:: CComPtr](../../atl/reference/ccomptr-class.md#ccomptr)<br/>
[CComQIPtr:: CComQIPtr](#ccomqiptr)<br/>
[Класс Ккомптрбасе](../../atl/reference/ccomptrbase-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Класс Ккомкиптрелементтраитс](../../atl/reference/ccomqiptrelementtraits-class.md)
