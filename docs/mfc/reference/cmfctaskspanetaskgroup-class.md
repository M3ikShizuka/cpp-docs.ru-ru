---
description: 'Дополнительные сведения о: CMFCTasksPaneTaskGroup Class'
title: Класс CMFCTasksPaneTaskGroup
ms.date: 11/19/2018
f1_keywords:
- CMFCTasksPaneTaskGroup
- AFXTASKSPANE/CMFCTasksPaneTaskGroup
- AFXTASKSPANE/CMFCTasksPaneTaskGroup::CMFCTasksPaneTaskGroup
- AFXTASKSPANE/CMFCTasksPaneTaskGroup::SetACCData
- AFXTASKSPANE/CMFCTasksPaneTaskGroup::m_bIsBottom
- AFXTASKSPANE/CMFCTasksPaneTaskGroup::m_bIsCollapsed
- AFXTASKSPANE/CMFCTasksPaneTaskGroup::m_bIsSpecial
- AFXTASKSPANE/CMFCTasksPaneTaskGroup::m_lstTasks
- AFXTASKSPANE/CMFCTasksPaneTaskGroup::m_rect
- AFXTASKSPANE/CMFCTasksPaneTaskGroup::m_rectGroup
- AFXTASKSPANE/CMFCTasksPaneTaskGroup::m_strName
helpviewer_keywords:
- CMFCTasksPaneTaskGroup [MFC], CMFCTasksPaneTaskGroup
- CMFCTasksPaneTaskGroup [MFC], SetACCData
- CMFCTasksPaneTaskGroup [MFC], m_bIsBottom
- CMFCTasksPaneTaskGroup [MFC], m_bIsCollapsed
- CMFCTasksPaneTaskGroup [MFC], m_bIsSpecial
- CMFCTasksPaneTaskGroup [MFC], m_lstTasks
- CMFCTasksPaneTaskGroup [MFC], m_rect
- CMFCTasksPaneTaskGroup [MFC], m_rectGroup
- CMFCTasksPaneTaskGroup [MFC], m_strName
ms.assetid: 2111640b-a46e-4b27-b033-29e88632b86a
ms.openlocfilehash: 6b09923c70ad6208b1b029e6ad555c22cd4c771f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97254707"
---
# <a name="cmfctaskspanetaskgroup-class"></a>Класс CMFCTasksPaneTaskGroup

`CMFCTasksPaneTaskGroup`Класс является вспомогательным классом, используемым элементом управления [CMFCTasksPane](../../mfc/reference/cmfctaskspane-class.md) . Объекты типа `CMFCTasksPaneTaskGroup` представляют *группу задач*. Группа задач — это список элементов, отображаемых структурой в отдельном поле с кнопкой "Свернуть". Поле может иметь необязательный заголовок (имя группы). Если группа свернута, список задач не отображается.

## <a name="syntax"></a>Синтаксис

```
class CMFCTasksPaneTaskGroup : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMFCTasksPaneTaskGroup:: CMFCTasksPaneTaskGroup](#cmfctaskspanetaskgroup)|Формирует объект `CMFCTasksPaneTaskGroup`.|
|`CMFCTasksPaneTaskGroup::~CMFCTasksPaneTaskGroup`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCTasksPaneTaskGroup:: Сетаккдата](#setaccdata)|Определяет данные специальных возможностей для текущей группы задач.|

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|[CMFCTasksPaneTaskGroup:: m_bIsBottom](#m_bisbottom)|Определяет, соответствует ли группа задач нижней части элемента управления "область задач".|
|[CMFCTasksPaneTaskGroup:: m_bIsCollapsed](#m_biscollapsed)|Определяет, свернута ли группа задач.|
|[CMFCTasksPaneTaskGroup:: m_bIsSpecial](#m_bisspecial)|Определяет, является ли группа задач *специальной.* Платформа отображает специальные субтитры в другом цвете.|
|[CMFCTasksPaneTaskGroup:: m_lstTasks](#m_lsttasks)|Содержит внутренний список задач.|
|[CMFCTasksPaneTaskGroup:: m_rect](#m_rect)|Задает ограничивающий прямоугольник для заголовка группы.|
|[CMFCTasksPaneTaskGroup:: m_rectGroup](#m_rectgroup)|Задает ограничивающий прямоугольник группы.|
|[CMFCTasksPaneTaskGroup:: m_strName](#m_strname)|Задает имя группы.|

## <a name="remarks"></a>Комментарии

На следующем рисунке показана развернутая группа задач:

![Группа задач, развернутая](../../mfc/reference/media/nexttaskgrpexpand.png "Развернутая группа задач")

На следующем рисунке показана свернутая группа задач:

![Свернутая группа задач](../../mfc/reference/media/nexttaskgrpcollapse.png "Свернутая группа задач")

На следующем рисунке показана группа задач без подписи:

![Группа задач без заголовка](../../mfc/reference/media/nexttaskgrpnocapt.png "Группа задач без заголовка")

На следующем рисунке показаны две группы задач. Первая группа задач помечается как специальная, установив `m_bIsSpecial` для флага значение true, а вторая группа задач — не специальная. Обратите внимание, что заголовок первой группы задач темнее, чем вторая группа задач:

![Специальная группа задач](../../mfc/reference/media/nexttaskgrpspecial.png "Специальная группа задач")

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCTasksPaneTaskGroup](../../mfc/reference/cmfctaskspanetaskgroup-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкстаскспане. h

## <a name="cmfctaskspanetaskgroupcmfctaskspanetaskgroup"></a><a name="cmfctaskspanetaskgroup"></a> CMFCTasksPaneTaskGroup:: CMFCTasksPaneTaskGroup

Формирует объект `CMFCTasksPaneTaskGroup`.

```
CMFCTasksPaneTaskGroup(
    LPCTSTR lpszName,
    BOOL bIsBottom,
    BOOL bIsSpecial=FALSE,
    BOOL bIsCollapsed=FALSE,
    CMFCTasksPanePropertyPage* pPage=NULL,
    HICON hIcon=NULL);
```

### <a name="parameters"></a>Параметры

*лпсзнаме*<br/>
Задает имя группы в заголовке группы.

*бисботтом*<br/>
Указывает, выдается ли группа по нижнему краю элемента управления области задач.

*бисспеЦиал*<br/>
Указывает, обозначена ли группа как *Специальная* , и таким образом, будет ли заголовок группы заполняться другим цветом.

*бисколлапсед*<br/>
Указывает, свернута ли группа.

*ппаже*<br/>
Указывает страницу свойств, которой принадлежит эта группа задач.

*hIcon*<br/>
Задает значок, отображаемый в заголовке группы.

### <a name="remarks"></a>Комментарии

## <a name="cmfctaskspanetaskgroupm_bisbottom"></a><a name="m_bisbottom"></a> CMFCTasksPaneTaskGroup:: m_bIsBottom

Определяет, соответствует ли группа задач нижней части элемента управления "область задач".

```
BOOL m_bIsBottom;
```

### <a name="remarks"></a>Комментарии

Только одну группу можно вычислить по нижней части элемента управления области задач. Эта группа задач должна быть добавлена последней. Дополнительные сведения см. в разделе [CMFCTasksPane:: addgroup](../../mfc/reference/cmfctaskspane-class.md#addgroup).

## <a name="cmfctaskspanetaskgroupm_biscollapsed"></a><a name="m_biscollapsed"></a> CMFCTasksPaneTaskGroup:: m_bIsCollapsed

Определяет, свернута ли группа задач.

```
BOOL m_bIsCollapsed;
```

### <a name="remarks"></a>Комментарии

Можно включить или отключить возможность сворачивать группы в области задач путем вызова [CMFCTasksPane:: енаблеграупколлапсе](../../mfc/reference/cmfctaskspane-class.md#enablegroupcollapse).

## <a name="cmfctaskspanetaskgroupm_bisspecial"></a><a name="m_bisspecial"></a> CMFCTasksPaneTaskGroup:: m_bIsSpecial

Определяет, является ли группа задач *специальной* и должна ли подпись для специальной группы задач определяться другим цветом.

```
BOOL m_bIsSpecial;
```

### <a name="remarks"></a>Комментарии

Если приложение использует визуальную тему Windows XP и `m_bIsSpecial` имеет значение false, то платформа вызывает `DrawThemeBackground` с флагом EBP_NORMALGROUPBACKGROUND. Если `m_bIsSpecial` имеет значение true, платформа вызывает `DrawThemeBackground` с флагом EBP_SPECIALGROUPBACKGROUND.

## <a name="cmfctaskspanetaskgroupm_lsttasks"></a><a name="m_lsttasks"></a> CMFCTasksPaneTaskGroup:: m_lstTasks

Содержит внутренний список задач.

```
CObList m_lstTasks;
```

### <a name="remarks"></a>Комментарии

Чтобы заполнить этот список, вызовите метод [CMFCTasksPane:: AddTask](../../mfc/reference/cmfctaskspane-class.md#addtask).

## <a name="cmfctaskspanetaskgroupm_rect"></a><a name="m_rect"></a> CMFCTasksPaneTaskGroup:: m_rect

Задает ограничивающий прямоугольник для заголовка группы.

```
CRect m_rect;
```

### <a name="remarks"></a>Комментарии

Это значение вычисляется платформой автоматически.

## <a name="cmfctaskspanetaskgroupm_rectgroup"></a><a name="m_rectgroup"></a> CMFCTasksPaneTaskGroup:: m_rectGroup

Задает ограничивающий прямоугольник группы.

```
CRect m_rectGroup;
```

### <a name="remarks"></a>Комментарии

Это значение вычисляется платформой автоматически.

## <a name="cmfctaskspanetaskgroupm_strname"></a><a name="m_strname"></a> CMFCTasksPaneTaskGroup:: m_strName

Задает имя группы.

```
CString m_strName;
```

### <a name="remarks"></a>Комментарии

Если это значение пусто, заголовок группы не отображается, и группа не может быть свернута.

## <a name="cmfctaskspanetaskgroupsetaccdata"></a><a name="setaccdata"></a> CMFCTasksPaneTaskGroup:: Сетаккдата

Определяет данные специальных возможностей для текущей группы задач.

```
virtual BOOL SetACCData(
    CWnd* pParent,
    CAccessibilityData& data);
```

### <a name="parameters"></a>Параметры

*ппарент*<br/>
окне Представляет родительское окно текущей группы задач.

*data*<br/>
заполняет Объект типа `CAccessibilityData` , заполненный данными о специальных возможностях текущей группы задач.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если параметр *данных* успешно заполнен данными о специальных возможностях текущей группы задач; в противном случае — значение FALSE.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCTasksPane](../../mfc/reference/cmfctaskspane-class.md)<br/>
[Класс CMFCTasksPaneTask](../../mfc/reference/cmfctaskspanetask-class.md)<br/>
[Класс CMFCOutlookBar](../../mfc/reference/cmfcoutlookbar-class.md)<br/>
[CObject, класс](../../mfc/reference/cobject-class.md)
