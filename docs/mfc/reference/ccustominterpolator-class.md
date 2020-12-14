---
description: 'Дополнительные сведения о: Ккустоминтерполатор Class'
title: Класс CCustomInterpolator
ms.date: 11/04/2016
f1_keywords:
- CCustomInterpolator
- AFXANIMATIONCONTROLLER/CCustomInterpolator
- AFXANIMATIONCONTROLLER/CCustomInterpolator::CCustomInterpolator
- AFXANIMATIONCONTROLLER/CCustomInterpolator::GetDependencies
- AFXANIMATIONCONTROLLER/CCustomInterpolator::GetDuration
- AFXANIMATIONCONTROLLER/CCustomInterpolator::GetFinalValue
- AFXANIMATIONCONTROLLER/CCustomInterpolator::Init
- AFXANIMATIONCONTROLLER/CCustomInterpolator::InterpolateValue
- AFXANIMATIONCONTROLLER/CCustomInterpolator::InterpolateVelocity
- AFXANIMATIONCONTROLLER/CCustomInterpolator::SetDuration
- AFXANIMATIONCONTROLLER/CCustomInterpolator::SetInitialValueAndVelocity
- AFXANIMATIONCONTROLLER/CCustomInterpolator::m_currentValue
- AFXANIMATIONCONTROLLER/CCustomInterpolator::m_currentVelocity
- AFXANIMATIONCONTROLLER/CCustomInterpolator::m_duration
- AFXANIMATIONCONTROLLER/CCustomInterpolator::m_finalValue
- AFXANIMATIONCONTROLLER/CCustomInterpolator::m_initialValue
- AFXANIMATIONCONTROLLER/CCustomInterpolator::m_initialVelocity
helpviewer_keywords:
- CCustomInterpolator [MFC], CCustomInterpolator
- CCustomInterpolator [MFC], GetDependencies
- CCustomInterpolator [MFC], GetDuration
- CCustomInterpolator [MFC], GetFinalValue
- CCustomInterpolator [MFC], Init
- CCustomInterpolator [MFC], InterpolateValue
- CCustomInterpolator [MFC], InterpolateVelocity
- CCustomInterpolator [MFC], SetDuration
- CCustomInterpolator [MFC], SetInitialValueAndVelocity
- CCustomInterpolator [MFC], m_currentValue
- CCustomInterpolator [MFC], m_currentVelocity
- CCustomInterpolator [MFC], m_duration
- CCustomInterpolator [MFC], m_finalValue
- CCustomInterpolator [MFC], m_initialValue
- CCustomInterpolator [MFC], m_initialVelocity
ms.assetid: 28d85595-989a-40a3-b003-e0e38437a94d
ms.openlocfilehash: 84fcdc20ce1a90441a508f1469d498095980af83
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227758"
---
# <a name="ccustominterpolator-class"></a>Класс CCustomInterpolator

Реализует базовый интерполятор.

## <a name="syntax"></a>Синтаксис

```
class CCustomInterpolator;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккустоминтерполатор:: Ккустоминтерполатор](#ccustominterpolator)|Перегружен. Создает пользовательский объект интерполяции и инициализирует заданные значения длительности и скорости.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккустоминтерполатор:: Dependencies](#getdependencies)|Возвращает зависимости интерполяции.|
|[Ккустоминтерполатор:: длит](#getduration)|Возвращает длительность интерполяции.|
|[Ккустоминтерполатор:: Жетфиналвалуе](#getfinalvalue)|Возвращает конечное значение, которое вызывает интерполяцию.|
|[Ккустоминтерполатор:: init](#init)|Инициализирует длительность и окончательное значение.|
|[Ккустоминтерполатор:: Интерполатевалуе](#interpolatevalue)|Выполняет интерполяцию значения по заданному смещению.|
|[Ккустоминтерполатор:: ИнтерполатевелоЦити](#interpolatevelocity)|Интерполяция скорости в заданном смещении|
|[Ккустоминтерполатор:: Сетдуратион](#setduration)|Задает длительность интерполяции.|
|[Ккустоминтерполатор:: СетинитиалвалуеандвелоЦити](#setinitialvalueandvelocity)|Задает начальное значение и скорость для интерполяции.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Ккустоминтерполатор:: m_currentValue](#m_currentvalue)|Значение интерполяции.|
|[Ккустоминтерполатор:: m_currentVelocity](#m_currentvelocity)|Скорость интерполяции.|
|[Ккустоминтерполатор:: m_duration](#m_duration)|Длительность перехода.|
|[Ккустоминтерполатор:: m_finalValue](#m_finalvalue)|Конечное значение переменной в конце перехода.|
|[Ккустоминтерполатор:: m_initialValue](#m_initialvalue)|Значение переменной в начале перехода.|
|[Ккустоминтерполатор:: m_initialVelocity](#m_initialvelocity)|Скорость переменной в начале перехода.|

## <a name="remarks"></a>Комментарии

Создайте класс, производный от Ккустоминтерполатор, и Переопределите все необходимые методы, чтобы реализовать пользовательский алгоритм интерполяции. Указатель на этот класс должен передаваться в качестве параметра Ккустомтранситион.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CCustomInterpolator`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="ccustominterpolatorccustominterpolator"></a><a name="ccustominterpolator"></a> Ккустоминтерполатор:: Ккустоминтерполатор

Конструирует пользовательский объект интерполяции и задает для всех значений значение по умолчанию 0.

```
CCustomInterpolator();

CCustomInterpolator(
    UI_ANIMATION_SECONDS duration,
    DOUBLE finalValue);
```

### <a name="parameters"></a>Параметры

*duration*<br/>
Длительность перехода.

*финалвалуе*

### <a name="remarks"></a>Комментарии

Используйте Ккустоминтерполатор:: init для инициализации длительности и окончательного значения позже в коде.

## <a name="ccustominterpolatorgetdependencies"></a><a name="getdependencies"></a> Ккустоминтерполатор:: Dependencies

Возвращает зависимости интерполяции.

```
virtual BOOL GetDependencies(
    UI_ANIMATION_DEPENDENCIES* initialValueDependencies,
    UI_ANIMATION_DEPENDENCIES* initialVelocityDependencies,
    UI_ANIMATION_DEPENDENCIES* durationDependencies);
```

### <a name="parameters"></a>Параметры

*инитиалвалуедепенденЦиес*<br/>
Выходные данные. Аспекты интерполяции, зависящие от первоначального значения, переданного в СетинитиалвалуеандвелоЦити.

*инитиалвелоЦитидепенденЦиес*<br/>
Выходные данные. Аспекты интерполяции, зависящие от начальной скорости, передаваемой в СетинитиалвалуеандвелоЦити.

*дуратиондепенденЦиес*<br/>
Выходные данные. Аспекты интерполяции, зависящие от длительности, переданной в Сетдуратион.

### <a name="return-value"></a>Возвращаемое значение

Базовая реализация всегда возвращает значение TRUE. Возвращает значение FALSE от переопределенной реализации, если требуется завершить событие.

## <a name="ccustominterpolatorgetduration"></a><a name="getduration"></a> Ккустоминтерполатор:: длит

Возвращает длительность интерполяции.

```
virtual BOOL GetDuration(UI_ANIMATION_SECONDS* duration);
```

### <a name="parameters"></a>Параметры

*duration*<br/>
Выходные данные. Длительность перехода в секундах.

### <a name="return-value"></a>Возвращаемое значение

Базовая реализация всегда возвращает значение TRUE. Возвращает значение FALSE от переопределенной реализации, если требуется завершить событие.

## <a name="ccustominterpolatorgetfinalvalue"></a><a name="getfinalvalue"></a> Ккустоминтерполатор:: Жетфиналвалуе

Возвращает конечное значение, которое вызывает интерполяцию.

```
virtual BOOL GetFinalValue(DOUBLE* value);
```

### <a name="parameters"></a>Параметры

*value*<br/>
Выходные данные. Конечное значение переменной в конце перехода.

### <a name="return-value"></a>Возвращаемое значение

Базовая реализация всегда возвращает значение TRUE. Возвращает значение FALSE от переопределенной реализации, если требуется завершить событие.

## <a name="ccustominterpolatorinit"></a><a name="init"></a> Ккустоминтерполатор:: init

Инициализирует длительность и окончательное значение.

```cpp
void Init(
    UI_ANIMATION_SECONDS duration,
    DOUBLE finalValue);
```

### <a name="parameters"></a>Параметры

*duration*<br/>
Длительность перехода.

*финалвалуе*<br/>
Конечное значение переменной в конце перехода.

## <a name="ccustominterpolatorinterpolatevalue"></a><a name="interpolatevalue"></a> Ккустоминтерполатор:: Интерполатевалуе

Выполняет интерполяцию значения по заданному смещению.

```
virtual BOOL InterpolateValue(
    UI_ANIMATION_SECONDS */,
    DOUBLE* value);
```

### <a name="parameters"></a>Параметры

*value*<br/>
Выходные данные. Значение интерполяции.

### <a name="return-value"></a>Возвращаемое значение

Базовая реализация всегда возвращает значение TRUE. Возвращает значение FALSE от переопределенной реализации, если требуется завершить событие.

## <a name="ccustominterpolatorinterpolatevelocity"></a><a name="interpolatevelocity"></a> Ккустоминтерполатор:: ИнтерполатевелоЦити

Интерполяция скорости в заданном смещении

```
virtual BOOL InterpolateVelocity(
    UI_ANIMATION_SECONDS */,
    DOUBLE* velocity);
```

### <a name="parameters"></a>Параметры

*скорость*<br/>
Выходные данные. Скорость переменной в смещении.

### <a name="return-value"></a>Возвращаемое значение

Базовая реализация всегда возвращает значение TRUE. Возвращает значение FALSE от переопределенной реализации, если требуется завершить событие.

## <a name="ccustominterpolatorm_currentvalue"></a><a name="m_currentvalue"></a> Ккустоминтерполатор:: m_currentValue

Значение интерполяции.

```
DOUBLE m_currentValue;
```

## <a name="ccustominterpolatorm_currentvelocity"></a><a name="m_currentvelocity"></a> Ккустоминтерполатор:: m_currentVelocity

Скорость интерполяции.

```
DOUBLE m_currentVelocity;
```

## <a name="ccustominterpolatorm_duration"></a><a name="m_duration"></a> Ккустоминтерполатор:: m_duration

Длительность перехода.

```
UI_ANIMATION_SECONDS m_duration;
```

## <a name="ccustominterpolatorm_finalvalue"></a><a name="m_finalvalue"></a> Ккустоминтерполатор:: m_finalValue

Конечное значение переменной в конце перехода.

```
DOUBLE m_finalValue;
```

## <a name="ccustominterpolatorm_initialvalue"></a><a name="m_initialvalue"></a> Ккустоминтерполатор:: m_initialValue

Значение переменной в начале перехода.

```
DOUBLE m_initialValue;
```

## <a name="ccustominterpolatorm_initialvelocity"></a><a name="m_initialvelocity"></a> Ккустоминтерполатор:: m_initialVelocity

Скорость переменной в начале перехода.

```
DOUBLE m_initialVelocity;
```

## <a name="ccustominterpolatorsetduration"></a><a name="setduration"></a> Ккустоминтерполатор:: Сетдуратион

Задает длительность интерполяции.

```
virtual BOOL SetDuration(UI_ANIMATION_SECONDS duration);
```

### <a name="parameters"></a>Параметры

*duration*<br/>
Длительность перехода.

### <a name="return-value"></a>Возвращаемое значение

Базовая реализация всегда возвращает значение TRUE. Возвращает значение FALSE от переопределенной реализации, если требуется завершить событие.

## <a name="ccustominterpolatorsetinitialvalueandvelocity"></a><a name="setinitialvalueandvelocity"></a> Ккустоминтерполатор:: СетинитиалвалуеандвелоЦити

Задает начальное значение и скорость для интерполяции.

```
virtual BOOL SetInitialValueAndVelocity(
    DOUBLE initialValue,
    DOUBLE initialVelocity);
```

### <a name="parameters"></a>Параметры

*инитиалвалуе*<br/>
Значение переменной в начале перехода.

*InitialVelocity равно*<br/>
Скорость переменной в начале перехода.

### <a name="return-value"></a>Возвращаемое значение

Базовая реализация всегда возвращает значение TRUE. Возвращает значение FALSE от переопределенной реализации, если требуется завершить событие.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
