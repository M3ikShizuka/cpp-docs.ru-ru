---
description: 'Дополнительные сведения о: Ксинусоидалтранситионфромранже Class'
title: Класс CSinusoidalTransitionFromRange
ms.date: 11/04/2016
f1_keywords:
- CSinusoidalTransitionFromRange
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromRange
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromRange::CSinusoidalTransitionFromRange
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromRange::Create
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromRange::m_dblMaximumValue
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromRange::m_dblMinimumValue
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromRange::m_duration
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromRange::m_period
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromRange::m_slope
helpviewer_keywords:
- CSinusoidalTransitionFromRange [MFC], CSinusoidalTransitionFromRange
- CSinusoidalTransitionFromRange [MFC], Create
- CSinusoidalTransitionFromRange [MFC], m_dblMaximumValue
- CSinusoidalTransitionFromRange [MFC], m_dblMinimumValue
- CSinusoidalTransitionFromRange [MFC], m_duration
- CSinusoidalTransitionFromRange [MFC], m_period
- CSinusoidalTransitionFromRange [MFC], m_slope
ms.assetid: 8b66a729-5f10-431a-b055-e3600d0065da
ms.openlocfilehash: 5d00b1cbfb8fe9b76a5a69bd1c9f10316ddf8141
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97264574"
---
# <a name="csinusoidaltransitionfromrange-class"></a>Класс CSinusoidalTransitionFromRange

Инкапсулирует переход в диапазоне синусоиды с заданной амплитудой колебаний.

## <a name="syntax"></a>Синтаксис

```
class CSinusoidalTransitionFromRange : public CBaseTransition;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ксинусоидалтранситионфромранже:: Ксинусоидалтранситионфромранже](#csinusoidaltransitionfromrange)|Конструирует объект перехода.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксинусоидалтранситионфромранже:: Create](#create)|Вызывает библиотеку переходов для создания COM-объекта инкапсулированного перехода. (Переопределяет [CBaseTransition:: Create](../../mfc/reference/cbasetransition-class.md#create).)|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Ксинусоидалтранситионфромранже:: m_dblMaximumValue](#m_dblmaximumvalue)|Значение переменной анимации в пиковую синусоидальной волна.|
|[Ксинусоидалтранситионфромранже:: m_dblMinimumValue](#m_dblminimumvalue)|Значение переменной анимации в траугх волны синусоидальной.|
|[Ксинусоидалтранситионфромранже:: m_duration](#m_duration)|Длительность перехода.|
|[Ксинусоидалтранситионфромранже:: m_period](#m_period)|Период колебаний синусоидальнойной волны в секундах.|
|[Ксинусоидалтранситионфромранже:: m_slope](#m_slope)|Наклон в начале перехода.|

## <a name="remarks"></a>Комментарии

Значение переменной анимации меняется между указанными минимальным и максимальным значениями в течение всей продолжительности перехода синусоидальной Range. Параметр наклона используется для устранения неоднозначности между двумя возможными синусами, заданными другими параметрами. Так как все переходы очищаются автоматически, рекомендуется выделять их с помощью оператора New. Инкапсулированный COM-объект Иуианиматионтранситион создается методом Каниматионконтроллер:: Аниматеграуп, пока он не будет равен NULL. Изменение переменных-членов после создания этого объекта COM не имеет силы.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CBaseTransition](../../mfc/reference/cbasetransition-class.md)

[ксинусоидалтранситионфромранже](../../mfc/reference/csinusoidaltransitionfromrange-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="csinusoidaltransitionfromrangecreate"></a><a name="create"></a> Ксинусоидалтранситионфромранже:: Create

Вызывает библиотеку переходов для создания COM-объекта инкапсулированного перехода.

```
virtual BOOL Create(
    IUIAnimationTransitionLibrary* pLibrary,
    IUIAnimationTransitionFactory* \*not used*\);
```

### <a name="parameters"></a>Параметры

*плибрари*<br/>
Указатель на библиотеку переходов, который отвечает за создание стандартных переходов.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если переход успешно создан; в противном случае — FALSE.

## <a name="csinusoidaltransitionfromrangecsinusoidaltransitionfromrange"></a><a name="csinusoidaltransitionfromrange"></a> Ксинусоидалтранситионфромранже:: Ксинусоидалтранситионфромранже

Конструирует объект перехода.

```
CSinusoidalTransitionFromRange(
    UI_ANIMATION_SECONDS duration,
    DOUBLE dblMinimumValue,
    DOUBLE dblMaximumValue,
    UI_ANIMATION_SECONDS period,
    UI_ANIMATION_SLOPE slope);
```

### <a name="parameters"></a>Параметры

*duration*<br/>
Длительность перехода.

*дблминимумвалуе*<br/>
Значение переменной анимации в траугх волны синусоидальной.

*дблмаксимумвалуе*<br/>
Значение переменной анимации в пиковую синусоидальной волна.

*периода*<br/>
Период колебаний синусоидальнойной волны в секундах.

*slope*<br/>
Наклон в начале перехода.

## <a name="csinusoidaltransitionfromrangem_dblmaximumvalue"></a><a name="m_dblmaximumvalue"></a> Ксинусоидалтранситионфромранже:: m_dblMaximumValue

Значение переменной анимации в пиковую синусоидальной волна.

```
DOUBLE m_dblMaximumValue;
```

## <a name="csinusoidaltransitionfromrangem_dblminimumvalue"></a><a name="m_dblminimumvalue"></a> Ксинусоидалтранситионфромранже:: m_dblMinimumValue

Значение переменной анимации в траугх волны синусоидальной.

```
DOUBLE m_dblMinimumValue;
```

## <a name="csinusoidaltransitionfromrangem_duration"></a><a name="m_duration"></a> Ксинусоидалтранситионфромранже:: m_duration

Длительность перехода.

```
UI_ANIMATION_SECONDS m_duration;
```

## <a name="csinusoidaltransitionfromrangem_period"></a><a name="m_period"></a> Ксинусоидалтранситионфромранже:: m_period

Период колебаний синусоидальнойной волны в секундах.

```
UI_ANIMATION_SECONDS m_period;
```

## <a name="csinusoidaltransitionfromrangem_slope"></a><a name="m_slope"></a> Ксинусоидалтранситионфромранже:: m_slope

Наклон в начале перехода.

```
UI_ANIMATION_SLOPE m_slope;
```

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
