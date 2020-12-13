---
description: 'Дополнительные сведения о: Каниматионпоинт Class'
title: Класс CAnimationPoint
ms.date: 11/04/2016
f1_keywords:
- CAnimationPoint
- AFXANIMATIONCONTROLLER/CAnimationPoint
- AFXANIMATIONCONTROLLER/CAnimationPoint::CAnimationPoint
- AFXANIMATIONCONTROLLER/CAnimationPoint::AddTransition
- AFXANIMATIONCONTROLLER/CAnimationPoint::GetDefaultValue
- AFXANIMATIONCONTROLLER/CAnimationPoint::GetValue
- AFXANIMATIONCONTROLLER/CAnimationPoint::GetX
- AFXANIMATIONCONTROLLER/CAnimationPoint::GetY
- AFXANIMATIONCONTROLLER/CAnimationPoint::SetDefaultValue
- AFXANIMATIONCONTROLLER/CAnimationPoint::GetAnimationVariableList
- AFXANIMATIONCONTROLLER/CAnimationPoint::m_xValue
- AFXANIMATIONCONTROLLER/CAnimationPoint::m_yValue
helpviewer_keywords:
- CAnimationPoint [MFC], CAnimationPoint
- CAnimationPoint [MFC], AddTransition
- CAnimationPoint [MFC], GetDefaultValue
- CAnimationPoint [MFC], GetValue
- CAnimationPoint [MFC], GetX
- CAnimationPoint [MFC], GetY
- CAnimationPoint [MFC], SetDefaultValue
- CAnimationPoint [MFC], GetAnimationVariableList
- CAnimationPoint [MFC], m_xValue
- CAnimationPoint [MFC], m_yValue
ms.assetid: 5dc4d46f-e695-4681-b15c-544b78b3e317
ms.openlocfilehash: ddefb93950f0ff1109478f3574413faf9f60a22a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336786"
---
# <a name="canimationpoint-class"></a>Класс CAnimationPoint

Реализует функции точки, координаты которой могут быть анимированы.

## <a name="syntax"></a>Синтаксис

```
class CAnimationPoint : public CAnimationBaseObject;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Каниматионпоинт:: Каниматионпоинт](#canimationpoint)|Перегружен. Конструирует объект Каниматионпоинт.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Каниматионпоинт:: Аддтранситион](#addtransition)|Добавляет переходы для координат X и Y.|
|[Каниматионпоинт:: DefaultValue](#getdefaultvalue)|Возвращает значения по умолчанию для координат X и Y.|
|[Каниматионпоинт:: GetValue](#getvalue)|Возвращает текущее значение.|
|[Каниматионпоинт:: Жеткс](#getx)|Предоставляет доступ к CAnimationVariable для координаты X.|
|[Каниматионпоинт:: Жети](#gety)|Предоставляет доступ к CAnimationVariable для координаты Y.|
|[Каниматионпоинт:: Сетдефаултвалуе](#setdefaultvalue)|Задает значение по умолчанию.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Каниматионпоинт:: Жетаниматионвариаблелист](#getanimationvariablelist)|Помещает переменные инкапсулированной анимации в список. (Переопределяет [каниматионбасеобжект:: жетаниматионвариаблелист](../../mfc/reference/canimationbaseobject-class.md#getanimationvariablelist).)|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Каниматионпоинт:: operator CPoint](#operator_cpoint)|Преобразует Каниматионпоинт в CPoint.|
|[Каниматионпоинт:: operator =](#operator_eq)|Присваивает Птсрк Каниматионпоинт.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Каниматионпоинт:: m_xValue](#m_xvalue)|Переменная инкапсулированной анимации, представляющая координату X точки анимации.|
|[Каниматионпоинт:: m_yValue](#m_yvalue)|Переменная инкапсулированной анимации, представляющая координату Y точки анимации.|

## <a name="remarks"></a>Комментарии

Класс Каниматионпоинт инкапсулирует два объекта CAnimationVariable и может представлять в приложениях точку. Например, этот класс можно использовать для анимации позиции любого объекта на экране (например, Текстовая строка, окружность, точка и т. д.). Чтобы использовать этот класс в приложении, просто создайте экземпляр объекта этого класса, добавьте его в контроллер анимации с помощью Каниматионконтроллер:: Адданиматионобжект и вызовите Аддтранситион, чтобы каждый переход был применен к координатам X и Y.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[каниматионбасеобжект](../../mfc/reference/canimationbaseobject-class.md)

`CAnimationPoint`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationpointaddtransition"></a><a name="addtransition"></a> Каниматионпоинт:: Аддтранситион

Добавляет переходы для координат X и Y.

```cpp
void AddTransition(
    CBaseTransition* pXTransition,
    CBaseTransition* pYTransition);
```

### <a name="parameters"></a>Параметры

*пкстранситион*<br/>
Указатель на переход для координат X.

*питранситион*<br/>
Указатель на переход для координаты Y.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы добавить указанные переходы во внутренний список переходов, применяемых к переменным анимации для координат X и Y. При добавлении переходов они не применяются немедленно и хранятся во внутреннем списке. Переходы применяются (добавляются к раскадровке для конкретного значения) при вызове Каниматионконтроллер:: Аниматеграуп. Если не нужно применять переход к одной из координат, можно передать значение NULL.

## <a name="canimationpointcanimationpoint"></a><a name="canimationpoint"></a> Каниматионпоинт:: Каниматионпоинт

Конструирует объект Каниматионпоинт.

```
CAnimationPoint();

CAnimationPoint(
    const CPoint& ptDefault,
    UINT32 nGroupID,
    UINT32 nObjectID = (UINT32)-1,
    DWORD dwUserData = 0);
```

### <a name="parameters"></a>Параметры

*птдефаулт*<br/>
Задает координаты точки по умолчанию.

*нграупид*<br/>
Указывает идентификатор группы.

*нобжектид*<br/>
Указывает идентификатор объекта.

*двусердата*<br/>
Указывает определяемые пользователем данные.

### <a name="remarks"></a>Комментарии

Конструирует объект Каниматионпоинт со свойствами по умолчанию: координаты точек по умолчанию, идентификатор группы и идентификатор объекта устанавливаются в 0.

## <a name="canimationpointgetanimationvariablelist"></a><a name="getanimationvariablelist"></a> Каниматионпоинт:: Жетаниматионвариаблелист

Помещает переменные инкапсулированной анимации в список.

```
virtual void GetAnimationVariableList(CList<CAnimationVariable*, CAnimationVariable*>& lst);
```

### <a name="parameters"></a>Параметры

*LST*<br/>
При возврате функции она содержит указатели на два объекта CAnimationVariable, представляющие координаты X и Y.

## <a name="canimationpointgetdefaultvalue"></a><a name="getdefaultvalue"></a> Каниматионпоинт:: DefaultValue

Возвращает значения по умолчанию для координат X и Y.

```
CPoint GetDefaultValue();
```

### <a name="return-value"></a>Возвращаемое значение

Точка, содержащая значение по умолчанию.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы получить значение по умолчанию, которое было ранее задано конструктором или Сетдефаултвалуе.

## <a name="canimationpointgetvalue"></a><a name="getvalue"></a> Каниматионпоинт:: GetValue

Возвращает текущее значение.

```
BOOL GetValue(CPoint& ptValue);
```

### <a name="parameters"></a>Параметры

*птвалуе*<br/>
Выходные данные. Содержит текущее значение при возврате из метода.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если текущее значение было успешно получено; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы получить текущее значение точки анимации. Если этот метод завершается неудачно или базовые COM-объекты для координат X и Y не были инициализированы, Птвалуе содержит значение по умолчанию, которое ранее было задано в конструкторе или Сетдефаултвалуе.

## <a name="canimationpointgetx"></a><a name="getx"></a> Каниматионпоинт:: Жеткс

Предоставляет доступ к CAnimationVariable для координаты X.

```
CAnimationVariable& GetX();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на инкапсулированный CAnimationVariable, представляющий координату X.

### <a name="remarks"></a>Комментарии

Этот метод можно вызвать для получения прямого доступа к базовой CAnimationVariable, представляющей координату X.

## <a name="canimationpointgety"></a><a name="gety"></a> Каниматионпоинт:: Жети

Предоставляет доступ к CAnimationVariable для координаты Y.

```
CAnimationVariable& GetY();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на инкапсулированный CAnimationVariable, представляющий координату Y.

### <a name="remarks"></a>Комментарии

Этот метод можно вызвать для получения прямого доступа к базовой CAnimationVariable, представляющей координату Y.

## <a name="canimationpointm_xvalue"></a><a name="m_xvalue"></a> Каниматионпоинт:: m_xValue

Переменная инкапсулированной анимации, представляющая координату X точки анимации.

```
CAnimationVariable m_xValue;
```

## <a name="canimationpointm_yvalue"></a><a name="m_yvalue"></a> Каниматионпоинт:: m_yValue

Переменная инкапсулированной анимации, представляющая координату Y точки анимации.

```
CAnimationVariable m_yValue;
```

## <a name="canimationpointoperator-cpoint"></a><a name="operator_cpoint"></a> Каниматионпоинт:: operator CPoint

Преобразует Каниматионпоинт в CPoint.

```
operator CPoint();
```

### <a name="return-value"></a>Возвращаемое значение

Текущее значение Каниматионпоинт как CPoint.

### <a name="remarks"></a>Комментарии

Эта функция внутренне вызывает метод GetValue. Если по какой бы то ни было причине не удается выполнить команду GetValue, возвращаемая точка будет содержать значения по умолчанию для координат X и Y.

## <a name="canimationpointoperator"></a><a name="operator_eq"></a> Каниматионпоинт:: operator =

Присваивает Птсрк Каниматионпоинт.

```cpp
void operator=(const CPoint& ptSrc);
```

### <a name="parameters"></a>Параметры

*птсрк*<br/>
Ссылается на CPoint или POINT.

### <a name="remarks"></a>Комментарии

Присваивает Птсрк Каниматионпоинт. Рекомендуется сделать это перед началом анимации, так как этот оператор вызывает Сетдефаултвалуе, который повторно создает базовые COM-объекты для координат X и Y, если они были созданы. Если вы подписаны на этот объект анимации на события (ValueChanged или Интежервалуечанжед), необходимо повторно включить эти события.

## <a name="canimationpointsetdefaultvalue"></a><a name="setdefaultvalue"></a> Каниматионпоинт:: Сетдефаултвалуе

Задает значение по умолчанию.

```cpp
void SetDefaultValue(const POINT& ptDefault);
```

### <a name="parameters"></a>Параметры

*птдефаулт*<br/>
Задает значение точки по умолчанию.

### <a name="remarks"></a>Комментарии

Эта функция используется для задания значения по умолчанию для объекта анимации. Этот метод присваивает значения по умолчанию координатам X и Y точки анимации. Он также повторно создает базовые COM-объекты, если они были созданы. Если вы подписаны на этот объект анимации на события (ValueChanged или Интежервалуечанжед), необходимо повторно включить эти события.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
