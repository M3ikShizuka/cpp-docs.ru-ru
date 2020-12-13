---
description: 'Дополнительные сведения о: Каниматионтимеревенсандлер Class'
title: Класс CAnimationTimerEventHandler
ms.date: 11/04/2016
f1_keywords:
- CAnimationTimerEventHandler
- AFXANIMATIONCONTROLLER/CAnimationTimerEventHandler
- AFXANIMATIONCONTROLLER/CAnimationTimerEventHandler::CreateInstance
- AFXANIMATIONCONTROLLER/CAnimationTimerEventHandler::OnPostUpdate
- AFXANIMATIONCONTROLLER/CAnimationTimerEventHandler::OnPreUpdate
- AFXANIMATIONCONTROLLER/CAnimationTimerEventHandler::OnRenderingTooSlow
- AFXANIMATIONCONTROLLER/CAnimationTimerEventHandler::SetAnimationController
helpviewer_keywords:
- CAnimationTimerEventHandler [MFC], CreateInstance
- CAnimationTimerEventHandler [MFC], OnPostUpdate
- CAnimationTimerEventHandler [MFC], OnPreUpdate
- CAnimationTimerEventHandler [MFC], OnRenderingTooSlow
- CAnimationTimerEventHandler [MFC], SetAnimationController
ms.assetid: 188dea3b-4b5e-4f6b-8df9-09d993a21619
ms.openlocfilehash: 5d5f3e07eeb7ffe3f3bb226afd566330808303ac
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336753"
---
# <a name="canimationtimereventhandler-class"></a>Класс CAnimationTimerEventHandler

Реализует обратный вызов, используемый API анимации, когда происходит событие расчета времени.

## <a name="syntax"></a>Синтаксис

```
class CAnimationTimerEventHandler : public CUIAnimationTimerEventHandlerBase<CAnimationTimerEventHandler>;
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Каниматионтимеревенсандлер:: CreateInstance](#createinstance)|Создает экземпляр `CAnimationTimerEventHandler` обратного вызова.|
|[Каниматионтимеревенсандлер:: Онпоступдате](#onpostupdate)|Обрабатывает события, происходящие после завершения обновления анимации. (Переопределяет `CUIAnimationTimerEventHandlerBase::OnPostUpdate`.)|
|[Каниматионтимеревенсандлер:: Онпреупдате](#onpreupdate)|Обрабатывает события, происходящие перед началом обновления анимации. (Переопределяет `CUIAnimationTimerEventHandlerBase::OnPreUpdate`.)|
|[Каниматионтимеревенсандлер:: Онрендерингтуслов](#onrenderingtooslow)|Обрабатывает события, происходящие, когда частота кадров отрисовки для анимации падает ниже минимально желаемой частоты кадров. (Переопределяет `CUIAnimationTimerEventHandlerBase::OnRenderingTooSlow`.)|
|[Каниматионтимеревенсандлер:: Сетаниматионконтроллер](#setanimationcontroller)|Хранит указатель на контроллер анимации для маршрутизации событий.|

## <a name="remarks"></a>Комментарии

Этот обработчик событий создается и передается в Иуианиматионтимер:: Сеттимеревенсандлер при вызове Каниматионконтроллер:: Енаблеаниматионтимеревенсандлер.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CUIAnimationCallbackBase`

`CUIAnimationTimerEventHandlerBase`

`CAnimationTimerEventHandler`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationtimereventhandlercreateinstance"></a><a name="createinstance"></a> Каниматионтимеревенсандлер:: CreateInstance

Создает экземпляр обратного вызова Каниматионтимеревенсандлер.

```
static COM_DECLSPEC_NOTHROW HRESULT CreateInstance(
    CAnimationController* pAnimationController,
    IUIAnimationTimerEventHandler** ppTimerEventHandler);
```

### <a name="parameters"></a>Параметры

*паниматионконтроллер*<br/>
Указатель на контроллер анимации, который будет принимать события.

*пптимеревенсандлер*

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="canimationtimereventhandleronpostupdate"></a><a name="onpostupdate"></a> Каниматионтимеревенсандлер:: Онпоступдате

Обрабатывает события, происходящие после завершения обновления анимации.

```
IFACEMETHOD(OnPostUpdate)();
```

### <a name="return-value"></a>Возвращаемое значение

S_OK, если метод выполнен. в противном случае E_FAIL.

## <a name="canimationtimereventhandleronpreupdate"></a><a name="onpreupdate"></a> Каниматионтимеревенсандлер:: Онпреупдате

Обрабатывает события, происходящие перед началом обновления анимации.

```
IFACEMETHOD(OnPreUpdate)();
```

### <a name="return-value"></a>Возвращаемое значение

S_OK, если метод выполнен. в противном случае E_FAIL.

## <a name="canimationtimereventhandleronrenderingtooslow"></a><a name="onrenderingtooslow"></a> Каниматионтимеревенсандлер:: Онрендерингтуслов

Обрабатывает события, происходящие, когда частота кадров отрисовки для анимации падает ниже минимально желаемой частоты кадров.

```
IFACEMETHOD(OnRenderingTooSlow)(UINT32 fps);
```

### <a name="parameters"></a>Параметры

*частота*

### <a name="return-value"></a>Возвращаемое значение

S_OK, если метод выполнен. в противном случае E_FAIL.

## <a name="canimationtimereventhandlersetanimationcontroller"></a><a name="setanimationcontroller"></a> Каниматионтимеревенсандлер:: Сетаниматионконтроллер

Хранит указатель на контроллер анимации для маршрутизации событий.

```cpp
void SetAnimationController(CAnimationController* pAnimationController);
```

### <a name="parameters"></a>Параметры

*паниматионконтроллер*<br/>
Указатель на контроллер анимации, который будет принимать события.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
