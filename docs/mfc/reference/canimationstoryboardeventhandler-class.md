---
description: 'Дополнительные сведения о: Каниматионсторибоардевенсандлер Class'
title: Класс CAnimationStoryboardEventHandler
ms.date: 11/04/2016
f1_keywords:
- CAnimationStoryboardEventHandler
- AFXANIMATIONCONTROLLER/CAnimationStoryboardEventHandler
- AFXANIMATIONCONTROLLER/CAnimationStoryboardEventHandler::CAnimationStoryboardEventHandler
- AFXANIMATIONCONTROLLER/CAnimationStoryboardEventHandler::CreateInstance
- AFXANIMATIONCONTROLLER/CAnimationStoryboardEventHandler::OnStoryboardStatusChanged
- AFXANIMATIONCONTROLLER/CAnimationStoryboardEventHandler::OnStoryboardUpdated
- AFXANIMATIONCONTROLLER/CAnimationStoryboardEventHandler::SetAnimationController
helpviewer_keywords:
- CAnimationStoryboardEventHandler [MFC], CAnimationStoryboardEventHandler
- CAnimationStoryboardEventHandler [MFC], CreateInstance
- CAnimationStoryboardEventHandler [MFC], OnStoryboardStatusChanged
- CAnimationStoryboardEventHandler [MFC], OnStoryboardUpdated
- CAnimationStoryboardEventHandler [MFC], SetAnimationController
ms.assetid: 10a7e86b-c02d-4124-9a2e-61ecf8ac62fc
ms.openlocfilehash: 7208ba91ec78a6de688699183b55a691b8e3d28d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97254746"
---
# <a name="canimationstoryboardeventhandler-class"></a>Класс CAnimationStoryboardEventHandler

Реализует обратный вызов, используемый API анимации при изменении состояния или обновлении раскадровки.

## <a name="syntax"></a>Синтаксис

```
class CAnimationStoryboardEventHandler : public CUIAnimationStoryboardEventHandlerBase<CAnimationStoryboardEventHandler>;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Каниматионсторибоардевенсандлер:: Каниматионсторибоардевенсандлер](#canimationstoryboardeventhandler)|Формирует объект `CAnimationStoryboardEventHandler`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Каниматионсторибоардевенсандлер:: CreateInstance](#createinstance)|Создает экземпляр `CAnimationStoryboardEventHandler` обратного вызова.|
|[Каниматионсторибоардевенсандлер:: Онсторибоардстатусчанжед](#onstoryboardstatuschanged)|Обрабатывает `OnStoryboardStatusChanged` события, происходящие при изменении состояния раскадровки (переопределений `CUIAnimationStoryboardEventHandlerBase::OnStoryboardStatusChanged` ).|
|[Каниматионсторибоардевенсандлер:: Онсторибоардупдатед](#onstoryboardupdated)|Обрабатывает `OnStoryboardUpdated` события, происходящие при обновлении раскадровки (переопределения `CUIAnimationStoryboardEventHandlerBase::OnStoryboardUpdated` .)|
|[Каниматионсторибоардевенсандлер:: Сетаниматионконтроллер](#setanimationcontroller)|Хранит указатель на контроллер анимации для маршрутизации событий.|

## <a name="remarks"></a>Комментарии

Этот обработчик событий создается и передается `IUIAnimationStoryboard::SetStoryboardEventHandler` методу при вызове метода `CAnimationController::EnableStoryboardEventHandler` .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CUIAnimationCallbackBase`

`CUIAnimationStoryboardEventHandlerBase`

`CAnimationStoryboardEventHandler`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationstoryboardeventhandlercanimationstoryboardeventhandler"></a><a name="canimationstoryboardeventhandler"></a> Каниматионсторибоардевенсандлер:: Каниматионсторибоардевенсандлер

Конструирует объект Каниматионсторибоардевенсандлер.

```
CAnimationStoryboardEventHandler();
```

## <a name="canimationstoryboardeventhandlercreateinstance"></a><a name="createinstance"></a> Каниматионсторибоардевенсандлер:: CreateInstance

Создает экземпляр обратного вызова Каниматионсторибоардевенсандлер.

```
static COM_DECLSPEC_NOTHROW HRESULT CreateInstance(
    CAnimationController* pAnimationController,
    IUIAnimationStoryboardEventHandler** ppHandler);
```

### <a name="parameters"></a>Параметры

*паниматионконтроллер*<br/>
Указатель на контроллер анимации, который будет принимать события.

*пфандлер*

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="canimationstoryboardeventhandleronstoryboardstatuschanged"></a><a name="onstoryboardstatuschanged"></a> Каниматионсторибоардевенсандлер:: Онсторибоардстатусчанжед

Обрабатывает события Онсторибоардстатусчанжед, происходящие при изменении состояния раскадровки

```
IFACEMETHOD(OnStoryboardStatusChanged) (
    __in IUIAnimationStoryboard* storyboard,
    __in UI_ANIMATION_STORYBOARD_STATUS newStatus,
    __in UI_ANIMATION_STORYBOARD_STATUS previousStatus);
```

### <a name="parameters"></a>Параметры

*выполнена*<br/>
Указатель на раскадровку, состояние которой изменилось.

*невстатус*<br/>
Указывает новое состояние раскадровки.

*превиаусстатус*<br/>
Указывает предыдущее состояние раскадровки.

### <a name="return-value"></a>Возвращаемое значение

S_OK, если метод выполнен. в противном случае E_FAIL.

## <a name="canimationstoryboardeventhandleronstoryboardupdated"></a><a name="onstoryboardupdated"></a> Каниматионсторибоардевенсандлер:: Онсторибоардупдатед

Обрабатывает события Онсторибоардупдатед, происходящие при обновлении раскадровки

```
IFACEMETHOD(OnStoryboardUpdated) (__in IUIAnimationStoryboard* storyboard);
```

### <a name="parameters"></a>Параметры

*выполнена*<br/>
Указатель на раскадровку, которая была обновлена.

### <a name="return-value"></a>Возвращаемое значение

S_OK, если метод выполнен. в противном случае E_FAIL.

## <a name="canimationstoryboardeventhandlersetanimationcontroller"></a><a name="setanimationcontroller"></a> Каниматионсторибоардевенсандлер:: Сетаниматионконтроллер

Хранит указатель на контроллер анимации для маршрутизации событий.

```cpp
void SetAnimationController(CAnimationController* pAnimationController);
```

### <a name="parameters"></a>Параметры

*паниматионконтроллер*<br/>
Указатель на контроллер анимации, который будет принимать события.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
