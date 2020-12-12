---
description: 'Дополнительные сведения о: Каниматионколор Class'
title: Класс CAnimationColor
ms.date: 11/04/2016
f1_keywords:
- CAnimationColor
- AFXANIMATIONCONTROLLER/CAnimationColor
- AFXANIMATIONCONTROLLER/CAnimationColor::CAnimationColor
- AFXANIMATIONCONTROLLER/CAnimationColor::AddTransition
- AFXANIMATIONCONTROLLER/CAnimationColor::GetB
- AFXANIMATIONCONTROLLER/CAnimationColor::GetDefaultValue
- AFXANIMATIONCONTROLLER/CAnimationColor::GetG
- AFXANIMATIONCONTROLLER/CAnimationColor::GetR
- AFXANIMATIONCONTROLLER/CAnimationColor::GetValue
- AFXANIMATIONCONTROLLER/CAnimationColor::SetDefaultValue
- AFXANIMATIONCONTROLLER/CAnimationColor::GetAnimationVariableList
- AFXANIMATIONCONTROLLER/CAnimationColor::m_bValue
- AFXANIMATIONCONTROLLER/CAnimationColor::m_gValue
- AFXANIMATIONCONTROLLER/CAnimationColor::m_rValue
helpviewer_keywords:
- CAnimationColor [MFC], CAnimationColor
- CAnimationColor [MFC], AddTransition
- CAnimationColor [MFC], GetB
- CAnimationColor [MFC], GetDefaultValue
- CAnimationColor [MFC], GetG
- CAnimationColor [MFC], GetR
- CAnimationColor [MFC], GetValue
- CAnimationColor [MFC], SetDefaultValue
- CAnimationColor [MFC], GetAnimationVariableList
- CAnimationColor [MFC], m_bValue
- CAnimationColor [MFC], m_gValue
- CAnimationColor [MFC], m_rValue
ms.assetid: 88bfabd4-efeb-4652-87e8-304253d8e48c
ms.openlocfilehash: 430f017bc9d60eed5e2d42b71f0303546deecaca
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318641"
---
# <a name="canimationcolor-class"></a>Класс CAnimationColor

Реализует функции цвета, красный, зеленый и синий компоненты которого могут быть анимированы.

## <a name="syntax"></a>Синтаксис

```
class CAnimationColor : public CAnimationBaseObject;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Каниматионколор:: Каниматионколор](#canimationcolor)|Перегружен. Конструирует объект цвета анимации.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Каниматионколор:: Аддтранситион](#addtransition)|Добавляет переходы для красного, зеленого и синего компонентов.|
|[Каниматионколор:: Жетб](#getb)|Предоставляет доступ к CAnimationVariable, представляющему синий компонент.|
|[Каниматионколор:: DefaultValue](#getdefaultvalue)|Возвращает значения по умолчанию для цветовых компонентов.|
|[Каниматионколор:: Жетг](#getg)|Предоставляет доступ к CAnimationVariable, представляющему зеленый компонент.|
|[Каниматионколор:: Жетр](#getr)|Предоставляет доступ к CAnimationVariable, представляющему красный компонент.|
|[Каниматионколор:: GetValue](#getvalue)|Возвращает текущее значение.|
|[Каниматионколор:: Сетдефаултвалуе](#setdefaultvalue)|Задает значение по умолчанию.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Каниматионколор:: Жетаниматионвариаблелист](#getanimationvariablelist)|Помещает переменные инкапсулированной анимации в список. (Переопределяет [каниматионбасеобжект:: жетаниматионвариаблелист](../../mfc/reference/canimationbaseobject-class.md#getanimationvariablelist).)|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Каниматионколор:: operator COLORREF](#operator_colorref)||
|[Каниматионколор:: operator =](#operator_eq)|Присваивает цвет Каниматионколор.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Каниматионколор:: m_bValue](#m_bvalue)|Переменная инкапсулированной анимации, представляющая синий компонент цвета анимации.|
|[Каниматионколор:: m_gValue](#m_gvalue)|Переменная инкапсулированной анимации, представляющая зеленый компонент цвета анимации.|
|[Каниматионколор:: m_rValue](#m_rvalue)|Переменная инкапсулированной анимации, представляющая красный компонент цвета анимации.|

## <a name="remarks"></a>Комментарии

Класс Каниматионколор инкапсулирует три объекта CAnimationVariable и может представлять в приложениях цвет. Например, этот класс можно использовать для анимации цветов любого объекта на экране (например, цвет текста, цвет фона и т. д.). Чтобы использовать этот класс в приложении, просто создайте экземпляр объекта этого класса, добавьте его в контроллер анимации с помощью Каниматионконтроллер:: Адданиматионобжект и вызовите Аддтранситион, чтобы каждый переход был применен к красному, зеленому и синему компонентам.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[каниматионбасеобжект](../../mfc/reference/canimationbaseobject-class.md)

`CAnimationColor`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationcoloraddtransition"></a><a name="addtransition"></a> Каниматионколор:: Аддтранситион

Добавляет переходы для красного, зеленого и синего компонентов.

```cpp
void AddTransition(
    CBaseTransition* pRTransition,
    CBaseTransition* pGTransition,
    CBaseTransition* pBTransition);
```

### <a name="parameters"></a>Параметры

*пртранситион*<br/>
Переход на красный компонент.

*пгтранситион*<br/>
Переход на зеленый компонент.

*пбтранситион*<br/>
Переход для синего компонента.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы добавить указанные переходы во внутренний список переходов для применения к переменным анимации, представляющим цветовые компоненты. При добавлении переходов они не применяются немедленно и хранятся во внутреннем списке. Переходы применяются (добавляются к раскадровке для конкретного значения) при вызове Каниматионконтроллер:: Аниматеграуп. Если не нужно применять переход к одному из компонентов цвета, можно передать значение NULL.

## <a name="canimationcolorcanimationcolor"></a><a name="canimationcolor"></a> Каниматионколор:: Каниматионколор

Конструирует объект Каниматионколор.

```
CAnimationColor();

CAnimationColor(
    COLORREF color,
    UINT32 nGroupID,
    UINT32 nObjectID = (UINT32)-1,
    DWORD dwUserData = 0);
```

### <a name="parameters"></a>Параметры

*color*<br/>
Задает цвет по умолчанию.

*нграупид*<br/>
Указывает идентификатор группы.

*нобжектид*<br/>
Указывает идентификатор объекта.

*двусердата*<br/>
Указывает определяемые пользователем данные.

### <a name="remarks"></a>Комментарии

Объект создается со значениями по умолчанию красного, зеленого, синего, идентификатора объекта и группы, для которых будет задано значение 0. Их можно изменить позже во время выполнения с помощью Сетдефаултвалуе и Сетид.

## <a name="canimationcolorgetanimationvariablelist"></a><a name="getanimationvariablelist"></a> Каниматионколор:: Жетаниматионвариаблелист

Помещает переменные инкапсулированной анимации в список.

```
virtual void GetAnimationVariableList(CList<CAnimationVariable*>& lst);
```

### <a name="parameters"></a>Параметры

*LST*<br/>
При возврате функции она содержит указатели на три объекта CAnimationVariable, представляющие красные, зеленые и синие компоненты.

## <a name="canimationcolorgetb"></a><a name="getb"></a> Каниматионколор:: Жетб

Предоставляет доступ к CAnimationVariable, представляющему синий компонент.

```
CAnimationVariable& GetB();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на инкапсулированный CAnimationVariable, представляющий синий компонент.

### <a name="remarks"></a>Комментарии

Этот метод можно вызвать для получения прямого доступа к базовому CAnimationVariable, представляющему синий компонент.

## <a name="canimationcolorgetdefaultvalue"></a><a name="getdefaultvalue"></a> Каниматионколор:: DefaultValue

Возвращает значения по умолчанию для цветовых компонентов.

```
COLORREF GetDefaultValue();
```

### <a name="return-value"></a>Возвращаемое значение

Значение COLORREF, содержащее значения по умолчанию для компонентов RGB.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы получить значение по умолчанию, которое было ранее задано конструктором или Сетдефаултвалуе.

## <a name="canimationcolorgetg"></a><a name="getg"></a> Каниматионколор:: Жетг

Предоставляет доступ к CAnimationVariable, представляющему зеленый компонент.

```
CAnimationVariable& GetG();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на инкапсулированный CAnimationVariable, представляющий зеленый компонент.

### <a name="remarks"></a>Комментарии

Этот метод можно вызвать для получения прямого доступа к базовым CAnimationVariable, представляющим зеленый компонент.

## <a name="canimationcolorgetr"></a><a name="getr"></a> Каниматионколор:: Жетр

Предоставляет доступ к CAnimationVariable, представляющему красный компонент.

```
CAnimationVariable& GetR();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на инкапсулированный CAnimationVariable, представляющий красный компонент.

### <a name="remarks"></a>Комментарии

Этот метод можно вызвать для получения прямого доступа к базовым CAnimationVariable, представляющим красный компонент.

## <a name="canimationcolorgetvalue"></a><a name="getvalue"></a> Каниматионколор:: GetValue

Возвращает текущее значение.

```
BOOL GetValue(COLORREF& color);
```

### <a name="parameters"></a>Параметры

*color*<br/>
Выходные данные. Содержит текущее значение при возврате из метода.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если текущее значение было успешно получено; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы получить текущее значение цвета анимации. Если этот метод завершается ошибкой или базовые COM-объекты для цветовых компонентов не были инициализированы, Color содержит значение по умолчанию, которое ранее было задано в конструкторе или Сетдефаултвалуе.

## <a name="canimationcolorm_bvalue"></a><a name="m_bvalue"></a> Каниматионколор:: m_bValue

Переменная инкапсулированной анимации, представляющая синий компонент цвета анимации.

```
CAnimationVariable m_bValue;
```

## <a name="canimationcolorm_gvalue"></a><a name="m_gvalue"></a> Каниматионколор:: m_gValue

Переменная инкапсулированной анимации, представляющая зеленый компонент цвета анимации.

```
CAnimationVariable m_gValue;
```

## <a name="canimationcolorm_rvalue"></a><a name="m_rvalue"></a> Каниматионколор:: m_rValue

Переменная инкапсулированной анимации, представляющая красный компонент цвета анимации.

```
CAnimationVariable m_rValue;
```

## <a name="canimationcoloroperator-colorref"></a><a name="operator_colorref"></a> Каниматионколор:: operator COLORREF

```
operator COLORREF();
```

### <a name="return-value"></a>Возвращаемое значение

## <a name="canimationcoloroperator"></a><a name="operator_eq"></a> Каниматионколор:: operator =

Присваивает цвет Каниматионколор.

```cpp
void operator=(COLORREF color);
```

### <a name="parameters"></a>Параметры

*color*<br/>
Задает цвет анимации нового значения.

### <a name="remarks"></a>Комментарии

Рекомендуется сделать это перед началом анимации, так как этот оператор вызывает Сетдефаултвалуе, который повторно создает базовые COM-объекты для цветовых компонентов, если они были созданы. Если вы подписаны на этот объект анимации на события (ValueChanged или Интежервалуечанжед), необходимо повторно включить эти события.

## <a name="canimationcolorsetdefaultvalue"></a><a name="setdefaultvalue"></a> Каниматионколор:: Сетдефаултвалуе

Задает значение по умолчанию.

```cpp
void SetDefaultValue(COLORREF color);
```

### <a name="parameters"></a>Параметры

*color*<br/>
Указывает новые значения по умолчанию для красного, зеленого и синего компонентов.

### <a name="remarks"></a>Комментарии

Эта функция используется для задания значения по умолчанию для объекта анимации. Этот метод присваивает значения по умолчанию цвету компонентов цвета анимации. Он также повторно создает базовые COM-объекты, если они были созданы. Если вы подписаны на этот объект анимации на события (ValueChanged или Интежервалуечанжед), необходимо повторно включить эти события.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
