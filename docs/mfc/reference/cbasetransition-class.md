---
description: 'Дополнительные сведения о: CBaseTransition Class'
title: Класс CBaseTransition
ms.date: 03/27/2019
f1_keywords:
- CBaseTransition
- AFXANIMATIONCONTROLLER/CBaseTransition
- AFXANIMATIONCONTROLLER/CBaseTransition::CBaseTransition
- AFXANIMATIONCONTROLLER/CBaseTransition::AddToStoryboard
- AFXANIMATIONCONTROLLER/CBaseTransition::AddToStoryboardAtKeyframes
- AFXANIMATIONCONTROLLER/CBaseTransition::Clear
- AFXANIMATIONCONTROLLER/CBaseTransition::Create
- AFXANIMATIONCONTROLLER/CBaseTransition::GetEndKeyframe
- AFXANIMATIONCONTROLLER/CBaseTransition::GetRelatedVariable
- AFXANIMATIONCONTROLLER/CBaseTransition::GetStartKeyframe
- AFXANIMATIONCONTROLLER/CBaseTransition::GetTransition
- AFXANIMATIONCONTROLLER/CBaseTransition::GetType
- AFXANIMATIONCONTROLLER/CBaseTransition::IsAdded
- AFXANIMATIONCONTROLLER/CBaseTransition::SetKeyframes
- AFXANIMATIONCONTROLLER/CBaseTransition::SetRelatedVariable
- AFXANIMATIONCONTROLLER/CBaseTransition::m_bAdded
- AFXANIMATIONCONTROLLER/CBaseTransition::m_pEndKeyframe
- AFXANIMATIONCONTROLLER/CBaseTransition::m_pRelatedVariable
- AFXANIMATIONCONTROLLER/CBaseTransition::m_pStartKeyframe
- AFXANIMATIONCONTROLLER/CBaseTransition::m_transition
- AFXANIMATIONCONTROLLER/CBaseTransition::m_type
helpviewer_keywords:
- CBaseTransition [MFC], CBaseTransition
- CBaseTransition [MFC], AddToStoryboard
- CBaseTransition [MFC], AddToStoryboardAtKeyframes
- CBaseTransition [MFC], Clear
- CBaseTransition [MFC], Create
- CBaseTransition [MFC], GetEndKeyframe
- CBaseTransition [MFC], GetRelatedVariable
- CBaseTransition [MFC], GetStartKeyframe
- CBaseTransition [MFC], GetTransition
- CBaseTransition [MFC], GetType
- CBaseTransition [MFC], IsAdded
- CBaseTransition [MFC], SetKeyframes
- CBaseTransition [MFC], SetRelatedVariable
- CBaseTransition [MFC], m_bAdded
- CBaseTransition [MFC], m_pEndKeyframe
- CBaseTransition [MFC], m_pRelatedVariable
- CBaseTransition [MFC], m_pStartKeyframe
- CBaseTransition [MFC], m_transition
- CBaseTransition [MFC], m_type
ms.assetid: dfe84007-bbc5-43b7-b5b8-fae9145573bf
ms.openlocfilehash: 16a7b5e7f88e292fd2b771c627f7169c70fec2c7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97122828"
---
# <a name="cbasetransition-class"></a>Класс CBaseTransition

Представляет базовый переход.

## <a name="syntax"></a>Синтаксис

```
class CBaseTransition : public CObject;
```

## <a name="members"></a>Члены

### <a name="public-enumerations"></a>Открытые перечисления

|Имя|Описание|
|----------|-----------------|
|[Перечисление CBaseTransition:: TRANSITION_TYPE](#transition_type_enumeration)|Определяет типы переходов, которые в настоящее время поддерживаются реализацией API анимации Windows в MFC.|

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CBaseTransition:: CBaseTransition](#cbasetransition)|Конструирует базовый объект перехода.|
|[CBaseTransition:: ~ CBaseTransition](#_dtorcbasetransition)|Деструктор Вызывается при уничтожении объекта перехода.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CBaseTransition:: Аддтосторибоард](#addtostoryboard)|Добавляет переход к раскадровке.|
|[CBaseTransition:: Аддтосторибоардаткэйфрамес](#addtostoryboardatkeyframes)|Добавляет переход к раскадровке.|
|[CBaseTransition:: Clear](#clear)|Освобождает объект COM, инкапсулированный в Иуианиматионтранситион.|
|[CBaseTransition:: Create](#create)|Создает COM-переход.|
|[CBaseTransition:: Жетендкэйфраме](#getendkeyframe)|Возвращает начальный опорный кадр.|
|[CBaseTransition:: Жетрелатедвариабле](#getrelatedvariable)|Возвращает указатель на связанную переменную.|
|[CBaseTransition:: Жетстарткэйфраме](#getstartkeyframe)|Возвращает начальный опорный кадр.|
|[CBaseTransition:: ontransition](#gettransition)|Перегружен. Возвращает указатель на базовый COM-объект перехода.|
|[CBaseTransition:: GetType](#gettype)|Возвращает тип перехода.|
|[CBaseTransition:: added](#isadded)|Сообщает, добавлен ли переход в раскадровку.|
|[CBaseTransition:: Сеткэйфрамес](#setkeyframes)|Задает опорные кадры для перехода.|
|[CBaseTransition:: Сетрелатедвариабле](#setrelatedvariable)|Устанавливает связь между переменной анимации и переходом.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CBaseTransition:: m_bAdded](#m_badded)|Указывает, был ли добавлен переход к раскадровке.|
|[CBaseTransition:: m_pEndKeyframe](#m_pendkeyframe)|Хранит указатель на опорный кадр, указывающий конец перехода.|
|[CBaseTransition:: m_pRelatedVariable](#m_prelatedvariable)|Указатель на переменную анимации, которая анимируется с переходом, хранящимся в m_transition.|
|[CBaseTransition:: m_pStartKeyframe](#m_pstartkeyframe)|Хранит указатель на опорный кадр, указывающий начало перехода.|
|[CBaseTransition:: m_transition](#m_transition)|Хранит указатель на Иуианиматионтранситион. Значение NULL, если объект перехода COM не был создан.|
|[CBaseTransition:: m_type](#m_type)|Хранит тип перехода.|

## <a name="remarks"></a>Комментарии

Этот класс инкапсулирует интерфейс Иуианиматионтранситион и служит базовым классом для всех переходов.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CBaseTransition`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="cbasetransitioncbasetransition"></a><a name="_dtorcbasetransition"></a> CBaseTransition:: ~ CBaseTransition

Деструктор Вызывается при уничтожении объекта перехода.

```
virtual ~CBaseTransition();
```

## <a name="cbasetransitionaddtostoryboard"></a><a name="addtostoryboard"></a> CBaseTransition:: Аддтосторибоард

Добавляет переход к раскадровке.

```
BOOL AddToStoryboard(IUIAnimationStoryboard* pStoryboard);
```

### <a name="parameters"></a>Параметры

*псторибоард*<br/>
Указатель на раскадровку, которая будет анимировать связанную переменную.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если переход успешно добавлен в раскадровку.

### <a name="remarks"></a>Комментарии

Применяет переход к связанной переменной в раскадровке. Если это первый переход, применяемый к этой переменной в этой раскадровке, переход начинается в начале раскадровки. В противном случае переход добавляется к переходу, добавленному последним в переменную.

## <a name="cbasetransitionaddtostoryboardatkeyframes"></a><a name="addtostoryboardatkeyframes"></a> CBaseTransition:: Аддтосторибоардаткэйфрамес

Добавляет переход к раскадровке.

```
BOOL AddToStoryboardAtKeyframes(IUIAnimationStoryboard* pStoryboard);
```

### <a name="parameters"></a>Параметры

*псторибоард*<br/>
Указатель на раскадровку, которая будет анимировать связанную переменную.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если переход успешно добавлен в раскадровку.

### <a name="remarks"></a>Комментарии

Применяет переход к связанной переменной в раскадровке. Если указан начальный опорный кадр, переход начинается с этого опорного кадра. Если указан конечный опорный кадр, переход начинается с начального опорного кадра и останавливается в конечном опорном кадре. Если переход был создан с указанным параметром Duration, эта длительность перезаписывается на период времени между начальным и конечным опорными кадрами. Если ключевой кадр не указан, переход добавляется к переходу, добавленному последним в переменную.

## <a name="cbasetransitioncbasetransition"></a><a name="cbasetransition"></a> CBaseTransition:: CBaseTransition

Конструирует базовый объект перехода.

```
CBaseTransition();
```

## <a name="cbasetransitionclear"></a><a name="clear"></a> CBaseTransition:: Clear

Освобождает объект COM, инкапсулированный в Иуианиматионтранситион.

```cpp
void Clear();
```

### <a name="remarks"></a>Комментарии

Этот метод следует вызывать из метода Create производного класса, чтобы предотвратить утечку интерфейса Иуитранситион.

## <a name="cbasetransitioncreate"></a><a name="create"></a> CBaseTransition:: Create

Создает COM-переход.

```
virtual BOOL Create(
    IUIAnimationTransitionLibrary* pLibrary,
    IUIAnimationTransitionFactory* pFactory) = 0;
```

### <a name="parameters"></a>Параметры

*плибрари*<br/>
Указатель на библиотеку переходов, которая создает стандартные переходы. Для пользовательских переходов может быть задано значение NULL.

*pFactory*<br/>
Указатель на фабрику переходов, который создает пользовательские переходы. Для стандартных переходов может быть задано значение NULL.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если COM-объект перехода успешно создан; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Это Чистая виртуальная функция, которая должна быть переопределена в производном классе. Он вызывается платформой для создания экземпляра базового COM-объекта перехода.

## <a name="cbasetransitiongetendkeyframe"></a><a name="getendkeyframe"></a> CBaseTransition:: Жетендкэйфраме

Возвращает начальный опорный кадр.

```
CBaseKeyFrame* GetEndKeyframe();
```

### <a name="return-value"></a>Возвращаемое значение

Допустимый указатель на опорный кадр или значение NULL, если переход не должен вставляться между опорными кадрами.

### <a name="remarks"></a>Комментарии

Этот метод можно использовать для доступа к объекту опорного кадра, который был ранее задан Сеткэйфрамес. Он вызывается кодом верхнего уровня, когда в раскадровку добавляются переходы.

## <a name="cbasetransitiongetrelatedvariable"></a><a name="getrelatedvariable"></a> CBaseTransition:: Жетрелатедвариабле

Возвращает указатель на связанную переменную.

```
CAnimationVariable* GetRelatedVariable();
```

### <a name="return-value"></a>Возвращаемое значение

Допустимый указатель на переменную анимации или значение NULL, если переменная анимации не была задана параметром Сетрелатедвариабле.

### <a name="remarks"></a>Комментарии

Это метод доступа к связанной переменной анимации.

## <a name="cbasetransitiongetstartkeyframe"></a><a name="getstartkeyframe"></a> CBaseTransition:: Жетстарткэйфраме

Возвращает начальный опорный кадр.

```
CBaseKeyFrame* GetStartKeyframe();
```

### <a name="return-value"></a>Возвращаемое значение

Допустимый указатель на опорный кадр или значение NULL, если переход не должен начинаться после опорного кадра.

### <a name="remarks"></a>Комментарии

Этот метод можно использовать для доступа к объекту опорного кадра, который был ранее задан Сеткэйфрамес. Он вызывается кодом верхнего уровня, когда в раскадровку добавляются переходы.

## <a name="cbasetransitiongettransition"></a><a name="gettransition"></a> CBaseTransition:: ontransition

Возвращает указатель на базовый COM-объект перехода.

```
IUIAnimationTransition* GetTransition(
    IUIAnimationTransitionLibrary* pLibrary,
    IUIAnimationTransitionFactory* pFactory);

IUIAnimationTransition* GetTransition();
```

### <a name="parameters"></a>Параметры

*плибрари*<br/>
Указатель на библиотеку переходов, которая создает стандартные переходы. Для пользовательских переходов может быть задано значение NULL.

*pFactory*<br/>
Указатель на фабрику переходов, который создает пользовательские переходы. Для стандартных переходов может быть задано значение NULL.

### <a name="return-value"></a>Возвращаемое значение

Допустимый указатель на Иуианиматионтранситион или значение NULL, если невозможно создать базовый переход.

### <a name="remarks"></a>Комментарии

Этот метод возвращает указатель на базовый COM-объект перехода и при необходимости создает его.

## <a name="cbasetransitiongettype"></a><a name="gettype"></a> CBaseTransition:: GetType

Возвращает тип перехода.

```
TRANSITION_TYPE GetType() const;
```

### <a name="return-value"></a>Возвращаемое значение

Одно из TRANSITION_TYPE перечислимых значений.

### <a name="remarks"></a>Комментарии

Этот метод можно использовать для обнаружения объекта перехода по его типу. Тип задается в конструкторе в производном классе.

## <a name="cbasetransitionisadded"></a><a name="isadded"></a> CBaseTransition:: added

Сообщает, добавлен ли переход в раскадровку.

```
BOOL IsAdded();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если переход был добавлен в раскадровку; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Этот флаг задается внутренне, когда код верхнего уровня добавляет в раскадровку переходы.

## <a name="cbasetransitionm_badded"></a><a name="m_badded"></a> CBaseTransition:: m_bAdded

Указывает, был ли добавлен переход к раскадровке.

```
BOOL m_bAdded;
```

## <a name="cbasetransitionm_pendkeyframe"></a><a name="m_pendkeyframe"></a> CBaseTransition:: m_pEndKeyframe

Хранит указатель на опорный кадр, указывающий конец перехода.

```
CBaseKeyFrame* m_pEndKeyframe;
```

## <a name="cbasetransitionm_prelatedvariable"></a><a name="m_prelatedvariable"></a> CBaseTransition:: m_pRelatedVariable

Указатель на переменную анимации, которая анимируется с переходом, хранящимся в m_transition.

```
CAnimationVariable* m_pRelatedVariable;
```

## <a name="cbasetransitionm_pstartkeyframe"></a><a name="m_pstartkeyframe"></a> CBaseTransition:: m_pStartKeyframe

Хранит указатель на опорный кадр, указывающий начало перехода.

```
CBaseKeyFrame* m_pStartKeyframe;
```

## <a name="cbasetransitionm_transition"></a><a name="m_transition"></a> CBaseTransition:: m_transition

Хранит указатель на Иуианиматионтранситион. Значение NULL, если объект перехода COM не был создан.

```
ATL::CComPtr<IUIAnimationTransition> m_transition;
```

## <a name="cbasetransitionm_type"></a><a name="m_type"></a> CBaseTransition:: m_type

Хранит тип перехода.

```
TRANSITION_TYPE m_type;
```

## <a name="cbasetransitionsetkeyframes"></a><a name="setkeyframes"></a> CBaseTransition:: Сеткэйфрамес

Задает опорные кадры для перехода.

```cpp
void SetKeyframes(
    CBaseKeyFrame* pStart = NULL,
    CBaseKeyFrame* pEnd = NULL);
```

### <a name="parameters"></a>Параметры

*пстарт*<br/>
Опорный кадр, указывающий начало перехода.

*Ожидаем*<br/>
Опорный кадр, указывающий конец перехода.

### <a name="remarks"></a>Комментарии

Этот метод сообщает, что переход запускается после указанного опорного кадра, и, при необходимости, если параметр "переложить" не равен NULL, заканчивается до указанного опорного кадра. Если переход был создан с указанным параметром Duration, эта длительность перезаписывается на период времени между начальным и конечным опорными кадрами.

## <a name="cbasetransitionsetrelatedvariable"></a><a name="setrelatedvariable"></a> CBaseTransition:: Сетрелатедвариабле

Устанавливает связь между переменной анимации и переходом.

```cpp
void SetRelatedVariable(CAnimationVariable* pVariable);
```

### <a name="parameters"></a>Параметры

*пвариабле*<br/>
Указатель на связанную переменную анимации.

### <a name="remarks"></a>Комментарии

Устанавливает связь между переменной анимации и переходом. Переход может применяться только к одной переменной.

## <a name="cbasetransitiontransition_type-enumeration"></a><a name="transition_type_enumeration"></a> Перечисление CBaseTransition:: TRANSITION_TYPE

Определяет типы переходов, которые в настоящее время поддерживаются реализацией API анимации Windows в MFC.

```
enum TRANSITION_TYPE;
```

### <a name="remarks"></a>Комментарии

Тип перехода задается в конструкторе конкретного перехода. Например, Ксинусоидалтранситионфромранже задает для его типа значение SINUSOIDAL_FROM_RANGE.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
