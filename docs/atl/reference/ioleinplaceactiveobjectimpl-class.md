---
description: 'Дополнительные сведения о: Иолеинплацеактивеобжектимпл Class'
title: Класс Иолеинплацеактивеобжектимпл
ms.date: 11/04/2016
f1_keywords:
- IOleInPlaceActiveObjectImpl
- ATLCTL/ATL::IOleInPlaceActiveObjectImpl
- ATLCTL/ATL::IOleInPlaceActiveObjectImpl::ContextSensitiveHelp
- ATLCTL/ATL::IOleInPlaceActiveObjectImpl::EnableModeless
- ATLCTL/ATL::IOleInPlaceActiveObjectImpl::GetWindow
- ATLCTL/ATL::IOleInPlaceActiveObjectImpl::OnDocWindowActivate
- ATLCTL/ATL::IOleInPlaceActiveObjectImpl::OnFrameWindowActivate
- ATLCTL/ATL::IOleInPlaceActiveObjectImpl::ResizeBorder
- ATLCTL/ATL::IOleInPlaceActiveObjectImpl::TranslateAccelerator
helpviewer_keywords:
- IOleInPlaceActiveObjectImpl class
- ActiveX controls [C++], communication between container and control
- IOleInPlaceActiveObject, ATL implementation
ms.assetid: 44e6cc6d-a2dc-4187-98e3-73cf0320dea9
ms.openlocfilehash: 02f74e462dca2aac2749b8602281f40c8eacd0eb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158196"
---
# <a name="ioleinplaceactiveobjectimpl-class"></a>Класс Иолеинплацеактивеобжектимпл

Этот класс предоставляет методы для облегчения взаимодействия между элементом управления на месте и его контейнером.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class T>
class IOleInPlaceActiveObjectImpl
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IOleInPlaceActiveObjectImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Иолеинплацеактивеобжектимпл:: Контекстсенситивехелп](#contextsensitivehelp)|Включает контекстную справку. Реализация ATL возвращает E_NOTIMPL.|
|[Иолеинплацеактивеобжектимпл:: Енаблемоделесс](#enablemodeless)|Включение немодальных диалоговых окон. Реализация ATL возвращает S_OK.|
|[Иолеинплацеактивеобжектимпл::/Window](#getwindow)|Получает дескриптор окна.|
|[Иолеинплацеактивеобжектимпл:: OnDocWindowActivate](#ondocwindowactivate)|Уведомляет элемент управления о том, что окно документа контейнера активировано или отключено. Реализация ATL возвращает S_OK.|
|[Иолеинплацеактивеобжектимпл:: OnFrameWindowActivate](#onframewindowactivate)|Уведомляет элемент управления о том, что окно фрейма верхнего уровня контейнера активировано или отключено. Реализация ATL возвращает|
|[Иолеинплацеактивеобжектимпл:: ResizeBorder](#resizeborder)|Информирует элемент управления, что ему нужно изменить размер границ. Реализация ATL возвращает S_OK.|
|[Иолеинплацеактивеобжектимпл:: TranslateAccelerator](#translateaccelerator)|В меню "процессы" — сообщения ключа ускорителя из контейнера. Реализация ATL возвращает E_NOTIMPL.|

## <a name="remarks"></a>Комментарии

Интерфейс [метода IOleInPlaceActiveObject](/windows/win32/api/oleidl/nn-oleidl-ioleinplaceactiveobject) помогает взаимодействовать между элементами управления на месте и его контейнером. Например, связь активного состояния элемента управления и контейнера и уведомление элемента управления о необходимости изменения размера. Класс `IOleInPlaceActiveObjectImpl` предоставляет реализацию по умолчанию `IOleInPlaceActiveObject` и поддерживает `IUnknown` , отправляя сведения на устройство дампа в отладочных сборках.

Руководство по **сопутствующим статьям** [ATL](../../atl/active-template-library-atl-tutorial.md), [Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IOleInPlaceActiveObject`

`IOleInPlaceActiveObjectImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлктл. h

## <a name="ioleinplaceactiveobjectimplcontextsensitivehelp"></a><a name="contextsensitivehelp"></a> Иолеинплацеактивеобжектимпл:: Контекстсенситивехелп

Включает контекстную справку.

```
HRESULT ContextSensitiveHelp(BOOL fEnterMode);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает E_NOTIMPL.

### <a name="remarks"></a>Комментарии

См. раздел [иолевиндов:: контекстсенситивехелп](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp) в Windows SDK.

## <a name="ioleinplaceactiveobjectimplenablemodeless"></a><a name="enablemodeless"></a> Иолеинплацеактивеобжектимпл:: Енаблемоделесс

Включение немодальных диалоговых окон.

```
HRESULT EnableModeless(BOOL fEnable);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK.

### <a name="remarks"></a>Комментарии

См. раздел [метода IOleInPlaceActiveObject:: енаблемоделесс](/windows/win32/api/oleidl/nf-oleidl-ioleinplaceactiveobject-enablemodeless) в Windows SDK.

## <a name="ioleinplaceactiveobjectimplgetwindow"></a><a name="getwindow"></a> Иолеинплацеактивеобжектимпл::/Window

Контейнер вызывает эту функцию для получения маркера окна элемента управления.

```
HRESULT GetWindow(HWND* phwnd);
```

### <a name="remarks"></a>Комментарии

Некоторые контейнеры не будут работать с элементом управления, не имеющим окон, даже если он в настоящий момент находится в окне. В реализации ATL, если `CComControl::m_bWasOnceWindowless` элемент данных имеет значение true, функция возвращает E_FAIL. В противном случае, если \* *ФВНД* не равно null, `GetWindow` присваивает *ФВНД* элементу данных класса элемента управления `m_hWnd` и возвращает S_OK.

См. раздел [иолевиндов:: onwindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) в Windows SDK.

## <a name="ioleinplaceactiveobjectimplondocwindowactivate"></a><a name="ondocwindowactivate"></a> Иолеинплацеактивеобжектимпл:: OnDocWindowActivate

Уведомляет элемент управления о том, что окно документа контейнера активировано или отключено.

```
HRESULT OnDocWindowActivate(BOOL fActivate);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK.

### <a name="remarks"></a>Комментарии

См. раздел [метода IOleInPlaceActiveObject:: OnDocWindowActivate](/windows/win32/api/oleidl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate) в Windows SDK.

## <a name="ioleinplaceactiveobjectimplonframewindowactivate"></a><a name="onframewindowactivate"></a> Иолеинплацеактивеобжектимпл:: OnFrameWindowActivate

Уведомляет элемент управления о том, что окно фрейма верхнего уровня контейнера активировано или отключено.

```
HRESULT OnFrameWindowActivate(BOOL fActivate);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK.

### <a name="remarks"></a>Комментарии

См. раздел [метода IOleInPlaceActiveObject:: OnFrameWindowActivate](/windows/win32/api/oleidl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate) в Windows SDK.

## <a name="ioleinplaceactiveobjectimplresizeborder"></a><a name="resizeborder"></a> Иолеинплацеактивеобжектимпл:: ResizeBorder

Информирует элемент управления, что ему нужно изменить размер границ.

```
HRESULT ResizeBorder(
    LPRECT prcBorder,
    IOleInPlaceUIWindow* pUIWindow,
    BOOL fFrameWindow);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK.

### <a name="remarks"></a>Комментарии

См. раздел [метода IOleInPlaceActiveObject:: ResizeBorder](/windows/win32/api/oleidl/nf-oleidl-ioleinplaceactiveobject-resizeborder) в Windows SDK.

## <a name="ioleinplaceactiveobjectimpltranslateaccelerator"></a><a name="translateaccelerator"></a> Иолеинплацеактивеобжектимпл:: TranslateAccelerator

В меню "процессы" — сообщения ключа ускорителя из контейнера.

```
HRESULT TranslateAccelerator(LPMSG lpmsg);
```

### <a name="return-value"></a>Возвращаемое значение

Этот метод поддерживает следующие возвращаемые значения.

S_OK, если сообщение было успешно переведено.

S_FALSE, если сообщение не было переведено.

### <a name="remarks"></a>Комментарии

См. раздел [метода IOleInPlaceActiveObject:: TranslateAccelerator](/windows/win32/api/oleidl/nf-oleidl-ioleinplaceactiveobject-translateaccelerator) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Класс Ккомконтрол](../../atl/reference/ccomcontrol-class.md)<br/>
[Интерфейсы элементов управления ActiveX](/windows/win32/com/activex-controls-interfaces)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
