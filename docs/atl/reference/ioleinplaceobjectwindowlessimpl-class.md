---
description: 'Дополнительные сведения о: Иолеинплацеобжектвиндовлессимпл Class'
title: Класс Иолеинплацеобжектвиндовлессимпл
ms.date: 11/04/2016
f1_keywords:
- IOleInPlaceObjectWindowlessImpl
- ATLCTL/ATL::IOleInPlaceObjectWindowlessImpl
- ATLCTL/ATL::IOleInPlaceObjectWindowlessImpl::ContextSensitiveHelp
- ATLCTL/ATL::IOleInPlaceObjectWindowlessImpl::GetDropTarget
- ATLCTL/ATL::IOleInPlaceObjectWindowlessImpl::GetWindow
- ATLCTL/ATL::IOleInPlaceObjectWindowlessImpl::InPlaceDeactivate
- ATLCTL/ATL::IOleInPlaceObjectWindowlessImpl::OnWindowMessage
- ATLCTL/ATL::IOleInPlaceObjectWindowlessImpl::ReactivateAndUndo
- ATLCTL/ATL::IOleInPlaceObjectWindowlessImpl::SetObjectRects
- ATLCTL/ATL::IOleInPlaceObjectWindowlessImpl::UIDeactivate
helpviewer_keywords:
- IOleInPlaceObjectWindowless, ATL implementation
- activation [C++], ATL
- IOleInPlaceObjectWindowlessImpl class
- ActiveX controls [C++], communication between container and control
- controls [ATL], windowless
- deactivating ATL
ms.assetid: a2e0feb4-bc59-4adf-aab2-105457bbdbb4
ms.openlocfilehash: 927a973565949bbfc6331e4b4e62d7cb270c2107
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139390"
---
# <a name="ioleinplaceobjectwindowlessimpl-class"></a>Класс Иолеинплацеобжектвиндовлессимпл

Этот класс реализует `IUnknown` и предоставляет методы, позволяющие безоконному управлению принимать сообщения окон и принимать участие в операциях перетаскивания.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class T>
class IOleInPlaceObjectWindowlessImpl
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IOleInPlaceObjectWindowlessImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Иолеинплацеобжектвиндовлессимпл:: Контекстсенситивехелп](#contextsensitivehelp)|Включает контекстную справку. Реализация ATL возвращает E_NOTIMPL.|
|[Иолеинплацеобжектвиндовлессимпл:: Жетдроптаржет](#getdroptarget)|Предоставляет `IDropTarget` интерфейс для активного, безоконного объекта, поддерживающего перетаскивание. Реализация ATL возвращает E_NOTIMPL.|
|[Иолеинплацеобжектвиндовлессимпл::/Window](#getwindow)|Получает дескриптор окна.|
|[Иолеинплацеобжектвиндовлессимпл:: Инплацедеактивате](#inplacedeactivate)|Деактивирует активный элемент управления на месте.|
|[Иолеинплацеобжектвиндовлессимпл:: Онвиндовмессаже](#onwindowmessage)|Отправляет сообщение из контейнера в безоконный элемент управления, который находится в активном состоянии.|
|[Иолеинплацеобжектвиндовлессимпл:: Реактиватеандундо](#reactivateandundo)|Повторно активирует ранее деактивированный элемент управления. Реализация ATL возвращает E_NOTIMPL.|
|[Иолеинплацеобжектвиндовлессимпл:: Сетобжектректс](#setobjectrects)|Указывает, какая часть элемента управления является видимой.|
|[Иолеинплацеобжектвиндовлессимпл:: Уидеактивате](#uideactivate)|Деактивирует и удаляет пользовательский интерфейс, поддерживающий активацию на месте.|

## <a name="remarks"></a>Комментарии

Интерфейс [иолеинплацеобжект](/windows/win32/api/oleidl/nn-oleidl-ioleinplaceobject) управляет повторной активацией и деактивацией элементов управления на месте и определяет, какая часть элемента управления должна быть видима. Интерфейс [иолеинплацеобжектвиндовлесс](/windows/win32/api/ocidl/nn-ocidl-ioleinplaceobjectwindowless) позволяет безоконному управлению принимать сообщения окон и участвовать в операциях перетаскивания. Класс `IOleInPlaceObjectWindowlessImpl` предоставляет реализацию по умолчанию `IOleInPlaceObject` и `IOleInPlaceObjectWindowless` реализует `IUnknown` , отправляя сведения в устройство дампа в отладочных сборках.

Руководство по **сопутствующим статьям** [ATL](../../atl/active-template-library-atl-tutorial.md), [Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IOleInPlaceObjectWindowless`

`IOleInPlaceObjectWindowlessImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлктл. h

## <a name="ioleinplaceobjectwindowlessimplcontextsensitivehelp"></a><a name="contextsensitivehelp"></a> Иолеинплацеобжектвиндовлессимпл:: Контекстсенситивехелп

Возвращает E_NOTIMPL.

```
HRESULT ContextSensitiveHelp(BOOL fEnterMode);
```

### <a name="remarks"></a>Комментарии

См. раздел [иолевиндов:: контекстсенситивехелп](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp) в Windows SDK.

## <a name="ioleinplaceobjectwindowlessimplgetdroptarget"></a><a name="getdroptarget"></a> Иолеинплацеобжектвиндовлессимпл:: Жетдроптаржет

Возвращает E_NOTIMPL.

```
HRESULT GetDropTarget(IDropTarget** ppDropTarget);
```

### <a name="remarks"></a>Комментарии

См. раздел [иолеинплацеобжектвиндовлесс:: жетдроптаржет](/windows/win32/api/ocidl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) в Windows SDK.

## <a name="ioleinplaceobjectwindowlessimplgetwindow"></a><a name="getwindow"></a> Иолеинплацеобжектвиндовлессимпл::/Window

Контейнер вызывает эту функцию для получения маркера окна элемента управления.

```
HRESULT GetWindow(HWND* phwnd);
```

### <a name="remarks"></a>Комментарии

Некоторые контейнеры не будут работать с элементом управления, не имеющим окон, даже если он в настоящий момент находится в окне. В реализации ATL, если элемент данных класса элемента управления `m_bWasOnceWindowless` имеет значение true, функция возвращает E_FAIL. В противном случае, если *ФВНД* не равен null, `GetWindow` устанавливает \* *ФВНД* в элемент данных класса элемента управления `m_hWnd` и возвращает S_OK.

См. раздел [иолевиндов:: onwindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) в Windows SDK.

## <a name="ioleinplaceobjectwindowlessimplinplacedeactivate"></a><a name="inplacedeactivate"></a> Иолеинплацеобжектвиндовлессимпл:: Инплацедеактивате

Вызывается контейнером для деактивации активного элемента управления на месте.

```
HRESULT InPlaceDeactivate(HWND* phwnd);
```

### <a name="remarks"></a>Комментарии

Этот метод выполняет полную или частичную деактивацию в зависимости от состояния элемента управления. При необходимости пользовательский интерфейс элемента управления деактивируется, и окно элемента управления, если таковое имеется, уничтожается. Контейнер уведомляется о том, что элемент управления больше не активен. `IOleInPlaceUIWindow`Интерфейс, используемый контейнером для согласования меню и пространства границ, освобождается.

См. раздел [иолеинплацеобжект:: инплацедеактивате](/windows/win32/api/oleidl/nf-oleidl-ioleinplaceobject-inplacedeactivate) в Windows SDK.

## <a name="ioleinplaceobjectwindowlessimplonwindowmessage"></a><a name="onwindowmessage"></a> Иолеинплацеобжектвиндовлессимпл:: Онвиндовмессаже

Отправляет сообщение из контейнера в безоконный элемент управления, который находится в активном состоянии.

```
HRESULT OnWindowMessage(
    UINT msg,
    WPARAM WParam,
    LPARAM LParam,
    LRESULT plResultParam);
```

### <a name="remarks"></a>Комментарии

См. раздел [иолеинплацеобжектвиндовлесс:: онвиндовмессаже](/windows/win32/api/ocidl/nf-ocidl-ioleinplaceobjectwindowless-onwindowmessage) в Windows SDK.

## <a name="ioleinplaceobjectwindowlessimplreactivateandundo"></a><a name="reactivateandundo"></a> Иолеинплацеобжектвиндовлессимпл:: Реактиватеандундо

Возвращает E_NOTIMPL.

```
HRESULT ReactivateAndUndo();
```

### <a name="remarks"></a>Комментарии

См. раздел [иолеинплацеобжект:: реактиватеандундо](/windows/win32/api/oleidl/nf-oleidl-ioleinplaceobject-reactivateandundo) в Windows SDK.

## <a name="ioleinplaceobjectwindowlessimplsetobjectrects"></a><a name="setobjectrects"></a> Иолеинплацеобжектвиндовлессимпл:: Сетобжектректс

Вызывается контейнером для информирования элемента управления о том, что его размер и (или) расположение изменились.

```
HRESULT SetObjectRects(LPCRECT prcPos, LPCRECT prcClip);
```

### <a name="remarks"></a>Комментарии

Обновляет элемент данных элемента управления `m_rcPos` и отображение элемента управления. Отображается только часть элемента управления, пересекающего область отсечения. Если отображение элемента управления было ранее обрезано, но обрезка была удалена, эту функцию можно вызвать для перерисовки полного представления элемента управления.

См. раздел [иолеинплацеобжект:: сетобжектректс](/windows/win32/api/oleidl/nf-oleidl-ioleinplaceobject-setobjectrects) в Windows SDK.

## <a name="ioleinplaceobjectwindowlessimpluideactivate"></a><a name="uideactivate"></a> Иолеинплацеобжектвиндовлессимпл:: Уидеактивате

Деактивирует и удаляет пользовательский интерфейс элемента управления, поддерживающий активацию на месте.

```
HRESULT UIDeactivate();
```

### <a name="remarks"></a>Комментарии

Задает для элемента данных класса элемента управления `m_bUIActive` значение false. Реализация этой функции в библиотеке ATL всегда возвращает S_OK.

См. раздел [иолеинплацеобжект:: уидеактивате](/windows/win32/api/oleidl/nf-oleidl-ioleinplaceobject-uideactivate) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Класс Ккомконтрол](../../atl/reference/ccomcontrol-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
