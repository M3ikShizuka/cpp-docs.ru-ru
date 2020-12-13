---
description: 'Дополнительные сведения о: Кфирепропнотифевент Class'
title: Класс Кфирепропнотифевент
ms.date: 11/04/2016
f1_keywords:
- CFirePropNotifyEvent
- ATLCTL/ATL::CFirePropNotifyEvent
- ATLCTL/ATL::CFirePropNotifyEvent::FireOnChanged
- ATLCTL/ATL::CFirePropNotifyEvent::FireOnRequestEdit
helpviewer_keywords:
- sinks, notifying of ATL events
- CFirePropNotifyEvent class
- connection points [C++], notifying of events
ms.assetid: eb7a563e-6bce-4cdf-8d20-8c6a5307781b
ms.openlocfilehash: 09102e67408195751e083807f444c1b028fd2762
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141730"
---
# <a name="cfirepropnotifyevent-class"></a>Класс Кфирепропнотифевент

Этот класс предоставляет методы для уведомления приемника контейнера об изменениях свойств элемента управления.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class CFirePropNotifyEvent
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кфирепропнотифевент:: Фиреончанжед](#fireonchanged)|Статически Сообщает приемнику контейнера, что свойство элемента управления изменилось.|
|[Кфирепропнотифевент:: Фиреонрекуестедит](#fireonrequestedit)|Статически Уведомляет приемник контейнера, что свойство элемента управления собирается измениться.|

## <a name="remarks"></a>Комментарии

`CFirePropNotifyEvent` содержит два метода, уведомляющих приемник контейнера о том, что свойство элемента управления изменилось или будет изменено.

Если класс, реализующий элемент управления, является производным от `IPropertyNotifySink` , `CFirePropNotifyEvent` методы вызываются при вызове метода `FireOnRequestEdit` или `FireOnChanged` . Если класс элемента управления не является производным от `IPropertyNotifySink` , вызовы этих функций возвращают S_OK.

Дополнительные сведения о создании элементов управления см. в [учебнике по ATL](../../atl/active-template-library-atl-tutorial.md).

## <a name="requirements"></a>Требования

**Заголовок:** атлктл. h

## <a name="cfirepropnotifyeventfireonchanged"></a><a name="fireonchanged"></a> Кфирепропнотифевент:: Фиреончанжед

Уведомляет все подключенные интерфейсы [ипропертинотифисинк](/windows/win32/api/ocidl/nn-ocidl-ipropertynotifysink) (в каждой точке соединения объекта) об изменении указанного свойства объекта.

```
static HRESULT FireOnChanged(IUnknown* pUnk, DISPID dispID);
```

### <a name="parameters"></a>Параметры

*pUnk*<br/>
окне Указатель на `IUnknown` объект объекта, отправляющего уведомление.

*dispID*<br/>
окне Идентификатор измененного свойства.

### <a name="return-value"></a>Возвращаемое значение

Одно из стандартных значений HRESULT.

### <a name="remarks"></a>Комментарии

Эту функцию можно вызывать, даже если элемент управления не поддерживает точки подключения.

## <a name="cfirepropnotifyeventfireonrequestedit"></a><a name="fireonrequestedit"></a> Кфирепропнотифевент:: Фиреонрекуестедит

Уведомляет все подключенные интерфейсы [ипропертинотифисинк](/windows/win32/api/ocidl/nn-ocidl-ipropertynotifysink) (в каждой точке соединения объекта) о том, что необходимо изменить указанное свойство объекта.

```
static HRESULT FireOnRequestEdit(IUnknown* pUnk, DISPID dispID);
```

### <a name="parameters"></a>Параметры

*pUnk*<br/>
окне Указатель на `IUnknown` объект объекта, отправляющего уведомление.

*dispID*<br/>
окне Идентификатор свойства, которое необходимо изменить.

### <a name="return-value"></a>Возвращаемое значение

Одно из стандартных значений HRESULT.

### <a name="remarks"></a>Комментарии

Эту функцию можно вызывать, даже если элемент управления не поддерживает точки подключения.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
