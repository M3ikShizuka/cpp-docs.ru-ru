---
description: 'Дополнительные сведения о: Каниматионманажеревенсандлер Class'
title: Класс CAnimationManagerEventHandler
ms.date: 11/04/2016
f1_keywords:
- CAnimationManagerEventHandler
- AFXANIMATIONCONTROLLER/CAnimationManagerEventHandler
- AFXANIMATIONCONTROLLER/CAnimationManagerEventHandler::CAnimationManagerEventHandler
- AFXANIMATIONCONTROLLER/CAnimationManagerEventHandler::CreateInstance
- AFXANIMATIONCONTROLLER/CAnimationManagerEventHandler::OnManagerStatusChanged
- AFXANIMATIONCONTROLLER/CAnimationManagerEventHandler::SetAnimationController
helpviewer_keywords:
- CAnimationManagerEventHandler [MFC], CAnimationManagerEventHandler
- CAnimationManagerEventHandler [MFC], CreateInstance
- CAnimationManagerEventHandler [MFC], OnManagerStatusChanged
- CAnimationManagerEventHandler [MFC], SetAnimationController
ms.assetid: 6089ec07-e661-4805-b227-823b4652aade
ms.openlocfilehash: aab944c23822486bbc04bb7710d257dd8c42beed
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97207950"
---
# <a name="canimationmanagereventhandler-class"></a>Класс CAnimationManagerEventHandler

Реализует обратный вызов, используемый API анимации при изменении состояния диспетчера анимации.

## <a name="syntax"></a>Синтаксис

```
class CAnimationManagerEventHandler : public CUIAnimationManagerEventHandlerBase<CAnimationManagerEventHandler>;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Каниматионманажеревенсандлер:: Каниматионманажеревенсандлер](#canimationmanagereventhandler)|Формирует объект `CAnimationManagerEventHandler`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Каниматионманажеревенсандлер:: CreateInstance](#createinstance)|Создает экземпляр `CAnimationManagerEventHandler` объекта.|
|[Каниматионманажеревенсандлер:: Онманажерстатусчанжед](#onmanagerstatuschanged)|Вызывается, когда изменилось состояние диспетчера анимации. (Переопределяет `CUIAnimationManagerEventHandlerBase::OnManagerStatusChanged`.)|
|[Каниматионманажеревенсандлер:: Сетаниматионконтроллер](#setanimationcontroller)|Хранит указатель на контроллер анимации для маршрутизации событий.|

## <a name="remarks"></a>Комментарии

Этот обработчик событий создается и передается методу Иуианиматионманажер:: Сетманажеревенсандлер при вызове Каниматионконтроллер:: Енаблеаниматионманажеревент.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CUIAnimationCallbackBase`

`CUIAnimationManagerEventHandlerBase`

`CAnimationManagerEventHandler`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationmanagereventhandlercanimationmanagereventhandler"></a><a name="canimationmanagereventhandler"></a> Каниматионманажеревенсандлер:: Каниматионманажеревенсандлер

Требуется Visual Studio 2010 с пакетом обновления 1 (SP1).

Конструирует объект Каниматионманажеревенсандлер.

```
CAnimationManagerEventHandler();
```

## <a name="canimationmanagereventhandlercreateinstance"></a><a name="createinstance"></a> Каниматионманажеревенсандлер:: CreateInstance

Требуется Visual Studio 2010 с пакетом обновления 1 (SP1).

Создает экземпляр объекта Каниматионманажеревенсандлер.

```
static COM_DECLSPEC_NOTHROW HRESULT CreateInstance(
    CAnimationController* pAnimationController,
    IUIAnimationManagerEventHandler** ppManagerEventHandler);
```

### <a name="parameters"></a>Параметры

*паниматионконтроллер*<br/>
Указатель на контроллер анимации, который будет принимать события.

*ппманажеревенсандлер*<br/>
Выходные данные. Если метод выполнен, он содержит указатель на COM-объект, который будет поддерживать обновления состояния для диспетчера анимации.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="canimationmanagereventhandleronmanagerstatuschanged"></a><a name="onmanagerstatuschanged"></a> Каниматионманажеревенсандлер:: Онманажерстатусчанжед

Требуется Visual Studio 2010 с пакетом обновления 1 (SP1).

Вызывается, когда изменилось состояние диспетчера анимации.

```
IFACEMETHOD(OnManagerStatusChanged)(
    UI_ANIMATION_MANAGER_STATUS newStatus,
    UI_ANIMATION_MANAGER_STATUS previousStatus);
```

### <a name="parameters"></a>Параметры

*невстатус*<br/>
Новое состояние.

*превиаусстатус*<br/>
Предыдущее состояние.

### <a name="return-value"></a>Возвращаемое значение

Текущая реализация всегда возвращает S_OK;

## <a name="canimationmanagereventhandlersetanimationcontroller"></a><a name="setanimationcontroller"></a> Каниматионманажеревенсандлер:: Сетаниматионконтроллер

Требуется Visual Studio 2010 с пакетом обновления 1 (SP1).

Хранит указатель на контроллер анимации для маршрутизации событий.

```cpp
void SetAnimationController(CAnimationController* pAnimationController);
```

### <a name="parameters"></a>Параметры

*паниматионконтроллер*<br/>
Указатель на контроллер анимации, который будет принимать события.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
