---
description: 'Дополнительные сведения о: Каниматионсизе Class'
title: Класс CAnimationSize
ms.date: 11/04/2016
f1_keywords:
- CAnimationSize
- AFXANIMATIONCONTROLLER/CAnimationSize
- AFXANIMATIONCONTROLLER/CAnimationSize::CAnimationSize
- AFXANIMATIONCONTROLLER/CAnimationSize::AddTransition
- AFXANIMATIONCONTROLLER/CAnimationSize::GetCX
- AFXANIMATIONCONTROLLER/CAnimationSize::GetCY
- AFXANIMATIONCONTROLLER/CAnimationSize::GetDefaultValue
- AFXANIMATIONCONTROLLER/CAnimationSize::GetValue
- AFXANIMATIONCONTROLLER/CAnimationSize::SetDefaultValue
- AFXANIMATIONCONTROLLER/CAnimationSize::GetAnimationVariableList
- AFXANIMATIONCONTROLLER/CAnimationSize::m_cxValue
- AFXANIMATIONCONTROLLER/CAnimationSize::m_cyValue
helpviewer_keywords:
- CAnimationSize [MFC], CAnimationSize
- CAnimationSize [MFC], AddTransition
- CAnimationSize [MFC], GetCX
- CAnimationSize [MFC], GetCY
- CAnimationSize [MFC], GetDefaultValue
- CAnimationSize [MFC], GetValue
- CAnimationSize [MFC], SetDefaultValue
- CAnimationSize [MFC], GetAnimationVariableList
- CAnimationSize [MFC], m_cxValue
- CAnimationSize [MFC], m_cyValue
ms.assetid: ea06d1b5-502c-44a3-82ca-8bd6ba6a9364
ms.openlocfilehash: 894675c485077291c3fca35acfb9bfa9a3d10286
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336769"
---
# <a name="canimationsize-class"></a>Класс CAnimationSize

Реализует функции объекта размера, размеры которого могут быть анимированы.

## <a name="syntax"></a>Синтаксис

```
class CAnimationSize : public CAnimationBaseObject;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Каниматионсизе:: Каниматионсизе](#canimationsize)|Перегружен. Конструирует объект размера анимации.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Каниматионсизе:: Аддтранситион](#addtransition)|Добавляет переходы для ширины и высоты.|
|[Каниматионсизе:: Жетккс](#getcx)|Предоставляет доступ к CAnimationVariable, представляющему ширину.|
|[Каниматионсизе:: Жетци](#getcy)|Предоставляет доступ к CAnimationVariable, представляющей высоту.|
|[Каниматионсизе:: DefaultValue](#getdefaultvalue)|Возвращает значения ширины и высоты по умолчанию.|
|[Каниматионсизе:: GetValue](#getvalue)|Возвращает текущее значение.|
|[Каниматионсизе:: Сетдефаултвалуе](#setdefaultvalue)|Задает значение по умолчанию.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Каниматионсизе:: Жетаниматионвариаблелист](#getanimationvariablelist)|Помещает переменные инкапсулированной анимации в список. (Переопределяет [каниматионбасеобжект:: жетаниматионвариаблелист](../../mfc/reference/canimationbaseobject-class.md#getanimationvariablelist).)|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Каниматионсизе:: operator Ксизе](#operator_csize)|Преобразует Каниматионсизе в Ксизе.|
|[Каниматионсизе:: operator =](#operator_eq)|Присваивает Сзсрк Каниматионсизе.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Каниматионсизе:: m_cxValue](#m_cxvalue)|Переменная инкапсулированной анимации, представляющая ширину размера анимации.|
|[Каниматионсизе:: m_cyValue](#m_cyvalue)|Переменная инкапсулированной анимации, представляющая высоту размера анимации.|

## <a name="remarks"></a>Комментарии

Класс Каниматионсизе инкапсулирует два объекта CAnimationVariable и может представлять в приложениях размер. Например, этот класс можно использовать для анимации размера любого двумерного объекта на экране (например, прямоугольника, элемента управления и т. д.). Чтобы использовать этот класс в приложении, просто создайте экземпляр объекта этого класса, добавьте его в контроллер анимации с помощью Каниматионконтроллер:: Адданиматионобжект и вызовите Аддтранситион, чтобы каждый переход был применен к ширине и (или) высоте.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[каниматионбасеобжект](../../mfc/reference/canimationbaseobject-class.md)

`CAnimationSize`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationsizeaddtransition"></a><a name="addtransition"></a> Каниматионсизе:: Аддтранситион

Добавляет переходы для ширины и высоты.

```cpp
void AddTransition(
    CBaseTransition* pCXTransition,
    CBaseTransition* pCYTransition);
```

### <a name="parameters"></a>Параметры

*пккстранситион*<br/>
Указатель на переход для ширины.

*пцитранситион*<br/>
Указатель на переход для высоты.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы добавить указанные переходы во внутренний список переходов, применяемых к переменным анимации для ширины и высоты. При добавлении переходов они не применяются немедленно и хранятся во внутреннем списке. Переходы применяются (добавляются к раскадровке для конкретного значения) при вызове Каниматионконтроллер:: Аниматеграуп. Если не нужно применять переход к одному из измерений, можно передать значение NULL.

## <a name="canimationsizecanimationsize"></a><a name="canimationsize"></a> Каниматионсизе:: Каниматионсизе

Конструирует объект размера анимации.

```
CAnimationSize();

CAnimationSize(
    const CSize& szDefault,
    UINT32 nGroupID,
    UINT32 nObjectID = (UINT32)-1,
    DWORD dwUserData = 0);
```

### <a name="parameters"></a>Параметры

*сздефаулт*<br/>
Задает размер по умолчанию.

*нграупид*<br/>
Указывает идентификатор группы.

*нобжектид*<br/>
Указывает идентификатор объекта.

*двусердата*<br/>
Указывает определяемые пользователем данные.

### <a name="remarks"></a>Комментарии

Объект создается со значениями по умолчанию для ширины, высоты, идентификатора объекта и идентификатора группы, которые будут установлены в 0. Их можно изменить позже во время выполнения с помощью Сетдефаултвалуе и Сетид.

## <a name="canimationsizegetanimationvariablelist"></a><a name="getanimationvariablelist"></a> Каниматионсизе:: Жетаниматионвариаблелист

Помещает переменные инкапсулированной анимации в список.

```
virtual void GetAnimationVariableList(
    CList<CAnimationVariable*,
    CAnimationVariable*>& lst);
```

### <a name="parameters"></a>Параметры

*LST*<br/>
При возврате функции она содержит указатели на два объекта CAnimationVariable, представляющие ширину и высоту.

## <a name="canimationsizegetcx"></a><a name="getcx"></a> Каниматионсизе:: Жетккс

Предоставляет доступ к CAnimationVariable, представляющему ширину.

```
CAnimationVariable& GetCX();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на инкапсулированный CAnimationVariable, представляющий ширину.

### <a name="remarks"></a>Комментарии

Этот метод можно вызвать для получения прямого доступа к базовым CAnimationVariable, представляющим ширину.

## <a name="canimationsizegetcy"></a><a name="getcy"></a> Каниматионсизе:: Жетци

Предоставляет доступ к CAnimationVariable, представляющей высоту.

```
CAnimationVariable& GetCY();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на инкапсулированный CAnimationVariable, представляющий высоту.

### <a name="remarks"></a>Комментарии

Этот метод можно вызвать для получения прямого доступа к базовым CAnimationVariable, представляющим высоту.

## <a name="canimationsizegetdefaultvalue"></a><a name="getdefaultvalue"></a> Каниматионсизе:: DefaultValue

Возвращает значения ширины и высоты по умолчанию.

```
CSize GetDefaultValue();
```

### <a name="return-value"></a>Возвращаемое значение

Объект Ксизе, содержащий значения по умолчанию.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы получить значение по умолчанию, которое было ранее задано конструктором или Сетдефаултвалуе.

## <a name="canimationsizegetvalue"></a><a name="getvalue"></a> Каниматионсизе:: GetValue

Возвращает текущее значение.

```
BOOL GetValue(CSize& szValue);
```

### <a name="parameters"></a>Параметры

*сзвалуе*<br/>
Выходные данные. Содержит текущее значение при возврате из метода.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если текущее значение было успешно получено; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы получить текущее значение размера анимации. Если этот метод завершается ошибкой или базовые COM-объекты для ширины и размера не были инициализированы, Сзвалуе содержит значение по умолчанию, которое ранее было задано в конструкторе или Сетдефаултвалуе.

## <a name="canimationsizem_cxvalue"></a><a name="m_cxvalue"></a> Каниматионсизе:: m_cxValue

Переменная инкапсулированной анимации, представляющая ширину размера анимации.

```
CAnimationVariable m_cxValue;
```

## <a name="canimationsizem_cyvalue"></a><a name="m_cyvalue"></a> Каниматионсизе:: m_cyValue

Переменная инкапсулированной анимации, представляющая высоту размера анимации.

```
CAnimationVariable m_cyValue;
```

## <a name="canimationsizeoperator-csize"></a><a name="operator_csize"></a> Каниматионсизе:: operator Ксизе

Преобразует Каниматионсизе в Ксизе.

```
operator CSize();
```

### <a name="return-value"></a>Возвращаемое значение

Текущее значение размера анимации в виде Ксизе.

### <a name="remarks"></a>Комментарии

Эта функция внутренне вызывает метод GetValue. Если по какой либо причине не удается выполнить GetValue, возвращаемый размер будет содержать значения по умолчанию для ширины и высоты.

## <a name="canimationsizeoperator"></a><a name="operator_eq"></a> Каниматионсизе:: operator =

Присваивает Сзсрк Каниматионсизе.

```cpp
void operator=(const CSize& szSrc);
```

### <a name="parameters"></a>Параметры

*сзсрк*<br/>
Ссылается на Ксизе или SIZE.

### <a name="remarks"></a>Комментарии

Присваивает Сзсрк Каниматионсизе. Рекомендуется сделать это перед началом анимации, так как этот оператор вызывает Сетдефаултвалуе, который повторно создает базовые объекты COM для ширины и высоты, если они были созданы. Если вы подписаны на этот объект анимации на события (ValueChanged или Интежервалуечанжед), необходимо повторно включить эти события.

## <a name="canimationsizesetdefaultvalue"></a><a name="setdefaultvalue"></a> Каниматионсизе:: Сетдефаултвалуе

Задает значение по умолчанию.

```cpp
void SetDefaultValue(const CSize& szDefault);
```

### <a name="parameters"></a>Параметры

*сздефаулт*<br/>
Указывает новый размер по умолчанию.

### <a name="remarks"></a>Комментарии

Эта функция используется для задания значения по умолчанию для объекта анимации. Этот метод присваивает значения по умолчанию Width и Height размера анимации. Он также повторно создает базовые COM-объекты, если они были созданы. Если вы подписаны на этот объект анимации на события (ValueChanged или Интежервалуечанжед), необходимо повторно включить эти события.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
