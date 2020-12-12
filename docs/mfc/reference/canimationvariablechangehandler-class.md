---
description: 'Дополнительные сведения о: CAnimationVariableChangeHandler Class'
title: Класс CAnimationVariableChangeHandler
ms.date: 11/04/2016
f1_keywords:
- CAnimationVariableChangeHandler
- AFXANIMATIONCONTROLLER/CAnimationVariableChangeHandler
- AFXANIMATIONCONTROLLER/CAnimationVariableChangeHandler::OnValueChanged
- AFXANIMATIONCONTROLLER/CAnimationVariableChangeHandler::SetAnimationController
helpviewer_keywords:
- CAnimationVariableChangeHandler [MFC], OnValueChanged
- CAnimationVariableChangeHandler [MFC], SetAnimationController
ms.assetid: 2ea4996d-5c04-4dfc-be79-d42d55050795
ms.openlocfilehash: 1c97bc908a29bfb7edf2222f6df117fefdaf4091
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97207882"
---
# <a name="canimationvariablechangehandler-class"></a>Класс CAnimationVariableChangeHandler

Реализует обратный вызов, используемый API анимации при изменении значения переменной анимации.

## <a name="syntax"></a>Синтаксис

```
class CAnimationVariableChangeHandler : public CUIAnimationVariableChangeHandlerBase<CAnimationVariableChangeHandler>;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CAnimationVariableChangeHandler::CAnimationVariableChangeHandler`|Формирует объект `CAnimationVariableChangeHandler`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|`CAnimationVariableChangeHandler::CreateInstance`|Создает экземпляр `CAnimationVariableChangeHandler` объекта.|
|[CAnimationVariableChangeHandler:: Онвалуечанжед](#onvaluechanged)|Вызывается, когда изменилось значение переменной анимации. (Переопределяет `CUIAnimationVariableChangeHandlerBase::OnValueChanged`.)|
|[CAnimationVariableChangeHandler:: Сетаниматионконтроллер](#setanimationcontroller)|Хранит указатель на контроллер анимации для маршрутизации событий.|

## <a name="remarks"></a>Комментарии

Этот обработчик событий создается и передается `IUIAnimationVariable::SetVariableChangeHandler` методу при вызове `CAnimationVariable::EnableValueChangedEvent` или `CAnimationBaseObject::EnableValueChangedEvent` (который включает это событие для всех переменных анимации, инкапсулированных в объекте анимации).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CUIAnimationCallbackBase`

`CUIAnimationVariableChangeHandlerBase`

`CAnimationVariableChangeHandler`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationvariablechangehandleronvaluechanged"></a><a name="onvaluechanged"></a> CAnimationVariableChangeHandler:: Онвалуечанжед

Вызывается, когда изменилось значение переменной анимации.

```
IFACEMETHOD(OnValueChanged) (
    __in IUIAnimationStoryboard* storyboard,
    __in IUIAnimationVariable* variable,
    __in DOUBLE newValue,
    __in DOUBLE previousValue);
```

### <a name="parameters"></a>Параметры

*выполнена*<br/>
Раскадровка, которая используется для анимации переменной.

*variable*<br/>
Переменная анимации, которая была обновлена.

*newValue*<br/>
Новое значение.

*превиаусвалуе*<br/>
Предыдущее значение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="canimationvariablechangehandlersetanimationcontroller"></a><a name="setanimationcontroller"></a> CAnimationVariableChangeHandler:: Сетаниматионконтроллер

Хранит указатель на контроллер анимации для маршрутизации событий.

```cpp
void SetAnimationController(CAnimationController* pAnimationController);
```

### <a name="parameters"></a>Параметры

*паниматионконтроллер*<br/>
Указатель на контроллер анимации, который будет принимать события.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
