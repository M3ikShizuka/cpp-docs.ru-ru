---
description: 'Дополнительные сведения о: Цинтерполаторбасе Class'
title: Класс CInterpolatorBase
ms.date: 11/04/2016
f1_keywords:
- CInterpolatorBase
- AFXANIMATIONCONTROLLER/CInterpolatorBase
- AFXANIMATIONCONTROLLER/CInterpolatorBase::CInterpolatorBase
- AFXANIMATIONCONTROLLER/CInterpolatorBase::CreateInstance
- AFXANIMATIONCONTROLLER/CInterpolatorBase::GetDependencies
- AFXANIMATIONCONTROLLER/CInterpolatorBase::GetDuration
- AFXANIMATIONCONTROLLER/CInterpolatorBase::GetFinalValue
- AFXANIMATIONCONTROLLER/CInterpolatorBase::InterpolateValue
- AFXANIMATIONCONTROLLER/CInterpolatorBase::InterpolateVelocity
- AFXANIMATIONCONTROLLER/CInterpolatorBase::SetCustomInterpolator
- AFXANIMATIONCONTROLLER/CInterpolatorBase::SetDuration
- AFXANIMATIONCONTROLLER/CInterpolatorBase::SetInitialValueAndVelocity
helpviewer_keywords:
- CInterpolatorBase [MFC], CInterpolatorBase
- CInterpolatorBase [MFC], CreateInstance
- CInterpolatorBase [MFC], GetDependencies
- CInterpolatorBase [MFC], GetDuration
- CInterpolatorBase [MFC], GetFinalValue
- CInterpolatorBase [MFC], InterpolateValue
- CInterpolatorBase [MFC], InterpolateVelocity
- CInterpolatorBase [MFC], SetCustomInterpolator
- CInterpolatorBase [MFC], SetDuration
- CInterpolatorBase [MFC], SetInitialValueAndVelocity
ms.assetid: bbc3dce7-8398-47f9-b97e-e4fd2d737232
ms.openlocfilehash: 73204e8b81db862fe30058d1b2451ea468d332e8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340961"
---
# <a name="cinterpolatorbase-class"></a>Класс CInterpolatorBase

Реализует обратный вызов, используемый API анимации, когда требуется рассчитать новое значение переменной анимации.

## <a name="syntax"></a>Синтаксис

```
class CInterpolatorBase : public CUIAnimationInterpolatorBase<CInterpolatorBase>;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Цинтерполаторбасе:: Цинтерполаторбасе](#cinterpolatorbase)|Конструирует `CInterpolatorBase` объект.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Цинтерполаторбасе:: CreateInstance](#createinstance)|Создает экземпляр `CInterpolatorBase` и сохраняет указатель на настраиваемую интерполяцию, которая будет обрабатывать события.|
|[Цинтерполаторбасе:: Dependencies](#getdependencies)|Возвращает зависимости интерполяции. (Переопределяет `CUIAnimationInterpolatorBase::GetDependencies`.)|
|[Цинтерполаторбасе:: длит](#getduration)|Возвращает длительность интерполяции. (Переопределяет `CUIAnimationInterpolatorBase::GetDuration`.)|
|[Цинтерполаторбасе:: Жетфиналвалуе](#getfinalvalue)|Возвращает конечное значение, которое вызывает интерполяцию. (Переопределяет `CUIAnimationInterpolatorBase::GetFinalValue`.)|
|[Цинтерполаторбасе:: Интерполатевалуе](#interpolatevalue)|Выполняет интерполяцию значения в заданном смещении (переопределения `CUIAnimationInterpolatorBase::InterpolateValue` .)|
|[Цинтерполаторбасе:: ИнтерполатевелоЦити](#interpolatevelocity)|Интерполирует скорость в заданном смещении (переопределения `CUIAnimationInterpolatorBase::InterpolateVelocity` .)|
|[Цинтерполаторбасе:: Сеткустоминтерполатор](#setcustominterpolator)|Хранит указатель на пользовательский интерполяций, который будет обрабатывать события.|
|[Цинтерполаторбасе:: Сетдуратион](#setduration)|Задает длительность интерполяции (переопределения `CUIAnimationInterpolatorBase::SetDuration` .)|
|[Цинтерполаторбасе:: СетинитиалвалуеандвелоЦити](#setinitialvalueandvelocity)|Задает начальное значение и скорость для интерполяции. (Переопределяет `CUIAnimationInterpolatorBase::SetInitialValueAndVelocity`.)|

## <a name="remarks"></a>Комментарии

Этот обработчик создается и передается в, `IUIAnimationTransitionFactory::CreateTransition` когда `CCustomTransition` объект создается как часть процесса инициализации анимации (запускается с помощью `CAnimationController::AnimateGroup` ). Обычно этот класс не требуется использовать напрямую, он просто перенадает все события в `CCustomInterpolator` производный класс, указатель которого передан конструктору `CCustomTransition` .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CUIAnimationCallbackBase`

`CUIAnimationInterpolatorBase`

`CInterpolatorBase`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="cinterpolatorbasecinterpolatorbase"></a><a name="cinterpolatorbase"></a> Цинтерполаторбасе:: Цинтерполаторбасе

Конструирует объект Цинтерполаторбасе.

```
CInterpolatorBase();
```

## <a name="cinterpolatorbasecreateinstance"></a><a name="createinstance"></a> Цинтерполаторбасе:: CreateInstance

Создает экземпляр Цинтерполаторбасе и сохраняет указатель на настраиваемую интерполяцию, которая будет обрабатывать события.

```
static COM_DECLSPEC_NOTHROW HRESULT CreateInstance(
    CCustomInterpolator* pInterpolator,
    IUIAnimationInterpolator** ppHandler);
```

### <a name="parameters"></a>Параметры

*пинтерполатор*<br/>
Указатель на настраиваемый интерполяцию.

*пфандлер*<br/>
Выходные данные. Содержит указатель на экземпляр Цинтерполаторбасе при возврате функции.

### <a name="return-value"></a>Возвращаемое значение

## <a name="cinterpolatorbasegetdependencies"></a><a name="getdependencies"></a> Цинтерполаторбасе:: Dependencies

Возвращает зависимости интерполяции.

```
IFACEMETHOD(GetDependencies)(
    __out UI_ANIMATION_DEPENDENCIES* initialValueDependencies,
    __out UI_ANIMATION_DEPENDENCIES* initialVelocityDependencies,
    __out UI_ANIMATION_DEPENDENCIES* durationDependencies);
```

### <a name="parameters"></a>Параметры

*инитиалвалуедепенденЦиес*<br/>
Выходные данные. Аспекты интерполяции, зависящие от первоначального значения, переданного в СетинитиалвалуеандвелоЦити.

*инитиалвелоЦитидепенденЦиес*<br/>
Выходные данные. Аспекты интерполяции, зависящие от начальной скорости, передаваемой в СетинитиалвалуеандвелоЦити.

*дуратиондепенденЦиес*<br/>
Выходные данные. Аспекты интерполяции, зависящие от длительности, переданной в Сетдуратион.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. Он возвращает E_FAIL, если Ккустоминтерполатор не задан, или пользовательская реализация возвращает значение FALSE из метода DEPENDENCIES.

## <a name="cinterpolatorbasegetduration"></a><a name="getduration"></a> Цинтерполаторбасе:: длит

Возвращает длительность интерполяции.

```
IFACEMETHOD(GetDuration)(__out UI_ANIMATION_SECONDS* duration);
```

### <a name="parameters"></a>Параметры

*duration*<br/>
Выходные данные. Длительность перехода в секундах.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. Он возвращает E_FAIL, если Ккустоминтерполатор не задан, или пользовательская реализация возвращает значение FALSE из метода IsFalse.

## <a name="cinterpolatorbasegetfinalvalue"></a><a name="getfinalvalue"></a> Цинтерполаторбасе:: Жетфиналвалуе

Возвращает конечное значение, которое вызывает интерполяцию.

```
IFACEMETHOD(GetFinalValue)(__out DOUBLE* value);
```

### <a name="parameters"></a>Параметры

*value*<br/>
Выходные данные. Конечное значение переменной в конце перехода.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. Он возвращает E_FAIL, если Ккустоминтерполатор не задан, или пользовательская реализация возвращает значение FALSE из метода Жетфиналвалуе.

## <a name="cinterpolatorbaseinterpolatevalue"></a><a name="interpolatevalue"></a> Цинтерполаторбасе:: Интерполатевалуе

Выполняет интерполяцию значения по заданному смещению

```
IFACEMETHOD(InterpolateValue)(
    __in UI_ANIMATION_SECONDS offset,
    __out DOUBLE* value);
```

### <a name="parameters"></a>Параметры

*offset*<br/>
Смещение от начала перехода. Смещение всегда больше или равно нулю и меньше, чем длительность перехода. Этот метод не вызывается, если длительность перехода равна нулю.

*value*<br/>
Выходные данные. Значение интерполяции.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. Он возвращает E_FAIL, если Ккустоминтерполатор не задан, или пользовательская реализация возвращает значение FALSE из метода Интерполатевалуе.

## <a name="cinterpolatorbaseinterpolatevelocity"></a><a name="interpolatevelocity"></a> Цинтерполаторбасе:: ИнтерполатевелоЦити

Интерполяция скорости в заданном смещении

```
IFACEMETHOD(InterpolateVelocity)(
    __in UI_ANIMATION_SECONDS offset,
    __out DOUBLE* velocity);
```

### <a name="parameters"></a>Параметры

*offset*<br/>
Смещение от начала перехода. Смещение всегда больше или равно нулю и меньше или равно длительности перехода. Этот метод не вызывается, если длительность перехода равна нулю.

*скорость*<br/>
Выходные данные. Скорость переменной в смещении.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. Он возвращает E_FAIL, если Ккустоминтерполатор не задан, или пользовательская реализация возвращает значение FALSE из метода ИнтерполатевелоЦити.

## <a name="cinterpolatorbasesetcustominterpolator"></a><a name="setcustominterpolator"></a> Цинтерполаторбасе:: Сеткустоминтерполатор

Хранит указатель на пользовательский интерполяций, который будет обрабатывать события.

```cpp
void SetCustomInterpolator(CCustomInterpolator* pInterpolator);
```

### <a name="parameters"></a>Параметры

*пинтерполатор*<br/>
Указатель на настраиваемый интерполяцию.

## <a name="cinterpolatorbasesetduration"></a><a name="setduration"></a> Цинтерполаторбасе:: Сетдуратион

Задает длительность интерполяции

```
IFACEMETHOD(SetDuration)(__in UI_ANIMATION_SECONDS duration);
```

### <a name="parameters"></a>Параметры

*duration*<br/>
Длительность перехода.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. Он возвращает E_FAIL, если Ккустоминтерполатор не задан, или пользовательская реализация возвращает значение FALSE из метода Сетдуратион.

## <a name="cinterpolatorbasesetinitialvalueandvelocity"></a><a name="setinitialvalueandvelocity"></a> Цинтерполаторбасе:: СетинитиалвалуеандвелоЦити

Задает начальное значение и скорость для интерполяции.

```
IFACEMETHOD(SetInitialValueAndVelocity)(
    __in DOUBLE initialValue,
    __in DOUBLE initialVelocity);
```

### <a name="parameters"></a>Параметры

*инитиалвалуе*<br/>
Значение переменной в начале перехода.

*InitialVelocity равно*<br/>
Скорость переменной в начале перехода.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. Он возвращает E_FAIL, если Ккустоминтерполатор не задан, или пользовательская реализация возвращает значение FALSE из метода СетинитиалвалуеандвелоЦити.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
