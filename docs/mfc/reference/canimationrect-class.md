---
description: 'Дополнительные сведения о: Каниматионрект Class'
title: Класс CAnimationRect
ms.date: 11/04/2016
f1_keywords:
- CAnimationRect
- AFXANIMATIONCONTROLLER/CAnimationRect
- AFXANIMATIONCONTROLLER/CAnimationRect::CAnimationRect
- AFXANIMATIONCONTROLLER/CAnimationRect::AddTransition
- AFXANIMATIONCONTROLLER/CAnimationRect::GetBottom
- AFXANIMATIONCONTROLLER/CAnimationRect::GetDefaultValue
- AFXANIMATIONCONTROLLER/CAnimationRect::GetLeft
- AFXANIMATIONCONTROLLER/CAnimationRect::GetRight
- AFXANIMATIONCONTROLLER/CAnimationRect::GetTop
- AFXANIMATIONCONTROLLER/CAnimationRect::GetValue
- AFXANIMATIONCONTROLLER/CAnimationRect::SetDefaultValue
- AFXANIMATIONCONTROLLER/CAnimationRect::GetAnimationVariableList
- AFXANIMATIONCONTROLLER/CAnimationRect::m_bFixedSize
- AFXANIMATIONCONTROLLER/CAnimationRect::m_bottomValue
- AFXANIMATIONCONTROLLER/CAnimationRect::m_leftValue
- AFXANIMATIONCONTROLLER/CAnimationRect::m_rightValue
- AFXANIMATIONCONTROLLER/CAnimationRect::m_szInitial
- AFXANIMATIONCONTROLLER/CAnimationRect::m_topValue
helpviewer_keywords:
- CAnimationRect [MFC], CAnimationRect
- CAnimationRect [MFC], AddTransition
- CAnimationRect [MFC], GetBottom
- CAnimationRect [MFC], GetDefaultValue
- CAnimationRect [MFC], GetLeft
- CAnimationRect [MFC], GetRight
- CAnimationRect [MFC], GetTop
- CAnimationRect [MFC], GetValue
- CAnimationRect [MFC], SetDefaultValue
- CAnimationRect [MFC], GetAnimationVariableList
- CAnimationRect [MFC], m_bFixedSize
- CAnimationRect [MFC], m_bottomValue
- CAnimationRect [MFC], m_leftValue
- CAnimationRect [MFC], m_rightValue
- CAnimationRect [MFC], m_szInitial
- CAnimationRect [MFC], m_topValue
ms.assetid: 0294156d-241e-4a57-92b2-31234fe557d6
ms.openlocfilehash: 590b1382992a32e0eb3d49e0ea562d10193c1990
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97207895"
---
# <a name="canimationrect-class"></a>Класс CAnimationRect

Реализует функции прямоугольника, стороны которого могут быть анимированы.

## <a name="syntax"></a>Синтаксис

```
class CAnimationRect : public CAnimationBaseObject;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Каниматионрект:: Каниматионрект](#canimationrect)|Перегружен. Конструирует объект Rect анимации.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Каниматионрект:: Аддтранситион](#addtransition)|Добавляет переходы для левых, верхних, правых и нижних координат.|
|[Каниматионрект::/низ](#getbottom)|Предоставляет доступ к CAnimationVariable, представляющей нижнюю координату.|
|[Каниматионрект:: DefaultValue](#getdefaultvalue)|Возвращает значения по умолчанию для границ прямоугольника.|
|[Каниматионрект:: Left](#getleft)|Предоставляет доступ к CAnimationVariable, представляющим левую координату.|
|[Каниматионрект:: направо](#getright)|Предоставляет доступ к CAnimationVariable, представляющим правую координату.|
|[Каниматионрект:: GetTop](#gettop)|Предоставляет доступ к CAnimationVariable, представляющим верхнюю координату.|
|[Каниматионрект:: GetValue](#getvalue)|Возвращает текущее значение.|
|[Каниматионрект:: Сетдефаултвалуе](#setdefaultvalue)|Задает значение по умолчанию.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Каниматионрект:: Жетаниматионвариаблелист](#getanimationvariablelist)|Помещает переменные инкапсулированной анимации в список. (Переопределяет [каниматионбасеобжект:: жетаниматионвариаблелист](../../mfc/reference/canimationbaseobject-class.md#getanimationvariablelist).)|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Каниматионрект:: operator RECT](#operator_rect)|Преобразует Каниматионрект в RECT.|
|[Каниматионрект:: operator =](#operator_eq)|Присваивает Rect значение Каниматионрект.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Каниматионрект:: m_bFixedSize](#m_bfixedsize)|Указывает, имеет ли прямоугольник фиксированный размер.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Каниматионрект:: m_bottomValue](#m_bottomvalue)|Переменная инкапсулированной анимации, представляющая нижнюю границу прямоугольника анимации.|
|[Каниматионрект:: m_leftValue](#m_leftvalue)|Переменная инкапсулированной анимации, представляющая левую границу прямоугольника анимации.|
|[Каниматионрект:: m_rightValue](#m_rightvalue)|Переменная инкапсулированной анимации, представляющая правую границу прямоугольника анимации.|
|[Каниматионрект:: m_szInitial](#m_szinitial)|Задает начальный размер прямоугольника анимации.|
|[Каниматионрект:: m_topValue](#m_topvalue)|Переменная инкапсулированной анимации, представляющая верхнюю границу прямоугольника анимации.|

## <a name="remarks"></a>Комментарии

Класс Каниматионрект инкапсулирует четыре объекта CAnimationVariable и может представлять в приложениях прямоугольник. Чтобы использовать этот класс в приложении, просто создайте экземпляр объекта этого класса, добавьте его в контроллер анимации с помощью Каниматионконтроллер:: Адданиматионобжект и вызовите Аддтранситион, чтобы каждый переход был применен к левой, правой верхней и нижней координатам.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[каниматионбасеобжект](../../mfc/reference/canimationbaseobject-class.md)

`CAnimationRect`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationrectaddtransition"></a><a name="addtransition"></a> Каниматионрект:: Аддтранситион

Добавляет переходы для левых, верхних, правых и нижних координат.

```cpp
void AddTransition(
    CBaseTransition* pLeftTransition,
    CBaseTransition* pTopTransition,
    CBaseTransition* pRightTransition,
    CBaseTransition* pBottomTransition);
```

### <a name="parameters"></a>Параметры

*плефттранситион*<br/>
Указывает переход для левой части.

*птоптранситион*<br/>
Указывает переход для верхней стороны.

*пригхттранситион*<br/>
Указывает переход для правой части.

*пботтомтранситион*<br/>
Указывает переход для нижней части.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы добавить указанные переходы во внутренний список переходов, применяемых к переменным анимации для каждой стороны прямоугольника. При добавлении переходов они не применяются немедленно и хранятся во внутреннем списке. Переходы применяются (добавляются к раскадровке для конкретного значения) при вызове Каниматионконтроллер:: Аниматеграуп. Если не нужно применять переход к одной из прямоугольников, можно передать значение NULL.

## <a name="canimationrectcanimationrect"></a><a name="canimationrect"></a> Каниматионрект:: Каниматионрект

Конструирует объект Каниматионрект.

```
CAnimationRect();

CAnimationRect(
    const CRect& rect,
    UINT32 nGroupID,
    UINT32 nObjectID = (UINT32)-1,
    DWORD dwUserData = 0);

CAnimationRect(
    const CPoint& pt,
    const CSize& sz,
    UINT32 nGroupID,
    UINT32 nObjectID = (UINT32)-1,
    DWORD dwUserData = 0);

CAnimationRect(
    int nLeft,
    int nTop,
    int nRight,
    int nBottom,
    UINT32 nGroupID,
    UINT32 nObjectID = (UINT32)-1,
    DWORD dwUserData = 0);
```

### <a name="parameters"></a>Параметры

*rect*<br/>
Задает прямоугольник по умолчанию.

*нграупид*<br/>
Указывает идентификатор группы.

*нобжектид*<br/>
Указывает идентификатор объекта.

*двусердата*<br/>
Указывает определяемые пользователем данные.

*пт*<br/>
Координата верхнего левого угла.

*SZ*<br/>
Размер прямоугольника.

*нлефт*<br/>
Задает координату левой границы.

*нтоп*<br/>
Задает координату верхней границы.

*нригхт*<br/>
Задает координату правой границы.

*нботтом*<br/>
Задает координату нижней границы.

### <a name="remarks"></a>Комментарии

Объект создается со значениями по умолчанию для левого, верхнего, правого и нижнего, идентификатора объекта и группы, для которых будет задано значение 0. Их можно изменить позже во время выполнения с помощью Сетдефаултвалуе и Сетид.

## <a name="canimationrectgetanimationvariablelist"></a><a name="getanimationvariablelist"></a> Каниматионрект:: Жетаниматионвариаблелист

Помещает переменные инкапсулированной анимации в список.

```
virtual void GetAnimationVariableList(
    CList<CAnimationVariable*,
    CAnimationVariable*>& lst);
```

### <a name="parameters"></a>Параметры

*LST*<br/>
При возврате функции она содержит указатели на четыре объекта CAnimationVariable, представляющие координаты прямоугольника.

## <a name="canimationrectgetbottom"></a><a name="getbottom"></a> Каниматионрект::/низ

Предоставляет доступ к CAnimationVariable, представляющей нижнюю координату.

```
CAnimationVariable& GetBottom();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на инкапсулированный CAnimationVariable, представляющий нижнюю координату.

### <a name="remarks"></a>Комментарии

Этот метод можно вызвать для получения прямого доступа к базовым CAnimationVariable, представляющим нижнюю координату.

## <a name="canimationrectgetdefaultvalue"></a><a name="getdefaultvalue"></a> Каниматионрект:: DefaultValue

Возвращает значения по умолчанию для границ прямоугольника.

```
CRect GetDefaultValue();
```

### <a name="return-value"></a>Возвращаемое значение

Значение Крект, содержащее значения по умолчанию слева, справа, сверху и снизу.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы получить значение по умолчанию, которое было ранее задано конструктором или Сетдефаултвалуе.

## <a name="canimationrectgetleft"></a><a name="getleft"></a> Каниматионрект:: Left

Предоставляет доступ к CAnimationVariable, представляющим левую координату.

```
CAnimationVariable& GetLeft();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на инкапсулированный CAnimationVariable, представляющий левую координату.

### <a name="remarks"></a>Комментарии

Этот метод можно вызвать для получения прямого доступа к базовым CAnimationVariable, представляющим левую координату.

## <a name="canimationrectgetright"></a><a name="getright"></a> Каниматионрект:: направо

Предоставляет доступ к CAnimationVariable, представляющим правую координату.

```
CAnimationVariable& GetRight();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на инкапсулированный CAnimationVariable, представляющий правую координату.

### <a name="remarks"></a>Комментарии

Этот метод можно вызвать для получения прямого доступа к базовому CAnimationVariable, представляющему правильную координату.

## <a name="canimationrectgettop"></a><a name="gettop"></a> Каниматионрект:: GetTop

Предоставляет доступ к CAnimationVariable, представляющим верхнюю координату.

```
CAnimationVariable& GetTop();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на инкапсулированный CAnimationVariable, представляющий верхнюю координату.

### <a name="remarks"></a>Комментарии

Этот метод можно вызвать для получения прямого доступа к базовому CAnimationVariable, представляющему верхнюю координату.

## <a name="canimationrectgetvalue"></a><a name="getvalue"></a> Каниматионрект:: GetValue

Возвращает текущее значение.

```
BOOL GetValue(CRect& rect);
```

### <a name="parameters"></a>Параметры

*rect*<br/>
Выходные данные. Содержит текущее значение при возврате из метода.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если текущее значение было успешно получено; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы получить текущее значение прямоугольника анимации. Если этот метод завершается ошибкой или базовые COM-объекты слева, сверху, справа и снизу не инициализированы, параметр rect содержит значение по умолчанию, которое ранее было задано в конструкторе или Сетдефаултвалуе.

## <a name="canimationrectm_bfixedsize"></a><a name="m_bfixedsize"></a> Каниматионрект:: m_bFixedSize

Указывает, имеет ли прямоугольник фиксированный размер.

```
BOOL m_bFixedSize;
```

### <a name="remarks"></a>Комментарии

Если этот член имеет значение true, то размер прямоугольника фиксирован, а значения right и Bottom пересчитываются каждый раз, когда верхний левый угол перемещается в соответствии с фиксированным размером. Задайте для этого параметра значение TRUE, чтобы легко перемещать прямоугольник вокруг экрана. В этом случае переходы, примененные к правой и нижней координатам, игнорируются. Размер хранится внутренне при создании объекта и/или вызове Сетдефаултвалуе. По умолчанию для этого элемента задано значение FALSE.

## <a name="canimationrectm_bottomvalue"></a><a name="m_bottomvalue"></a> Каниматионрект:: m_bottomValue

Переменная инкапсулированной анимации, представляющая нижнюю границу прямоугольника анимации.

```
CAnimationVariable m_bottomValue;
```

## <a name="canimationrectm_leftvalue"></a><a name="m_leftvalue"></a> Каниматионрект:: m_leftValue

Переменная инкапсулированной анимации, представляющая левую границу прямоугольника анимации.

```
CAnimationVariable m_leftValue;
```

## <a name="canimationrectm_rightvalue"></a><a name="m_rightvalue"></a> Каниматионрект:: m_rightValue

Переменная инкапсулированной анимации, представляющая правую границу прямоугольника анимации.

```
CAnimationVariable m_rightValue;
```

## <a name="canimationrectm_szinitial"></a><a name="m_szinitial"></a> Каниматионрект:: m_szInitial

Задает начальный размер прямоугольника анимации.

```
CSize m_szInitial;
```

## <a name="canimationrectm_topvalue"></a><a name="m_topvalue"></a> Каниматионрект:: m_topValue

Переменная инкапсулированной анимации, представляющая верхнюю границу прямоугольника анимации.

```
CAnimationVariable m_topValue;
```

## <a name="canimationrectoperator-rect"></a><a name="operator_rect"></a> Каниматионрект:: operator RECT

Преобразует Каниматионрект в RECT.

```
operator RECT();
```

### <a name="return-value"></a>Возвращаемое значение

Текущее значение прямоугольника анимации в качестве RECT.

### <a name="remarks"></a>Комментарии

Эта функция внутренне вызывает метод GetValue. Если по какой бы то ни было причине не удается выполнить GetValue, возвращаемый RECT будет содержать значения по умолчанию для всех координат прямоугольника.

## <a name="canimationrectoperator"></a><a name="operator_eq"></a> Каниматионрект:: operator =

Присваивает Rect значение Каниматионрект.

```cpp
void operator=(const RECT& rect);
```

### <a name="parameters"></a>Параметры

*rect*<br/>
Новое значение прямоугольника анимации.

### <a name="remarks"></a>Комментарии

Рекомендуется сделать это перед началом анимации, так как этот оператор вызывает Сетдефаултвалуе, который повторно создает базовые COM-объекты для цветовых компонентов, если они были созданы. Если вы подписаны на этот объект анимации на события (ValueChanged или Интежервалуечанжед), необходимо повторно включить эти события.

## <a name="canimationrectsetdefaultvalue"></a><a name="setdefaultvalue"></a> Каниматионрект:: Сетдефаултвалуе

Задает значение по умолчанию.

```cpp
void SetDefaultValue(const CRect& rect);
```

### <a name="parameters"></a>Параметры

*rect*<br/>
Указывает новые значения по умолчанию для левого, верхнего, правого и нижнего.

### <a name="remarks"></a>Комментарии

Эта функция используется для задания значения по умолчанию для объекта анимации. Этот метод присваивает значения по умолчанию границам прямоугольника. Он также повторно создает базовые COM-объекты, если они были созданы. Если вы подписаны на этот объект анимации на события (ValueChanged или Интежервалуечанжед), необходимо повторно включить эти события.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
