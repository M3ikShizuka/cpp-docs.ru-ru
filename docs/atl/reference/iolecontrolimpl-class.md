---
description: 'Дополнительные сведения о: Иолеконтролимпл Class'
title: Класс Иолеконтролимпл
ms.date: 11/04/2016
f1_keywords:
- IOleControlImpl
- ATLCTL/ATL::IOleControlImpl
- ATLCTL/ATL::IOleControlImpl::FreezeEvents
- ATLCTL/ATL::IOleControlImpl::GetControlInfo
- ATLCTL/ATL::IOleControlImpl::OnAmbientPropertyChange
- ATLCTL/ATL::IOleControlImpl::OnMnemonic
helpviewer_keywords:
- IOleControlImpl class
ms.assetid: 5a4255ad-ede4-49ca-ba9a-07c2e919fa85
ms.openlocfilehash: e224f6f8db79c05cb8a774cd57517ba06108e592
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139429"
---
# <a name="iolecontrolimpl-class"></a>Класс Иолеконтролимпл

Этот класс предоставляет реализацию интерфейса по умолчанию `IOleControl` и реализует `IUnknown` .

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class T>
class IOleControlImpl
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IOleControlImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Иолеконтролимпл:: FreezeEvents](#freezeevents)|Указывает, будет ли контейнер игнорировать или принимать события от элемента управления.|
|[Иолеконтролимпл:: Жетконтролинфо](#getcontrolinfo)|Заполняет сведения о поведении клавиатуры элемента управления. Реализация ATL возвращает E_NOTIMPL.|
|[Иолеконтролимпл:: Онамбиентпропертичанже](#onambientpropertychange)|Информирует элемент управления, что изменилось одно или несколько внешних свойств контейнера. Реализация ATL возвращает S_OK.|
|[Иолеконтролимпл:: OnMnemonic](#onmnemonic)|Информирует элемент управления о нажатии пользователем указанного нажатия клавиши. Реализация ATL возвращает E_NOTIMPL.|

## <a name="remarks"></a>Комментарии

Класс `IOleControlImpl` предоставляет реализацию интерфейса [метод интерфейса IOleControl](/windows/win32/api/ocidl/nn-ocidl-iolecontrol) по умолчанию и реализует `IUnknown` , отправляя сведения в устройство дампа в отладочных сборках.

Руководство по **сопутствующим статьям** [ATL](../../atl/active-template-library-atl-tutorial.md), [Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IOleControl`

`IOleControlImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлктл. h

## <a name="iolecontrolimplfreezeevents"></a><a name="freezeevents"></a> Иолеконтролимпл:: FreezeEvents

В реализации ATL `FreezeEvents` увеличивает элемент данных класса элемента управления, `m_nFreezeEvents` Если `bFreeze` имеет значение true, и уменьшает, `m_nFreezeEvents` Если имеет значение `bFreeze` false.

```
HRESULT FreezeEvents(BOOL bFreeze);
```

### <a name="remarks"></a>Комментарии

`FreezeEvents` затем возвращает S_OK.

См. раздел [метод интерфейса IOleControl:: FreezeEvents](/windows/win32/api/ocidl/nf-ocidl-iolecontrol-freezeevents) в Windows SDK.

## <a name="iolecontrolimplgetcontrolinfo"></a><a name="getcontrolinfo"></a> Иолеконтролимпл:: Жетконтролинфо

Заполняет сведения о поведении клавиатуры элемента управления.

```
HRESULT GetControlInfo(LPCONTROLINFO pCI);
```

### <a name="remarks"></a>Комментарии

См. раздел [метод интерфейса IOleControl: жетконтролинфо](/windows/win32/api/ocidl/nf-ocidl-iolecontrol-getcontrolinfo) в Windows SDK.

### <a name="return-value"></a>Возвращаемое значение

Возвращает E_NOTIMPL.

## <a name="iolecontrolimplonambientpropertychange"></a><a name="onambientpropertychange"></a> Иолеконтролимпл:: Онамбиентпропертичанже

Информирует элемент управления, что изменилось одно или несколько внешних свойств контейнера.

```
HRESULT OnAmbientPropertyChange(DISPID dispid);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK.

### <a name="remarks"></a>Комментарии

См. раздел [метод интерфейса IOleControl:: онамбиентпропертичанже](/windows/win32/api/ocidl/nf-ocidl-iolecontrol-onambientpropertychange) в Windows SDK.

## <a name="iolecontrolimplonmnemonic"></a><a name="onmnemonic"></a> Иолеконтролимпл:: OnMnemonic

Информирует элемент управления о нажатии пользователем указанного нажатия клавиши.

```
HRESULT OnMnemonic(LPMSG pMsg);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает E_NOTIMPL.

### <a name="remarks"></a>Комментарии

См. раздел [метод интерфейса IOleControl:: OnMnemonic](/windows/win32/api/ocidl/nf-ocidl-iolecontrol-onmnemonic) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Класс Иолеобжектимпл](../../atl/reference/ioleobjectimpl-class.md)<br/>
[Интерфейсы элементов управления ActiveX](/windows/win32/com/activex-controls-interfaces)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
