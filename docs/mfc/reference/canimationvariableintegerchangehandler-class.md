---
description: 'Дополнительные сведения о: Каниматионвариаблеинтежерчанжехандлер Class'
title: Класс CAnimationVariableIntegerChangeHandler
ms.date: 11/04/2016
f1_keywords:
- CAnimationVariableIntegerChangeHandler
- AFXANIMATIONCONTROLLER/CAnimationVariableIntegerChangeHandler
- AFXANIMATIONCONTROLLER/CAnimationVariableIntegerChangeHandler::CAnimationVariableIntegerChangeHandler
- AFXANIMATIONCONTROLLER/CAnimationVariableIntegerChangeHandler::CreateInstance
- AFXANIMATIONCONTROLLER/CAnimationVariableIntegerChangeHandler::OnIntegerValueChanged
- AFXANIMATIONCONTROLLER/CAnimationVariableIntegerChangeHandler::SetAnimationController
helpviewer_keywords:
- CAnimationVariableIntegerChangeHandler [MFC], CAnimationVariableIntegerChangeHandler
- CAnimationVariableIntegerChangeHandler [MFC], CreateInstance
- CAnimationVariableIntegerChangeHandler [MFC], OnIntegerValueChanged
- CAnimationVariableIntegerChangeHandler [MFC], SetAnimationController
ms.assetid: 6ac8e91b-e514-4ff6-babd-33f77c4b2b61
ms.openlocfilehash: 53a0a1838e021294b4ccc870e6f01b873233a0c9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336731"
---
# <a name="canimationvariableintegerchangehandler-class"></a>Класс CAnimationVariableIntegerChangeHandler

Реализует обратный вызов, используемый API анимации при изменении значения переменной анимации.

## <a name="syntax"></a>Синтаксис

```
class CAnimationVariableIntegerChangeHandler : public CUIAnimationVariableIntegerChangeHandlerBase<CAnimationVariableIntegerChangeHandler>;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Каниматионвариаблеинтежерчанжехандлер:: Каниматионвариаблеинтежерчанжехандлер](#canimationvariableintegerchangehandler)|Формирует объект `CAnimationVariableIntegerChangeHandler`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Каниматионвариаблеинтежерчанжехандлер:: CreateInstance](#createinstance)|Создает экземпляр `CAnimationVariableIntegerChangeHandler` обратного вызова.|
|[Каниматионвариаблеинтежерчанжехандлер:: Онинтежервалуечанжед](#onintegervaluechanged)|Вызывается, когда изменилось значение переменной анимации. (Переопределяет `CUIAnimationVariableIntegerChangeHandlerBase::OnIntegerValueChanged`.)|
|[Каниматионвариаблеинтежерчанжехандлер:: Сетаниматионконтроллер](#setanimationcontroller)|Хранит указатель на контроллер анимации для маршрутизации событий.|

## <a name="remarks"></a>Комментарии

Этот обработчик событий создается и передается методу Иуианиматионвариабле:: Сетвариаблеинтежерчанжехандлер при вызове CAnimationVariable:: Енаблеинтежервалуечанжедевент или CAnimationBaseObject:: EnableIntegerValueChangedEvent (который включает это событие для всех переменных анимации, инкапсулированных в объекте анимации).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[Классы MFC](../../mfc/reference/mfc-classes.md)

`CUIAnimationCallbackBase`

`CUIAnimationVariableIntegerChangeHandlerBase`

`CAnimationVariableIntegerChangeHandler`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationvariableintegerchangehandlercanimationvariableintegerchangehandler"></a><a name="canimationvariableintegerchangehandler"></a> Каниматионвариаблеинтежерчанжехандлер:: Каниматионвариаблеинтежерчанжехандлер

Конструирует объект Каниматионвариаблеинтежерчанжехандлер.

```
CAnimationVariableIntegerChangeHandler ();
```

## <a name="canimationvariableintegerchangehandlercreateinstance"></a><a name="createinstance"></a> Каниматионвариаблеинтежерчанжехандлер:: CreateInstance

Создает экземпляр обратного вызова Каниматионвариаблеинтежерчанжехандлер.

```
static COM_DECLSPEC_NOTHROW HRESULT CreateInstance(
    CAnimationController* pAnimationController,
    IUIAnimationVariableIntegerChangeHandler** ppHandler);
```

### <a name="parameters"></a>Параметры

*паниматионконтроллер*<br/>
Указатель на контроллер анимации, который будет принимать события.

*пфандлер*

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="canimationvariableintegerchangehandleronintegervaluechanged"></a><a name="onintegervaluechanged"></a> Каниматионвариаблеинтежерчанжехандлер:: Онинтежервалуечанжед

Вызывается, когда изменилось значение переменной анимации.

```
IFACEMETHOD(OnIntegerValueChanged) (
    __in IUIAnimationStoryboard* storyboard,
    __in IUIAnimationVariable* variable,
    __in INT32 newValue,
    __in INT32 previousValue);
```

### <a name="parameters"></a>Параметры

*выполнена*<br/>
Раскадровка, которая используется для анимации переменной.

*variable*<br/>
Переменная анимации, которая была обновлена.

*newValue*<br/>
Новое округленное значение.

*превиаусвалуе*<br/>
Предыдущее округленное значение.

### <a name="return-value"></a>Возвращаемое значение

S_OK, если метод выполнен. в противном случае E_FAIL.

## <a name="canimationvariableintegerchangehandlersetanimationcontroller"></a><a name="setanimationcontroller"></a> Каниматионвариаблеинтежерчанжехандлер:: Сетаниматионконтроллер

Хранит указатель на контроллер анимации для маршрутизации событий.

```cpp
void SetAnimationController(CAnimationController* pAnimationController);
```

### <a name="parameters"></a>Параметры

*паниматионконтроллер*<br/>
Указатель на контроллер анимации, который будет принимать события.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
