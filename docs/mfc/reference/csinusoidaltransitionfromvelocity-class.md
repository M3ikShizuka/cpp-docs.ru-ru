---
description: 'Дополнительные сведения о: КсинусоидалтранситионфромвелоЦити Class'
title: Класс CSinusoidalTransitionFromVelocity
ms.date: 11/04/2016
f1_keywords:
- CSinusoidalTransitionFromVelocity
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromVelocity
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromVelocity::CSinusoidalTransitionFromVelocity
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromVelocity::Create
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromVelocity::m_duration
- AFXANIMATIONCONTROLLER/CSinusoidalTransitionFromVelocity::m_period
helpviewer_keywords:
- CSinusoidalTransitionFromVelocity [MFC], CSinusoidalTransitionFromVelocity
- CSinusoidalTransitionFromVelocity [MFC], Create
- CSinusoidalTransitionFromVelocity [MFC], m_duration
- CSinusoidalTransitionFromVelocity [MFC], m_period
ms.assetid: cc885f17-b84b-45ee-8f1f-36a8bbb7adad
ms.openlocfilehash: 96f4a4c6343f3635f3b60480f49c5af6e6f1e089
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97342758"
---
# <a name="csinusoidaltransitionfromvelocity-class"></a>Класс CSinusoidalTransitionFromVelocity

Инкапсулирует переход с синусоидальной скоростью, амплитуда которого определяется начальной скоростью переменной анимации.

## <a name="syntax"></a>Синтаксис

```
class CSinusoidalTransitionFromVelocity : public CBaseTransition;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[КсинусоидалтранситионфромвелоЦити:: КсинусоидалтранситионфромвелоЦити](#csinusoidaltransitionfromvelocity)|Конструирует объект перехода.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[КсинусоидалтранситионфромвелоЦити:: Create](#create)|Вызывает библиотеку переходов для создания COM-объекта инкапсулированного перехода. (Переопределяет [CBaseTransition:: Create](../../mfc/reference/cbasetransition-class.md#create).)|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[КсинусоидалтранситионфромвелоЦити:: m_duration](#m_duration)|Длительность перехода.|
|[КсинусоидалтранситионфромвелоЦити:: m_period](#m_period)|Период колебаний синусоидальнойной волны в секундах.|

## <a name="remarks"></a>Комментарии

Значение переменной анимации осЦиллатес вокруг первоначального значения в течение всей продолжительности перехода синусоидальной Range. Амплитуда колебаний определяется скоростью переменной анимации при начале перехода. Так как все переходы очищаются автоматически, рекомендуется выделять их с помощью оператора New. Инкапсулированный COM-объект Иуианиматионтранситион создается методом Каниматионконтроллер:: Аниматеграуп, пока он не будет равен NULL. Изменение переменных-членов после создания этого объекта COM не имеет силы.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CBaseTransition](../../mfc/reference/cbasetransition-class.md)

[ксинусоидалтранситионфромвелоЦити](../../mfc/reference/csinusoidaltransitionfromvelocity-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="csinusoidaltransitionfromvelocitycreate"></a><a name="create"></a> КсинусоидалтранситионфромвелоЦити:: Create

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

## <a name="csinusoidaltransitionfromvelocitycsinusoidaltransitionfromvelocity"></a><a name="csinusoidaltransitionfromvelocity"></a> КсинусоидалтранситионфромвелоЦити:: КсинусоидалтранситионфромвелоЦити

Конструирует объект перехода.

```
CSinusoidalTransitionFromVelocity(
    UI_ANIMATION_SECONDS duration,
    UI_ANIMATION_SECONDS period);
```

### <a name="parameters"></a>Параметры

*duration*<br/>
Длительность перехода.

*периода*<br/>
Период колебаний синусоидальнойной волны в секундах.

## <a name="csinusoidaltransitionfromvelocitym_duration"></a><a name="m_duration"></a> КсинусоидалтранситионфромвелоЦити:: m_duration

Длительность перехода.

```
UI_ANIMATION_SECONDS m_duration;
```

## <a name="csinusoidaltransitionfromvelocitym_period"></a><a name="m_period"></a> КсинусоидалтранситионфромвелоЦити:: m_period

Период колебаний синусоидальнойной волны в секундах.

```
UI_ANIMATION_SECONDS m_period;
```

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
