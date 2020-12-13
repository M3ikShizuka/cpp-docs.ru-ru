---
description: 'Дополнительные сведения о: CAnimationGroup Class'
title: Класс CAnimationGroup
ms.date: 03/27/2019
f1_keywords:
- CAnimationGroup
- AFXANIMATIONCONTROLLER/CAnimationGroup
- AFXANIMATIONCONTROLLER/CAnimationGroup::CAnimationGroup
- AFXANIMATIONCONTROLLER/CAnimationGroup::Animate
- AFXANIMATIONCONTROLLER/CAnimationGroup::ApplyTransitions
- AFXANIMATIONCONTROLLER/CAnimationGroup::FindAnimationObject
- AFXANIMATIONCONTROLLER/CAnimationGroup::GetGroupID
- AFXANIMATIONCONTROLLER/CAnimationGroup::RemoveKeyframes
- AFXANIMATIONCONTROLLER/CAnimationGroup::RemoveTransitions
- AFXANIMATIONCONTROLLER/CAnimationGroup::Schedule
- AFXANIMATIONCONTROLLER/CAnimationGroup::SetAutodestroyTransitions
- AFXANIMATIONCONTROLLER/CAnimationGroup::AddKeyframes
- AFXANIMATIONCONTROLLER/CAnimationGroup::AddTransitions
- AFXANIMATIONCONTROLLER/CAnimationGroup::CreateTransitions
- AFXANIMATIONCONTROLLER/CAnimationGroup::m_bAutoclearTransitions
- AFXANIMATIONCONTROLLER/CAnimationGroup::m_bAutodestroyAnimationObjects
- AFXANIMATIONCONTROLLER/CAnimationGroup::m_bAutodestroyKeyframes
- AFXANIMATIONCONTROLLER/CAnimationGroup::m_lstAnimationObjects
- AFXANIMATIONCONTROLLER/CAnimationGroup::m_lstKeyFrames
- AFXANIMATIONCONTROLLER/CAnimationGroup::m_pStoryboard
- AFXANIMATIONCONTROLLER/CAnimationGroup::m_nGroupID
- AFXANIMATIONCONTROLLER/CAnimationGroup::m_pParentController
helpviewer_keywords:
- CAnimationGroup [MFC], CAnimationGroup
- CAnimationGroup [MFC], Animate
- CAnimationGroup [MFC], ApplyTransitions
- CAnimationGroup [MFC], FindAnimationObject
- CAnimationGroup [MFC], GetGroupID
- CAnimationGroup [MFC], RemoveKeyframes
- CAnimationGroup [MFC], RemoveTransitions
- CAnimationGroup [MFC], Schedule
- CAnimationGroup [MFC], SetAutodestroyTransitions
- CAnimationGroup [MFC], AddKeyframes
- CAnimationGroup [MFC], AddTransitions
- CAnimationGroup [MFC], CreateTransitions
- CAnimationGroup [MFC], m_bAutoclearTransitions
- CAnimationGroup [MFC], m_bAutodestroyAnimationObjects
- CAnimationGroup [MFC], m_bAutodestroyKeyframes
- CAnimationGroup [MFC], m_lstAnimationObjects
- CAnimationGroup [MFC], m_lstKeyFrames
- CAnimationGroup [MFC], m_pStoryboard
- CAnimationGroup [MFC], m_nGroupID
- CAnimationGroup [MFC], m_pParentController
ms.assetid: 8bc18ceb-33a2-41d0-9731-71811adacab7
ms.openlocfilehash: 45fd49b95f73811f52795b87bf3de2dd004fa5ee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336794"
---
# <a name="canimationgroup-class"></a>Класс CAnimationGroup

Реализует группу анимации, объединяющую раскадровку анимации, объекты анимации и переходы для определения анимации.

## <a name="syntax"></a>Синтаксис

```
class CAnimationGroup;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CAnimationGroup:: CAnimationGroup](#canimationgroup)|Конструирует группу анимации.|
|[CAnimationGroup:: ~ CAnimationGroup](#_dtorcanimationgroup)|Деструктор Вызывается при уничтожении группы анимации.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CAnimationGroup:: анимировать](#animate)|Выполняет анимацию группы.|
|[CAnimationGroup:: Апплитранситионс](#applytransitions)|Применяет переходы к объектам анимации.|
|[CAnimationGroup:: Финданиматионобжект](#findanimationobject)|Находит объект анимации, содержащий указанную переменную анимации.|
|[CAnimationGroup:: Жетграупид](#getgroupid)|Возвращает значение GroupID.|
|[CAnimationGroup:: Ремовекэйфрамес](#removekeyframes)|Удаляет и при необходимости уничтожает все ключевые кадры, принадлежащие группе анимации.|
|[CAnimationGroup:: Ремоветранситионс](#removetransitions)|Удаляет переходы из объектов анимации, принадлежащих группе анимации.|
|[CAnimationGroup:: Schedule](#schedule)|Планирует анимацию в указанное время.|
|[CAnimationGroup:: Сетаутодестройтранситионс](#setautodestroytransitions)|Направляет все объекты анимации, входящие в группу, автоматически уничтожать переходы.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[CAnimationGroup:: Аддкэйфрамес](#addkeyframes)|Вспомогательный объект, добавляющий опорные кадры в раскадровку.|
|[CAnimationGroup:: Аддтранситионс](#addtransitions)|Вспомогательный объект, добавляющий переходы в раскадровку.|
|[CAnimationGroup:: Креатетранситионс](#createtransitions)|Вспомогательный объект, который создает COM-объекты перехода.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[CAnimationGroup:: m_bAutoclearTransitions](#m_bautocleartransitions)|Задает способ очистки переходов от объектов анимации, принадлежащих группе. Если этот член имеет значение TRUE, переходы автоматически удаляются при планировании анимации. В противном случае необходимо удалить переходы вручную.|
|[CAnimationGroup:: m_bAutodestroyAnimationObjects](#m_bautodestroyanimationobjects)|Указывает, как уничтожить объекты анимации. Если этот параметр имеет значение TRUE, объекты анимации будут автоматически уничтожены при удалении группы. В противном случае объекты анимации необходимо уничтожить вручную. Значение по умолчанию — FALSE. Присвойте этому параметру значение TRUE, только если все объекты анимации, принадлежащие к группе, выделяются динамически с помощью оператора New.|
|[CAnimationGroup:: m_bAutodestroyKeyframes](#m_bautodestroykeyframes)|Задает способ уничтожения опорных кадров. Если это значение равно TRUE, все опорные кадры удаляются и уничтожаются; в противном случае они удаляются только из списка. Значение по умолчанию — TRUE.|
|[CAnimationGroup:: m_lstAnimationObjects](#m_lstanimationobjects)|Содержит список объектов анимации.|
|[CAnimationGroup:: m_lstKeyFrames](#m_lstkeyframes)|Содержит список опорных кадров.|
|[CAnimationGroup:: m_pStoryboard](#m_pstoryboard)|Указывает на раскадровку анимации. Этот указатель допустим только после вызова в анимации.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CAnimationGroup:: m_nGroupID](#m_ngroupid)|Уникальный идентификатор группы анимации.|
|[CAnimationGroup:: m_pParentController](#m_pparentcontroller)|Указатель на контроллер анимации, к которому принадлежит эта группа.|

## <a name="remarks"></a>Комментарии

Группы анимации создаются автоматически контроллером анимации (Каниматионконтроллер) при добавлении объектов анимации с помощью Каниматионконтроллер:: Адданиматионобжект. Группа анимации определяется параметром GroupID, который обычно используется в качестве параметра для управления группами анимации. Объект GroupID берется из первого объекта анимации, добавляемого в новую группу анимации. Раскадровка инкапсулированной анимации создается после вызова Каниматионконтроллер:: Аниматеграуп и доступна через открытый член m_pStoryboard.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CAnimationGroup`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="canimationgroupcanimationgroup"></a><a name="_dtorcanimationgroup"></a> CAnimationGroup:: ~ CAnimationGroup

Деструктор Вызывается при уничтожении группы анимации.

```
~CAnimationGroup();
```

## <a name="canimationgroupaddkeyframes"></a><a name="addkeyframes"></a> CAnimationGroup:: Аддкэйфрамес

Вспомогательный объект, добавляющий опорные кадры в раскадровку.

```cpp
void AddKeyframes(IUIAnimationStoryboard* pStoryboard, BOOL bAddDeep);
```

### <a name="parameters"></a>Параметры

*псторибоард*<br/>
Указатель на COM-объект раскадровки.

*бадддип*<br/>
Указывает, должен ли этот метод добавляться к опорным кадрам раскадровки, которые зависят от других опорных кадров.

## <a name="canimationgroupaddtransitions"></a><a name="addtransitions"></a> CAnimationGroup:: Аддтранситионс

Вспомогательный объект, добавляющий переходы в раскадровку.

```cpp
void AddTransitions(
    IUIAnimationStoryboard* pStoryboard,
    BOOL bDependOnKeyframes);
```

### <a name="parameters"></a>Параметры

*псторибоард*<br/>
Указатель на COM-объект раскадровки.

*бдепендонкэйфрамес*

## <a name="canimationgroupanimate"></a><a name="animate"></a> CAnimationGroup:: анимировать

Выполняет анимацию группы.

```
BOOL Animate(
    IUIAnimationManager* pManager,
    IUIAnimationTimer* pTimer,
    BOOL bScheduleNow);
```

### <a name="parameters"></a>Параметры

*пманажер*<br/>
*птимер* 
 *бсчедуленов*

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если метод выполнен. в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Этот метод создает внутреннюю раскадровку, создает и применяет переходы и планирует анимацию, если Бсчедуленов имеет значение TRUE. Если Бсчедуленов имеет значение FALSE, необходимо вызвать Schedule для запуска анимации в указанное время.

## <a name="canimationgroupapplytransitions"></a><a name="applytransitions"></a> CAnimationGroup:: Апплитранситионс

Применяет переходы к объектам анимации.

```cpp
void ApplyTransitions();
```

### <a name="remarks"></a>Комментарии

Этот метод УТВЕРЖДАЕТся в режиме отладки, если раскадровка не была создана. Сначала создаются все переходы, затем добавляются "статические" ключевые кадры (опорные кадры, зависящие от смещений), добавляются переходы, которые не зависят от ключевых кадров, добавляются ключевые кадры в зависимости от переходов и других опорных кадров, а при последнем добавлении переходов, зависящих от опорных кадров.

## <a name="canimationgroupcanimationgroup"></a><a name="canimationgroup"></a> CAnimationGroup:: CAnimationGroup

Конструирует группу анимации.

```
CAnimationGroup(CAnimationController* pParentController, UINT32 nGroupID);
```

### <a name="parameters"></a>Параметры

*ппарентконтроллер*<br/>
Указатель на контроллер анимации, который создает группу.

*нграупид*<br/>
Указывает GroupID.

## <a name="canimationgroupcreatetransitions"></a><a name="createtransitions"></a> CAnimationGroup:: Креатетранситионс

Вспомогательный объект, который создает COM-объекты перехода.

```
BOOL CreateTransitions();
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если метод выполняется, в противном случае — значение FALSE.

## <a name="canimationgroupfindanimationobject"></a><a name="findanimationobject"></a> CAnimationGroup:: Финданиматионобжект

Находит объект анимации, содержащий указанную переменную анимации.

```
CAnimationBaseObject* FindAnimationObject(IUIAnimationVariable* pVariable);
```

### <a name="parameters"></a>Параметры

*пвариабле*<br/>
Указатель на переменную анимации.

### <a name="return-value"></a>Возвращаемое значение

Указатель на объект анимации или значение NULL, если объект анимации не найден.

## <a name="canimationgroupgetgroupid"></a><a name="getgroupid"></a> CAnimationGroup:: Жетграупид

Возвращает значение GroupID.

```
UINT32 GetGroupID() const;
```

### <a name="return-value"></a>Возвращаемое значение

Идентификатор группы.

## <a name="canimationgroupm_bautocleartransitions"></a><a name="m_bautocleartransitions"></a> CAnimationGroup:: m_bAutoclearTransitions

Задает способ очистки переходов от объектов анимации, принадлежащих группе. Если этот член имеет значение TRUE, переходы автоматически удаляются при планировании анимации. В противном случае необходимо удалить переходы вручную.

```
BOOL m_bAutoclearTransitions;
```

## <a name="canimationgroupm_bautodestroyanimationobjects"></a><a name="m_bautodestroyanimationobjects"></a> CAnimationGroup:: m_bAutodestroyAnimationObjects

Указывает, как уничтожить объекты анимации. Если этот параметр имеет значение TRUE, объекты анимации будут автоматически уничтожены при удалении группы. В противном случае объекты анимации необходимо уничтожить вручную. Значение по умолчанию — FALSE. Присвойте этому параметру значение TRUE, только если все объекты анимации, принадлежащие к группе, выделяются динамически с помощью оператора New.

```
BOOL m_bAutodestroyAnimationObjects;
```

## <a name="canimationgroupm_bautodestroykeyframes"></a><a name="m_bautodestroykeyframes"></a> CAnimationGroup:: m_bAutodestroyKeyframes

Задает способ уничтожения опорных кадров. Если это значение равно TRUE, все опорные кадры удаляются и уничтожаются; в противном случае они удаляются только из списка. Значение по умолчанию — TRUE.

```
BOOL m_bAutodestroyKeyframes;
```

## <a name="canimationgroupm_lstanimationobjects"></a><a name="m_lstanimationobjects"></a> CAnimationGroup:: m_lstAnimationObjects

Содержит список объектов анимации.

```
CObList m_lstAnimationObjects;
```

## <a name="canimationgroupm_lstkeyframes"></a><a name="m_lstkeyframes"></a> CAnimationGroup:: m_lstKeyFrames

Содержит список опорных кадров.

```
CObList m_lstKeyFrames;
```

## <a name="canimationgroupm_ngroupid"></a><a name="m_ngroupid"></a> CAnimationGroup:: m_nGroupID

Уникальный идентификатор группы анимации.

```
UINT32 m_nGroupID;
```

## <a name="canimationgroupm_pparentcontroller"></a><a name="m_pparentcontroller"></a> CAnimationGroup:: m_pParentController

Указатель на контроллер анимации, к которому принадлежит эта группа.

```
CAnimationController* m_pParentController;
```

## <a name="canimationgroupm_pstoryboard"></a><a name="m_pstoryboard"></a> CAnimationGroup:: m_pStoryboard

Указывает на раскадровку анимации. Этот указатель допустим только после вызова в анимации.

```
ATL::CComPtr<IUIAnimationStoryboard> m_pStoryboard;
```

## <a name="canimationgroupremovekeyframes"></a><a name="removekeyframes"></a> CAnimationGroup:: Ремовекэйфрамес

Удаляет и при необходимости уничтожает все ключевые кадры, принадлежащие группе анимации.

```cpp
void RemoveKeyframes();
```

### <a name="remarks"></a>Комментарии

Если m_bAutodestroyKeyframes член имеет значение TRUE, кадры удаляются и уничтожаются, в противном случае кадры удаляются из внутреннего списка опорных кадров.

## <a name="canimationgroupremovetransitions"></a><a name="removetransitions"></a> CAnimationGroup:: Ремоветранситионс

Удаляет переходы из объектов анимации, принадлежащих группе анимации.

```cpp
void RemoveTransitions();
```

### <a name="remarks"></a>Комментарии

Если флаг m_bAutoclearTransitions имеет значение TRUE, этот метод выполняет перебор всех объектов анимации, принадлежащих группе, и вызывает Каниматионобжект:: Клеартранситионс (FALSE).

## <a name="canimationgroupschedule"></a><a name="schedule"></a> CAnimationGroup:: Schedule

Планирует анимацию в указанное время.

```
BOOL Schedule(IUIAnimationTimer* pTimer, UI_ANIMATION_SECONDS time);
```

### <a name="parameters"></a>Параметры

*птимер*<br/>
Указатель на таймер анимации.

*time*<br/>
Указывает время запланировать анимацию.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если метод выполнен. Значение FALSE, если метод завершается неудачно или если не вызывалась анимация с параметром Бсчедуленов со значением FALSE.

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы запланировать анимацию в указанное время. Необходимо сначала вызвать метод анимации с параметром Бсчедуленов, равным FALSE.

## <a name="canimationgroupsetautodestroytransitions"></a><a name="setautodestroytransitions"></a> CAnimationGroup:: Сетаутодестройтранситионс

Направляет все объекты анимации, входящие в группу, автоматически уничтожать переходы.

```cpp
void SetAutodestroyTransitions(BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*баутодестрой*<br/>
Задает способ уничтожения переходов.

### <a name="remarks"></a>Комментарии

Присвойте этому параметру значение FALSE только при выделении переходов в стеке. Значение по умолчанию — TRUE, поэтому настоятельно рекомендуется выделить объекты перехода с помощью оператора New.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
