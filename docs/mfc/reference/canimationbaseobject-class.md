---
description: 'Дополнительные сведения о: Каниматионбасеобжект Class'
title: Класс CAnimationBaseObject
ms.date: 03/27/2019
f1_keywords:
- CAnimationBaseObject
- AFXANIMATIONCONTROLLER/CAnimationBaseObject
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::CAnimationBaseObject
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::ApplyTransitions
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::ClearTransitions
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::ContainsVariable
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::CreateTransitions
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::DetachFromController
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::EnableIntegerValueChangedEvent
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::EnableValueChangedEvent
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::GetAutodestroyTransitions
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::GetGroupID
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::GetObjectID
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::GetUserData
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::SetAutodestroyTransitions
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::SetID
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::SetUserData
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::GetAnimationVariableList
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::SetParentAnimationObjects
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::m_bAutodestroyTransitions
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::m_dwUserData
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::m_nGroupID
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::m_nObjectID
- AFXANIMATIONCONTROLLER/CAnimationBaseObject::m_pParentController
helpviewer_keywords:
- CAnimationBaseObject [MFC], CAnimationBaseObject
- CAnimationBaseObject [MFC], ApplyTransitions
- CAnimationBaseObject [MFC], ClearTransitions
- CAnimationBaseObject [MFC], ContainsVariable
- CAnimationBaseObject [MFC], CreateTransitions
- CAnimationBaseObject [MFC], DetachFromController
- CAnimationBaseObject [MFC], EnableIntegerValueChangedEvent
- CAnimationBaseObject [MFC], EnableValueChangedEvent
- CAnimationBaseObject [MFC], GetAutodestroyTransitions
- CAnimationBaseObject [MFC], GetGroupID
- CAnimationBaseObject [MFC], GetObjectID
- CAnimationBaseObject [MFC], GetUserData
- CAnimationBaseObject [MFC], SetAutodestroyTransitions
- CAnimationBaseObject [MFC], SetID
- CAnimationBaseObject [MFC], SetUserData
- CAnimationBaseObject [MFC], GetAnimationVariableList
- CAnimationBaseObject [MFC], SetParentAnimationObjects
- CAnimationBaseObject [MFC], m_bAutodestroyTransitions
- CAnimationBaseObject [MFC], m_dwUserData
- CAnimationBaseObject [MFC], m_nGroupID
- CAnimationBaseObject [MFC], m_nObjectID
- CAnimationBaseObject [MFC], m_pParentController
ms.assetid: 76b25917-940e-4eba-940f-31d270702603
ms.openlocfilehash: bc44d0e55b409f66648007eeb27fefd386640d9f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318667"
---
# <a name="canimationbaseobject-class"></a>Класс CAnimationBaseObject

Базовый класс для всех объектов анимации.

## <a name="syntax"></a>Синтаксис

```
class CAnimationBaseObject : public CObject;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Каниматионбасеобжект:: Каниматионбасеобжект](#canimationbaseobject)|Перегружен. Конструирует объект анимации.|
|[Каниматионбасеобжект:: ~ Каниматионбасеобжект](#_dtorcanimationbaseobject)|Деструктор Вызывается при уничтожении объекта анимации.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Каниматионбасеобжект:: Апплитранситионс](#applytransitions)|Добавляет переходы к раскадровке со инкапсулированной переменной анимации.|
|[Каниматионбасеобжект:: Клеартранситионс](#cleartransitions)|Удаляет все связанные переходы.|
|[Каниматионбасеобжект:: Контаинсвариабле](#containsvariable)|Определяет, содержит ли объект анимации определенную переменную анимации.|
|[Каниматионбасеобжект:: Креатетранситионс](#createtransitions)|Создает переходы, связанные с объектом анимации.|
|[Каниматионбасеобжект::D Етачфромконтроллер](#detachfromcontroller)|Отсоединяет объект анимации от родительского контроллера анимации.|
|[Каниматионбасеобжект:: Енаблеинтежервалуечанжедевент](#enableintegervaluechangedevent)|Настраивает обработчик событий измененного целочисленного значения.|
|[Каниматионбасеобжект:: Енаблевалуечанжедевент](#enablevaluechangedevent)|Настраивает обработчик событий изменения значения.|
|[Каниматионбасеобжект:: Жетаутодестройтранситионс](#getautodestroytransitions)|Указывает, уничтожаются ли связанные переходы автоматически.|
|[Каниматионбасеобжект:: Жетграупид](#getgroupid)|Возвращает идентификатор текущей группы.|
|[Каниматионбасеобжект:: ObjectID](#getobjectid)|Возвращает идентификатор текущего объекта.|
|[Каниматионбасеобжект:: UserData](#getuserdata)|Возвращает определяемые пользователем данные.|
|[Каниматионбасеобжект:: Сетаутодестройтранситионс](#setautodestroytransitions)|Задает флаг для автоматического уничтожения переходов.|
|[Каниматионбасеобжект:: Сетид](#setid)|Задает новые идентификаторы.|
|[Каниматионбасеобжект:: Сетусердата](#setuserdata)|Задает определяемые пользователем данные.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Каниматионбасеобжект:: Жетаниматионвариаблелист](#getanimationvariablelist)|Собирает указатели на содержащиеся в них переменные анимации.|
|[Каниматионбасеобжект:: Сетпарентаниматионобжектс](#setparentanimationobjects)|Устанавливает связь между переменными анимации, содержащимися в объекте анимации, и их контейнером.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Каниматионбасеобжект:: m_bAutodestroyTransitions](#m_bautodestroytransitions)|Указывает, следует ли автоматически удалять связанные переходы.|
|[Каниматионбасеобжект:: m_dwUserData](#m_dwuserdata)|Хранит определяемые пользователем данные.|
|[Каниматионбасеобжект:: m_nGroupID](#m_ngroupid)|Задает идентификатор группы объекта анимации.|
|[Каниматионбасеобжект:: m_nObjectID](#m_nobjectid)|Указывает идентификатор объекта анимации.|
|[Каниматионбасеобжект:: m_pParentController](#m_pparentcontroller)|Указатель на родительский контроллер анимации.|

## <a name="remarks"></a>Комментарии

Этот класс реализует базовые методы для всех объектов анимации. Объект анимации может представлять значение, точку, размер, прямоугольник или цвет в приложении, а также любую пользовательскую сущность. Объекты анимации хранятся в группах анимации (см. CAnimationGroup). Каждая группа может быть анимирована отдельно и может рассматриваться как аналог раскадровки. Объект анимации инкапсулирует одну или несколько переменных анимации (см. CAnimationVariable) в зависимости от его логического представления. Например, Каниматионрект содержит четыре переменные анимации — одну переменную для каждой стороны прямоугольника. Каждый класс объектов анимации предоставляет перегруженный метод Аддтранситион, который следует использовать для применения переходов к инкапсулированным переменным анимации. Объект анимации может быть идентифицирован по ИДЕНТИФИКАТОРу объекта (необязательно) и по ИДЕНТИФИКАТОРу группы. Идентификатор группы необходим для того, чтобы поместить объект анимации в правильную группу, но если идентификатор группы не указан, объект помещается в группу по умолчанию с ИДЕНТИФИКАТОРом 0. При вызове Сетид с разными GroupID объект анимации будет перемещен в другую группу (при необходимости создается новая группа).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CAnimationBaseObject`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationbaseobjectcanimationbaseobject"></a><a name="_dtorcanimationbaseobject"></a> Каниматионбасеобжект:: ~ Каниматионбасеобжект

Деструктор Вызывается при уничтожении объекта анимации.

```
virtual ~CAnimationBaseObject();
```

## <a name="canimationbaseobjectapplytransitions"></a><a name="applytransitions"></a> Каниматионбасеобжект:: Апплитранситионс

Добавляет переходы к раскадровке со инкапсулированной переменной анимации.

```
virtual BOOL ApplyTransitions(
    IUIAnimationStoryboard* pStoryboard,
    BOOL bDependOnKeyframes);
```

### <a name="parameters"></a>Параметры

*псторибоард*<br/>
Указатель на раскадровку.

*бдепендонкэйфрамес*<br/>
Если значение равно "FALSE", этот метод добавляет только те переходы, которые не зависят от опорных кадров.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если переходы были успешно добавлены.

### <a name="remarks"></a>Комментарии

Добавляет связанные переходы, которые были добавлены с помощью Аддтранситион (перегруженные методы в производных классах) в раскадровку.

## <a name="canimationbaseobjectcanimationbaseobject"></a><a name="canimationbaseobject"></a> Каниматионбасеобжект:: Каниматионбасеобжект

Конструирует объект анимации.

```
CAnimationBaseObject();

CAnimationBaseObject(
    UINT32 nGroupID,
    UINT32 nObjectID = (UINT32)-1,
    DWORD dwUserData = 0);
```

### <a name="parameters"></a>Параметры

*нграупид*<br/>
Указывает идентификатор группы.

*нобжектид*<br/>
Указывает идентификатор объекта.

*двусердата*<br/>
Определяемые пользователем данные, которые можно связать с объектом анимации и получить позже во время выполнения.

### <a name="remarks"></a>Комментарии

Конструирует объекты анимации и назначает идентификатор объекта по умолчанию (0) и идентификатор группы (0).

## <a name="canimationbaseobjectcleartransitions"></a><a name="cleartransitions"></a> Каниматионбасеобжект:: Клеартранситионс

Удаляет все связанные переходы.

```
virtual void ClearTransitions(BOOL bAutodestroy);
```

### <a name="parameters"></a>Параметры

*баутодестрой*<br/>
Указывает, следует ли уничтожать объекты перехода автоматически или просто удалить их из связанного списка.

### <a name="remarks"></a>Комментарии

Удаляет все связанные переходы и уничтожает их, если флаг Баутодестрой или m_bAutodestroyTransitions имеет значение TRUE. Переходы должны быть уничтожены автоматически только в том случае, если они не выделены в стеке. Если приведенные выше флаги имеют значение FALSE, то переходы просто удаляются из внутреннего списка связанных переходов.

## <a name="canimationbaseobjectcontainsvariable"></a><a name="containsvariable"></a> Каниматионбасеобжект:: Контаинсвариабле

Определяет, содержит ли объект анимации определенную переменную анимации.

```
virtual BOOL ContainsVariable(IUIAnimationVariable* pVariable);
```

### <a name="parameters"></a>Параметры

*пвариабле*<br/>
Указатель на переменную анимации.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если переменная анимации содержится в объекте анимации; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

С помощью этого метода можно определить, содержится ли в объекте анимации переменная анимации, заданная параметром Пвариабле. Объект анимации в зависимости от его типа может содержать несколько переменных анимации. Например, Каниматионколор содержит три переменные: по одному для каждого компонента цвета (красный, зеленый и синий). При изменении значения переменной анимации API анимации Windows отправляет события ValueChanged или Интежервалуечанжед (если они включены), а параметр этого события — указатель на интерфейс Иуианиматионвариабле переменной анимации. Этот метод помогает получить указатель на анимацию из указателя на содержащийся объект COM.

## <a name="canimationbaseobjectcreatetransitions"></a><a name="createtransitions"></a> Каниматионбасеобжект:: Креатетранситионс

Создает переходы, связанные с объектом анимации.

```
BOOL CreateTransitions();
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если переходы успешно созданы; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Перебирает список переменных анимации, инкапсулированных в производный объект анимации, и создает переходы, связанные с каждой переменной анимации.

## <a name="canimationbaseobjectdetachfromcontroller"></a><a name="detachfromcontroller"></a> Каниматионбасеобжект::D Етачфромконтроллер

Отсоединяет объект анимации от родительского контроллера анимации.

```cpp
void DetachFromController();
```

### <a name="remarks"></a>Комментарии

Этот метод используется внутренним образом.

## <a name="canimationbaseobjectenableintegervaluechangedevent"></a><a name="enableintegervaluechangedevent"></a> Каниматионбасеобжект:: Енаблеинтежервалуечанжедевент

Настраивает обработчик событий измененного целочисленного значения.

```
virtual void EnableIntegerValueChangedEvent(
    CAnimationController* pController,
    BOOL bEnable);
```

### <a name="parameters"></a>Параметры

*пконтроллер*<br/>
Указатель на родительский контроллер.

*bEnable*<br/>
Указывает, следует ли включить или отключить событие изменения целочисленного значения.

### <a name="remarks"></a>Комментарии

Если включен обработчик событий "целочисленное значение изменено", это событие можно обрабатывать в методе Каниматионконтроллер:: Онаниматионинтежервалуечанжед, который должен быть переопределен в классе, производном от Каниматионконтроллер. Этот метод вызывается каждый раз при изменении целочисленного значения анимации.

## <a name="canimationbaseobjectenablevaluechangedevent"></a><a name="enablevaluechangedevent"></a> Каниматионбасеобжект:: Енаблевалуечанжедевент

Настраивает обработчик событий изменения значения.

```
virtual void EnableValueChangedEvent(
    CAnimationController* pController,
    BOOL bEnable);
```

### <a name="parameters"></a>Параметры

*пконтроллер*<br/>
Указатель на родительский контроллер.

*bEnable*<br/>
Указывает, следует ли включить или отключить событие изменения значения.

### <a name="remarks"></a>Комментарии

Если включен обработчик событий изменения значения, это событие можно обрабатывать в методе Каниматионконтроллер:: Онаниматионвалуечанжед, который должен быть переопределен в классе, производном от Каниматионконтроллер. Этот метод вызывается каждый раз при изменении значения анимации.

## <a name="canimationbaseobjectgetanimationvariablelist"></a><a name="getanimationvariablelist"></a> Каниматионбасеобжект:: Жетаниматионвариаблелист

Собирает указатели на содержащиеся в них переменные анимации.

```
virtual void GetAnimationVariableList(
    CList<CAnimationVariable*,
    CAnimationVariable*>& list) = 0;
```

### <a name="parameters"></a>Параметры

*list*<br/>
Список, который должен быть заполнен переменными анимации, содержащимися в объекте анимации.

### <a name="remarks"></a>Комментарии

Этот чистый виртуальный метод должен быть переопределен в производном классе. Объект анимации в зависимости от его типа содержит одну или несколько переменных анимации. Например, Каниматионпоинт содержит две переменные для координат X и Y соответственно. Базовый класс Каниматионбасеобжект реализует некоторые универсальные методы, которые работают со списком переменных анимации: Апплитранситионс, Клеартранситионс, Енаблевалуечанжедевент, EnableIntegerValueChangedEvent. Эти методы вызывают Жетаниматионвариаблелист, который заполняется производным классом с фактическими переменными анимации, содержащимися в определенном объекте анимации, затем выполняет цикл над списком и выполняют необходимые действия. При создании настраиваемого объекта анимации необходимо добавить в *список* всех переменных анимации, содержащихся в этом объекте.

## <a name="canimationbaseobjectgetautodestroytransitions"></a><a name="getautodestroytransitions"></a> Каниматионбасеобжект:: Жетаутодестройтранситионс

Указывает, уничтожаются ли связанные переходы автоматически.

```
BOOL GetAutodestroyTransitions() const;
```

### <a name="return-value"></a>Возвращаемое значение

Если значение равно TRUE, связанные переходы уничтожаются автоматически; Если значение равно FALSE, объекты перехода должны быть освобождены путем вызова приложения.

### <a name="remarks"></a>Комментарии

По умолчанию этот флаг имеет значение TRUE. Этот флаг устанавливается только в том случае, если вы выделили переход на стек и (или) переходы должны быть освобождены вызывающим приложением.

## <a name="canimationbaseobjectgetgroupid"></a><a name="getgroupid"></a> Каниматионбасеобжект:: Жетграупид

Возвращает идентификатор текущей группы.

```
UINT32 GetGroupID() const;
```

### <a name="return-value"></a>Возвращаемое значение

ИДЕНТИФИКАТОР текущей группы.

### <a name="remarks"></a>Комментарии

Используйте этот метод для получения идентификатора группы. Значение 0, если идентификатор группы не был явно задан в конструкторе или с помощью Сетид.

## <a name="canimationbaseobjectgetobjectid"></a><a name="getobjectid"></a> Каниматионбасеобжект:: ObjectID

Возвращает идентификатор текущего объекта.

```
UINT32 GetObjectID() const;
```

### <a name="return-value"></a>Возвращаемое значение

Текущий идентификатор объекта.

### <a name="remarks"></a>Комментарии

Используйте этот метод для получения идентификатора объекта. Значение 0, если идентификатор объекта не был явно задан в конструкторе или с помощью Сетид.

## <a name="canimationbaseobjectgetuserdata"></a><a name="getuserdata"></a> Каниматионбасеобжект:: UserData

Возвращает определяемые пользователем данные.

```
DWORD GetUserData() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение пользовательских данных.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы получить пользовательские данные во время выполнения. Возвращаемое значение будет равно 0, если оно не было явно инициализировано в конструкторе или с Сетусердата.

## <a name="canimationbaseobjectm_bautodestroytransitions"></a><a name="m_bautodestroytransitions"></a> Каниматионбасеобжект:: m_bAutodestroyTransitions

Указывает, следует ли автоматически удалять связанные переходы.

```
BOOL m_bAutodestroyTransitions;
```

## <a name="canimationbaseobjectm_dwuserdata"></a><a name="m_dwuserdata"></a> Каниматионбасеобжект:: m_dwUserData

Хранит определяемые пользователем данные.

```
DWORD m_dwUserData;
```

## <a name="canimationbaseobjectm_ngroupid"></a><a name="m_ngroupid"></a> Каниматионбасеобжект:: m_nGroupID

Задает идентификатор группы объекта анимации.

```
UINT32 m_nGroupID;
```

## <a name="canimationbaseobjectm_nobjectid"></a><a name="m_nobjectid"></a> Каниматионбасеобжект:: m_nObjectID

Указывает идентификатор объекта анимации.

```
UINT32 m_nObjectID;
```

## <a name="canimationbaseobjectm_pparentcontroller"></a><a name="m_pparentcontroller"></a> Каниматионбасеобжект:: m_pParentController

Указатель на родительский контроллер анимации.

```
CAnimationController* m_pParentController;
```

## <a name="canimationbaseobjectsetautodestroytransitions"></a><a name="setautodestroytransitions"></a> Каниматионбасеобжект:: Сетаутодестройтранситионс

Задает флаг для автоматического уничтожения переходов.

```cpp
void SetAutodestroyTransitions(BOOL bValue);
```

### <a name="parameters"></a>Параметры

*bValue*<br/>
Задает флаг автоматического уничтожения.

### <a name="remarks"></a>Комментарии

Установите этот флаг только в том случае, если вы выделили объекты перехода с помощью оператора New. Если по некоторым причинам объекты перехода выделяются в стеке, флаг автоматического уничтожения должен иметь значение FALSE. По умолчанию этот флаг имеет значение TRUE.

## <a name="canimationbaseobjectsetid"></a><a name="setid"></a> Каниматионбасеобжект:: Сетид

Задает новые идентификаторы.

```cpp
void SetID(
    UINT32 nObjectID,
    UINT32 nGroupID = 0);
```

### <a name="parameters"></a>Параметры

*нобжектид*<br/>
Указывает новый идентификатор объекта.

*нграупид*<br/>
Указывает новый идентификатор группы.

### <a name="remarks"></a>Комментарии

Позволяет изменить идентификатор объекта и идентификатор группы. Если новый идентификатор группы отличается от текущего, объект анимации перемещается в другую группу (при необходимости создается новая группа).

## <a name="canimationbaseobjectsetparentanimationobjects"></a><a name="setparentanimationobjects"></a> Каниматионбасеобжект:: Сетпарентаниматионобжектс

Устанавливает связь между переменными анимации, содержащимися в объекте анимации, и их контейнером.

```
virtual void SetParentAnimationObjects();
```

### <a name="remarks"></a>Комментарии

Этот вспомогательный метод можно использовать для установления связи между переменными анимации, содержащимися в объекте анимации, и их контейнером. Он циклически перебирает переменные анимации и устанавливает обратный указатель на родительский объект анимации для каждой переменной анимации. В текущей реализации фактическая связь устанавливается в Каниматионбасеобжект:: Апплитранситионс, поэтому указатели обратного вызова не задаются, пока не будет вызван CAnimationGroup:: анимировать. Знание связи может оказаться полезной при обработке событий и необходимости получить родительский объект анимации из CAnimationVariable. Используйте CAnimationVariable:: Жетпарентаниматионобжект.

## <a name="canimationbaseobjectsetuserdata"></a><a name="setuserdata"></a> Каниматионбасеобжект:: Сетусердата

Задает определяемые пользователем данные.

```cpp
void SetUserData (DWORD dwUserData);
```

### <a name="parameters"></a>Параметры

*двусердата*<br/>
Задает пользовательские данные.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы связать пользовательские данные с объектом анимации. Эти данные можно получить позже во время выполнения с помощью UserData.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
