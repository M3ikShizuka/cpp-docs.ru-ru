---
description: 'Дополнительные сведения о: Кпараболиктранситионфромакцелератион Class'
title: Класс CParabolicTransitionFromAcceleration
ms.date: 11/04/2016
f1_keywords:
- CParabolicTransitionFromAcceleration
- AFXANIMATIONCONTROLLER/CParabolicTransitionFromAcceleration
- AFXANIMATIONCONTROLLER/CParabolicTransitionFromAcceleration::CParabolicTransitionFromAcceleration
- AFXANIMATIONCONTROLLER/CParabolicTransitionFromAcceleration::Create
- AFXANIMATIONCONTROLLER/CParabolicTransitionFromAcceleration::m_dblAcceleration
- AFXANIMATIONCONTROLLER/CParabolicTransitionFromAcceleration::m_dblFinalValue
- AFXANIMATIONCONTROLLER/CParabolicTransitionFromAcceleration::m_dblFinalVelocity
helpviewer_keywords:
- CParabolicTransitionFromAcceleration [MFC], CParabolicTransitionFromAcceleration
- CParabolicTransitionFromAcceleration [MFC], Create
- CParabolicTransitionFromAcceleration [MFC], m_dblAcceleration
- CParabolicTransitionFromAcceleration [MFC], m_dblFinalValue
- CParabolicTransitionFromAcceleration [MFC], m_dblFinalVelocity
ms.assetid: 1e59b86f-358b-4da0-a4fd-8eaf5e85e00f
ms.openlocfilehash: 037c2ff8391b655c556339547966b14ee094fee0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97301494"
---
# <a name="cparabolictransitionfromacceleration-class"></a>Класс CParabolicTransitionFromAcceleration

Инкапсулирует переход с параболическим ускорением.

## <a name="syntax"></a>Синтаксис

```
class CParabolicTransitionFromAcceleration : public CBaseTransition;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кпараболиктранситионфромакцелератион:: Кпараболиктранситионфромакцелератион](#cparabolictransitionfromacceleration)|Создает переход параболическим-Acceleration и инициализирует его с указанными параметрами.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кпараболиктранситионфромакцелератион:: Create](#create)|Вызывает библиотеку переходов для создания COM-объекта инкапсулированного перехода. (Переопределяет [CBaseTransition:: Create](../../mfc/reference/cbasetransition-class.md#create).)|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Кпараболиктранситионфромакцелератион:: m_dblAcceleration](#m_dblacceleration)|Ускорение переменной анимации во время перехода.|
|[Кпараболиктранситионфромакцелератион:: m_dblFinalValue](#m_dblfinalvalue)|Значение переменной анимации в конце перехода.|
|[Кпараболиктранситионфромакцелератион:: m_dblFinalVelocity](#m_dblfinalvelocity)|Скорость переменной анимации в конце перехода.|

## <a name="remarks"></a>Комментарии

При переходе параболическим-Acceleration значение переменной анимации меняется с начального на конечное значение, завершающееся с указанной скоростью. Можно контролировать, насколько быстро переменная достигает конечного значения, указывая скорость ускорения. Так как все переходы очищаются автоматически, рекомендуется выделять их с помощью оператора New. Инкапсулированный COM-объект Иуианиматионтранситион создается методом Каниматионконтроллер:: Аниматеграуп, пока он не будет равен NULL. Изменение переменных-членов после создания этого объекта COM не имеет силы.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CBaseTransition](../../mfc/reference/cbasetransition-class.md)

[кпараболиктранситионфромакцелератион](../../mfc/reference/cparabolictransitionfromacceleration-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="cparabolictransitionfromaccelerationcparabolictransitionfromacceleration"></a><a name="cparabolictransitionfromacceleration"></a> Кпараболиктранситионфромакцелератион:: Кпараболиктранситионфромакцелератион

Создает переход параболическим-Acceleration и инициализирует его с указанными параметрами.

```
CParabolicTransitionFromAcceleration(
    DOUBLE dblFinalValue,
    DOUBLE dblFinalVelocity,
    DOUBLE dblAcceleration);
```

### <a name="parameters"></a>Параметры

*дблфиналвалуе*<br/>
Значение переменной анимации в конце перехода.

*дблфиналвелоЦити*<br/>
Скорость переменной анимации в конце перехода.

*дблакцелератион*<br/>
Ускорение переменной анимации во время перехода.

## <a name="cparabolictransitionfromaccelerationcreate"></a><a name="create"></a> Кпараболиктранситионфромакцелератион:: Create

Вызывает библиотеку переходов для создания COM-объекта инкапсулированного перехода.

```
virtual BOOL Create(
    IUIAnimationTransitionLibrary* pLibrary,
    IUIAnimationTransitionFactory* /* not used */);
```

### <a name="parameters"></a>Параметры

*плибрари*<br/>
Указатель на библиотеку переходов, который отвечает за создание стандартных переходов.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если переход успешно создан; в противном случае — FALSE.

## <a name="cparabolictransitionfromaccelerationm_dblacceleration"></a><a name="m_dblacceleration"></a> Кпараболиктранситионфромакцелератион:: m_dblAcceleration

Ускорение переменной анимации во время перехода.

```
DOUBLE m_dblAcceleration;
```

## <a name="cparabolictransitionfromaccelerationm_dblfinalvalue"></a><a name="m_dblfinalvalue"></a> Кпараболиктранситионфромакцелератион:: m_dblFinalValue

Значение переменной анимации в конце перехода.

```
DOUBLE m_dblFinalValue;
```

## <a name="cparabolictransitionfromaccelerationm_dblfinalvelocity"></a><a name="m_dblfinalvelocity"></a> Кпараболиктранситионфромакцелератион:: m_dblFinalVelocity

Скорость переменной анимации в конце перехода.

```
DOUBLE m_dblFinalVelocity;
```

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
