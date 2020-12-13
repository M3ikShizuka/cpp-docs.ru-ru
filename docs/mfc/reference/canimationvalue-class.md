---
description: 'Дополнительные сведения о: CAnimationValue Class'
title: Класс CAnimationValue
ms.date: 11/04/2016
f1_keywords:
- CAnimationValue
- AFXANIMATIONCONTROLLER/CAnimationValue
- AFXANIMATIONCONTROLLER/CAnimationValue::CAnimationValue
- AFXANIMATIONCONTROLLER/CAnimationValue::AddTransition
- AFXANIMATIONCONTROLLER/CAnimationValue::GetValue
- AFXANIMATIONCONTROLLER/CAnimationValue::GetVariable
- AFXANIMATIONCONTROLLER/CAnimationValue::SetDefaultValue
- AFXANIMATIONCONTROLLER/CAnimationValue::GetAnimationVariableList
- AFXANIMATIONCONTROLLER/CAnimationValue::m_value
helpviewer_keywords:
- CAnimationValue [MFC], CAnimationValue
- CAnimationValue [MFC], AddTransition
- CAnimationValue [MFC], GetValue
- CAnimationValue [MFC], GetVariable
- CAnimationValue [MFC], SetDefaultValue
- CAnimationValue [MFC], GetAnimationVariableList
- CAnimationValue [MFC], m_value
ms.assetid: 78c5ae19-ede5-4f20-bfbe-68b467b603c2
ms.openlocfilehash: d704e83d286b4078af90d09edef35e8445d149d3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336750"
---
# <a name="canimationvalue-class"></a>Класс CAnimationValue

Реализует функции объекта анимации, имеющего одно значение.

## <a name="syntax"></a>Синтаксис

```
class CAnimationValue : public CAnimationBaseObject;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CAnimationValue:: CAnimationValue](#canimationvalue)|Перегружен. Конструирует объект CAnimationValue.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CAnimationValue:: Аддтранситион](#addtransition)|Добавляет переход, применяемый к значению.|
|[CAnimationValue:: GetValue](#getvalue)|Перегружен. Извлекает текущее значение.|
|[CAnimationValue:: variable](#getvariable)|Предоставляет доступ к переменной инкапсулированной анимации.|
|[CAnimationValue:: Сетдефаултвалуе](#setdefaultvalue)|Задает значение по умолчанию.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[CAnimationValue:: Жетаниматионвариаблелист](#getanimationvariablelist)|Помещает переменную инкапсулированной анимации в список. (Переопределяет [каниматионбасеобжект:: жетаниматионвариаблелист](../../mfc/reference/canimationbaseobject-class.md#getanimationvariablelist).)|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CAnimationValue:: operator, двойной](#operator_double)|Обеспечивает преобразование между CAnimationValue и DOUBLE.|
|[CAnimationValue:: operator INT32](#operator_int32)|Обеспечивает преобразование между CAnimationValue и INT32.|
|[CAnimationValue:: operator =](#operator_eq)|Перегружен. Присваивает значение INT32 CAnimationValue.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CAnimationValue:: m_value](#m_value)|Переменная инкапсулированной анимации, представляющая значение анимации.|

## <a name="remarks"></a>Комментарии

Класс CAnimationValue инкапсулирует один объект CAnimationVariable и может представлять в приложениях одно анимированное значение. Например, этот класс можно использовать для анимированной прозрачности (эффекта исчезновения), угла (для поворота объектов) или для любого другого случая, когда необходимо создать анимацию в зависимости от одного анимированного значения. Чтобы использовать этот класс в приложении, просто создайте экземпляр объекта этого класса, добавьте его в контроллер анимации с помощью Каниматионконтроллер:: Адданиматионобжект и вызовите Аддтранситион для каждого перехода, применяемого к значению.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[каниматионбасеобжект](../../mfc/reference/canimationbaseobject-class.md)

`CAnimationValue`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationvalueaddtransition"></a><a name="addtransition"></a> CAnimationValue:: Аддтранситион

Добавляет переход, применяемый к значению.

```cpp
void AddTransition(CBaseTransition* pTransition);
```

### <a name="parameters"></a>Параметры

*птранситион*<br/>
Указатель на объект перехода.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы добавить переход к внутреннему списку переходов, применяемых к переменной анимации. При добавлении переходов они не применяются немедленно и хранятся во внутреннем списке. Переходы применяются (добавляются к раскадровке для конкретного значения) при вызове Каниматионконтроллер:: Аниматеграуп.

## <a name="canimationvaluecanimationvalue"></a><a name="canimationvalue"></a> CAnimationValue:: CAnimationValue

Конструирует объект CAnimationValue.

```
CAnimationValue();

CAnimationValue(
    DOUBLE dblDefaultValue,
    UINT32 nGroupID,
    UINT32 nObjectID = (UINT32)-1,
    DWORD dwUserData = 0);
```

### <a name="parameters"></a>Параметры

*дблдефаултвалуе*<br/>
Задает значение по умолчанию.

*нграупид*<br/>
Указывает идентификатор группы.

*нобжектид*<br/>
Указывает идентификатор объекта.

*двусердата*<br/>
указывает определяемые пользователем данные.

### <a name="remarks"></a>Комментарии

Конструирует объект CAnimationValue со свойствами по умолчанию: значение по умолчанию, идентификатор группы и идентификатор объекта устанавливаются в 0.

## <a name="canimationvaluegetanimationvariablelist"></a><a name="getanimationvariablelist"></a> CAnimationValue:: Жетаниматионвариаблелист

Помещает переменную инкапсулированной анимации в список.

```
virtual void GetAnimationVariableList(
    CList<CAnimationVariable*,
    CAnimationVariable*>& lst);
```

### <a name="parameters"></a>Параметры

*LST*<br/>
При возврате функции она содержит указатель на CAnimationVariable, представляющий анимированное значение.

## <a name="canimationvaluegetvalue"></a><a name="getvalue"></a> CAnimationValue:: GetValue

Извлекает текущее значение.

```
BOOL GetValue(DOUBLE& dblValue);
BOOL GetValue(INT32& nValue);
```

### <a name="parameters"></a>Параметры

*дблвалуе*<br/>
Выходные данные. При возврате функции она содержит текущее значение переменной анимации.

*Nзначение*<br/>
Выходные данные. При возврате функции она содержит текущее значение переменной анимации.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если текущее значение успешно получено; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы получить текущее значение. Эта реализация вызывает инкапсулированный COM-объект, и если вызов завершается неудачно, этот метод возвращает значение по умолчанию, которое было ранее задано в конструкторе или с помощью Сетдефаултвалуе.

## <a name="canimationvaluegetvariable"></a><a name="getvariable"></a> CAnimationValue:: variable

Предоставляет доступ к переменной инкапсулированной анимации.

```
CAnimationVariable& GetVariable();
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на переменную инкапсулированной анимации.

### <a name="remarks"></a>Комментарии

Используйте этот метод для доступа к переменной инкапсулированной анимации. Из CAnimationVariable вы получаете доступ к базовому объекту Иуианиматионвариабле, указатель которого может иметь значение NULL, если переменная анимации не была создана.

## <a name="canimationvaluem_value"></a><a name="m_value"></a> CAnimationValue:: m_value

Переменная инкапсулированной анимации, представляющая значение анимации.

```
CAnimationVariable m_value;
```

## <a name="canimationvalueoperator-double"></a><a name="operator_double"></a> CAnimationValue:: operator, двойной

Обеспечивает преобразование между CAnimationValue и DOUBLE.

```
operator DOUBLE();
```

### <a name="return-value"></a>Возвращаемое значение

Текущее значение значения анимации.

### <a name="remarks"></a>Комментарии

Обеспечивает преобразование между CAnimationValue и DOUBLE. Этот метод внутренне вызывает функцию GetValue и не проверяет наличие ошибок. Если не удается выполнить GetValue, возвращаемое значение будет содержать значение по умолчанию, установленное ранее в конструкторе или с Сетдефаултвалуе.

## <a name="canimationvalueoperator-int32"></a><a name="operator_int32"></a> CAnimationValue:: operator INT32

Обеспечивает преобразование между CAnimationValue и INT32.

```
operator INT32();
```

### <a name="return-value"></a>Возвращаемое значение

Текущее значение значения анимации в виде целого числа.

### <a name="remarks"></a>Комментарии

Обеспечивает преобразование между CAnimationValue и INT32. Этот метод внутренне вызывает функцию GetValue и не проверяет наличие ошибок. Если не удается выполнить GetValue, возвращаемое значение будет содержать значение по умолчанию, установленное ранее в конструкторе или с Сетдефаултвалуе.

## <a name="canimationvalueoperator"></a><a name="operator_eq"></a> CAnimationValue:: operator =

Присваивает значение типа DOUBLE CAnimationValue.

```cpp
void operator=(DOUBLE dblVal);
void operator=(INT32 nVal);
```

### <a name="parameters"></a>Параметры

*дблвал*<br/>
Указывает значение, присваиваемое значению анимации.

*Непредвиденное nval*<br/>
Указывает значение, присваиваемое значению анимации.

### <a name="remarks"></a>Комментарии

Присваивает значение типа DOUBLE CAnimationValue. Это значение задается как значение по умолчанию для переменной инкапсулированной анимации. Если вы подписаны на этот объект анимации на события (ValueChanged или Интежервалуечанжед), необходимо повторно включить эти события.

## <a name="canimationvaluesetdefaultvalue"></a><a name="setdefaultvalue"></a> CAnimationValue:: Сетдефаултвалуе

Задает значение по умолчанию.

```cpp
void SetDefaultValue(DOUBLE dblDefaultValue);
```

### <a name="parameters"></a>Параметры

*дблдефаултвалуе*<br/>
Задает значение по умолчанию.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы задать значение по умолчанию. Значение по умолчанию возвращается приложению, если анимация не была запущена, а базовый COM-объект не создан. Если базовый COM-объект, инкапсулированный в Каниматионварибле, уже создан, этот метод повторно создает его, поэтому может потребоваться снова вызвать методы Енаблевалуечанжед/Енаблеинтежервалуечанжед.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
