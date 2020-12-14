---
description: 'Дополнительные сведения о: Ккубиктранситион Class'
title: Класс CCubicTransition
ms.date: 11/04/2016
f1_keywords:
- CCubicTransition
- AFXANIMATIONCONTROLLER/CCubicTransition
- AFXANIMATIONCONTROLLER/CCubicTransition::CCubicTransition
- AFXANIMATIONCONTROLLER/CCubicTransition::Create
- AFXANIMATIONCONTROLLER/CCubicTransition::m_dblFinalValue
- AFXANIMATIONCONTROLLER/CCubicTransition::m_dblFinalVelocity
- AFXANIMATIONCONTROLLER/CCubicTransition::m_duration
helpviewer_keywords:
- CCubicTransition [MFC], CCubicTransition
- CCubicTransition [MFC], Create
- CCubicTransition [MFC], m_dblFinalValue
- CCubicTransition [MFC], m_dblFinalVelocity
- CCubicTransition [MFC], m_duration
ms.assetid: 4fc30e9c-160c-45e1-bdbe-51adf8fee9c5
ms.openlocfilehash: 2e83aa10e013595c80a87b5d79cddf80bc46b6ac
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227784"
---
# <a name="ccubictransition-class"></a>Класс CCubicTransition

Инкапсулирует кубический переход.

## <a name="syntax"></a>Синтаксис

```
class CCubicTransition : public CBaseTransition;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккубиктранситион:: Ккубиктранситион](#ccubictransition)|Создает объект перехода и инициализирует его параметры.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккубиктранситион:: Create](#create)|Вызывает библиотеку переходов для создания COM-объекта инкапсулированного перехода. (Переопределяет [CBaseTransition:: Create](../../mfc/reference/cbasetransition-class.md#create).)|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Ккубиктранситион:: m_dblFinalValue](#m_dblfinalvalue)|Значение переменной анимации в конце перехода.|
|[Ккубиктранситион:: m_dblFinalVelocity](#m_dblfinalvelocity)|Скорость переменной в конце перехода.|
|[Ккубиктранситион:: m_duration](#m_duration)|Длительность перехода.|

## <a name="remarks"></a>Комментарии

Во время перехода в кубический куб значение переменной анимации меняется с начального на заданное конечное значение на время перехода, заканчивая на указанную скорость. Так как все переходы очищаются автоматически, рекомендуется выделять их с помощью оператора New. Инкапсулированный COM-объект Иуианиматионтранситион создается методом Каниматионконтроллер:: Аниматеграуп, пока он не будет равен NULL. Изменение переменных-членов после создания этого объекта COM не имеет силы.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CBaseTransition](../../mfc/reference/cbasetransition-class.md)

`CCubicTransition`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="ccubictransitionccubictransition"></a><a name="ccubictransition"></a> Ккубиктранситион:: Ккубиктранситион

Создает объект перехода и инициализирует его параметры.

```
CCubicTransition(
    UI_ANIMATION_SECONDS duration,
    DOUBLE finalValue,
    DOUBLE finalVelocity);
```

### <a name="parameters"></a>Параметры

*duration*<br/>
Длительность перехода.

*финалвалуе*<br/>
Значение переменной анимации в конце перехода.

*финалвелоЦити*<br/>
Скорость переменной в конце перехода.

## <a name="ccubictransitioncreate"></a><a name="create"></a> Ккубиктранситион:: Create

Вызывает библиотеку переходов для создания COM-объекта инкапсулированного перехода.

```
virtual BOOL Create(
    IUIAnimationTransitionLibrary* pLibrary,
    IUIAnimationTransitionFactory* \*not used*\);
```

### <a name="parameters"></a>Параметры

*плибрари*<br/>
Указатель на [интерфейс иуианиматионтранситионлибрари](/windows/win32/api/uianimation/nn-uianimation-iuianimationtransitionlibrary), который определяет библиотеку стандартных переходов.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если переход успешно создан; в противном случае — FALSE.

## <a name="ccubictransitionm_dblfinalvalue"></a><a name="m_dblfinalvalue"></a> Ккубиктранситион:: m_dblFinalValue

Значение переменной анимации в конце перехода.

```
DOUBLE m_dblFinalValue;
```

## <a name="ccubictransitionm_dblfinalvelocity"></a><a name="m_dblfinalvelocity"></a> Ккубиктранситион:: m_dblFinalVelocity

Скорость переменной в конце перехода.

```
DOUBLE m_dblFinalVelocity;
```

## <a name="ccubictransitionm_duration"></a><a name="m_duration"></a> Ккубиктранситион:: m_duration

Длительность перехода.

```
UI_ANIMATION_SECONDS m_duration;
```

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
