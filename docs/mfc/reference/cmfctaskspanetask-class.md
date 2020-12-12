---
description: 'Дополнительные сведения о: CMFCTasksPaneTask Class'
title: Класс CMFCTasksPaneTask
ms.date: 11/19/2018
f1_keywords:
- CMFCTasksPaneTask
- AFXTASKSPANE/CMFCTasksPaneTask
- AFXTASKSPANE/CMFCTasksPaneTask::CMFCTasksPaneTask
- AFXTASKSPANE/CMFCTasksPaneTask::SetACCData
- AFXTASKSPANE/CMFCTasksPaneTask::m_bAutoDestroyWindow
- AFXTASKSPANE/CMFCTasksPaneTask::m_bIsBold
- AFXTASKSPANE/CMFCTasksPaneTask::m_dwUserData
- AFXTASKSPANE/CMFCTasksPaneTask::m_hwndTask
- AFXTASKSPANE/CMFCTasksPaneTask::m_nIcon
- AFXTASKSPANE/CMFCTasksPaneTask::m_nWindowHeight
- AFXTASKSPANE/CMFCTasksPaneTask::m_pGroup
- AFXTASKSPANE/CMFCTasksPaneTask::m_rect
- AFXTASKSPANE/CMFCTasksPaneTask::m_strName
- AFXTASKSPANE/CMFCTasksPaneTask::m_uiCommandID
helpviewer_keywords:
- CMFCTasksPaneTask [MFC], CMFCTasksPaneTask
- CMFCTasksPaneTask [MFC], SetACCData
- CMFCTasksPaneTask [MFC], m_bAutoDestroyWindow
- CMFCTasksPaneTask [MFC], m_bIsBold
- CMFCTasksPaneTask [MFC], m_dwUserData
- CMFCTasksPaneTask [MFC], m_hwndTask
- CMFCTasksPaneTask [MFC], m_nIcon
- CMFCTasksPaneTask [MFC], m_nWindowHeight
- CMFCTasksPaneTask [MFC], m_pGroup
- CMFCTasksPaneTask [MFC], m_rect
- CMFCTasksPaneTask [MFC], m_strName
- CMFCTasksPaneTask [MFC], m_uiCommandID
ms.assetid: c5a7513b-cd8f-4e2e-b16f-650e1fe30954
ms.openlocfilehash: 8dad8520c938cae655143464189897d216a5f3ce
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97306772"
---
# <a name="cmfctaskspanetask-class"></a>Класс CMFCTasksPaneTask

`CMFCTasksPaneTask`Класс является вспомогательным классом, представляющим задачи для элемента управления области задач ( [CMFCTasksPane](../../mfc/reference/cmfctaskspane-class.md)). Объект Task представляет элемент в группе задач ( [CMFCTasksPaneTaskGroup](../../mfc/reference/cmfctaskspanetaskgroup-class.md)). Каждая задача может иметь команду, которую платформа выполняет, когда пользователь щелкает задачу, и значок, который присутствует слева от имени задачи.

## <a name="syntax"></a>Синтаксис

```
class CMFCTasksPaneTask : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMFCTasksPaneTask:: CMFCTasksPaneTask](#cmfctaskspanetask)|Создает и инициализирует объект `CMFCTasksPaneTask`.|
|`CMFCTasksPaneTask::~CMFCTasksPaneTask`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCTasksPaneTask:: Сетаккдата](#setaccdata)|Определяет данные о специальных возможностях для текущей задачи.|

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|[CMFCTasksPaneTask:: m_bAutoDestroyWindow](#m_bautodestroywindow)|Определяет, будет ли автоматически уничтожено окно задачи.|
|[CMFCTasksPaneTask:: m_bIsBold](#m_bisbold)|Определяет, будет ли платформа рисовать метку задачи в полужирном тексте.|
|[CMFCTasksPaneTask:: m_dwUserData](#m_dwuserdata)|Содержит определяемые пользователем данные, которые платформа связывает с задачей. Установите нулевое значение, если задача не имеет связанных данных.|
|[CMFCTasksPaneTask:: m_hwndTask](#m_hwndtask)|Маркер окна задачи.|
|[CMFCTasksPaneTask:: m_nIcon](#m_nicon)|Индекс в списке изображений изображения, отображаемого платформой рядом с задачей.|
|[CMFCTasksPaneTask:: m_nWindowHeight](#m_nwindowheight)|Высота окна задачи. Если в задаче нет окна задачи, это значение равно нулю.|
|[CMFCTasksPaneTask:: m_pGroup](#m_pgroup)|Указатель на объект `CMFCTasksPaneTaskGroup` , к которому относится эта задача.|
|[CMFCTasksPaneTask:: m_rect](#m_rect)|Задает ограничивающий прямоугольник задачи.|
|[CMFCTasksPaneTask:: m_strName](#m_strname)|Имя данной задачи.|
|[CMFCTasksPaneTask:: m_uiCommandID](#m_uicommandid)|Указывает идентификатор команды, выполняемой платформой при нажатии пользователем задачи. Если это значение не является допустимым ИДЕНТИФИКАТОРом команды, задача рассматривается как простая метка.|

## <a name="remarks"></a>Комментарии

На следующем рисунке показана группа задач, содержащая три задачи:

![Группа задач, развернутая](../../mfc/reference/media/nexttaskgrpexpand.png "Развернутая группа задач")

> [!NOTE]
> Если у задачи нет допустимого идентификатора команды, она рассматривается как простая метка.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCTasksPaneTask](../../mfc/reference/cmfctaskspanetask-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкстаскспане. h

## <a name="cmfctaskspanetaskcmfctaskspanetask"></a><a name="cmfctaskspanetask"></a> CMFCTasksPaneTask:: CMFCTasksPaneTask

Создает и инициализирует объект `CMFCTasksPaneTask`.

```
CMFCTasksPaneTask(
    CMFCTasksPaneTaskGroup* pGroup,
    LPCTSTR lpszName,
    int nIcon,
    UINT uiCommandID,
    DWORD dwUserData = 0,
    HWND hwndTask = NULL,
    BOOL bAutoDestroyWindow = FALSE,
    int nWindowHeight = 0);
```

### <a name="parameters"></a>Параметры

*пграуп*<br/>
Указывает [CMFCTasksPaneTaskGroup](../../mfc/reference/cmfctaskspanetaskgroup-class.md) , к которому принадлежит задача.

*лпсзнаме*<br/>
Указание названия задачи.

*никон*<br/>
Указывает индекс изображения задачи в списке изображений.

*уикоммандид*<br/>
Указывает идентификатор команды, которая выполняется при нажатии на задачу.

*двусердата*<br/>
Определяемые пользователем данные.

*хвндтаск*<br/>
Указывает маркер для окна задачи.

*баутодестройвиндов*<br/>
Если значение — TRUE, окно задачи будет удалено автоматически.

*нвиндовхеигхт*<br/>
Задает высоту окна задачи.

### <a name="remarks"></a>Комментарии

## <a name="cmfctaskspanetaskm_bautodestroywindow"></a><a name="m_bautodestroywindow"></a> CMFCTasksPaneTask:: m_bAutoDestroyWindow

Определяет, будет ли автоматически уничтожено окно задачи.

```
BOOL m_bAutoDestroyWindow;
```

### <a name="remarks"></a>Комментарии

Задайте значение TRUE, чтобы указать, что окно задач ( [CMFCTasksPaneTask:: m_hwndTask](#m_hwndtask)) следует автоматически уничтожить; в противном случае — значение FALSE.

## <a name="cmfctaskspanetaskm_bisbold"></a><a name="m_bisbold"></a> CMFCTasksPaneTask:: m_bIsBold

Определяет, отображается ли метка задачи полужирным шрифтом.

```
BOOL m_bIsBold;
```

### <a name="remarks"></a>Комментарии

Установите для этого элемента значение TRUE, чтобы в метке задачи отображался полужирный текст.

## <a name="cmfctaskspanetaskm_dwuserdata"></a><a name="m_dwuserdata"></a> CMFCTasksPaneTask:: m_dwUserData

Содержит определяемые пользователем данные, связанные с задачей. Установите нулевое значение, если с задачей не связаны никакие данные.

```
DWORD m_dwUserData;
```

### <a name="remarks"></a>Комментарии

## <a name="cmfctaskspanetaskm_hwndtask"></a><a name="m_hwndtask"></a> CMFCTasksPaneTask:: m_hwndTask

Маркер окна задачи.

```
HWND m_hwndTask;
```

### <a name="remarks"></a>Комментарии

Чтобы добавить окно задачи, вызовите [CMFCTasksPane:: аддвиндов](../../mfc/reference/cmfctaskspane-class.md#addwindow).

## <a name="cmfctaskspanetaskm_nicon"></a><a name="m_nicon"></a> CMFCTasksPaneTask:: m_nIcon

Позиция индекса в списке изображений, которая определяет изображение, отображаемое рядом с указанной задачей.

```
int m_nIcon;
```

### <a name="remarks"></a>Комментарии

Список изображений задается с помощью [CMFCTasksPane:: сетиконслист](../../mfc/reference/cmfctaskspane-class.md#seticonslist).

Установите значение `m_nIcon` -1, если требуется отобразить задачу без изображения.

## <a name="cmfctaskspanetaskm_nwindowheight"></a><a name="m_nwindowheight"></a> CMFCTasksPaneTask:: m_nWindowHeight

Высота окна задачи. Если в задаче нет окна задачи, это значение равно нулю.

```
int m_nWindowHeight;
```

### <a name="remarks"></a>Комментарии

## <a name="cmfctaskspanetaskm_pgroup"></a><a name="m_pgroup"></a> CMFCTasksPaneTask:: m_pGroup

Указатель на [CMFCTasksPaneTaskGroup](../../mfc/reference/cmfctaskspanetaskgroup-class.md) , к которому принадлежит эта задача.

```
CMFCTasksPaneTaskGroup* m_pGroup;
```

### <a name="remarks"></a>Комментарии

У каждой задачи должна быть родительская группа. Группы добавляются в область задач путем вызова [CMFCTasksPane:: addgroup](../../mfc/reference/cmfctaskspane-class.md#addgroup).

## <a name="cmfctaskspanetaskm_rect"></a><a name="m_rect"></a> CMFCTasksPaneTask:: m_rect

Задает ограничивающий прямоугольник задачи.

```
CRect m_rect;
```

### <a name="remarks"></a>Комментарии

Это значение вычисляется платформой при прорисовке задачи.

## <a name="cmfctaskspanetaskm_strname"></a><a name="m_strname"></a> CMFCTasksPaneTask:: m_strName

Имя данной задачи.

```
CString m_strName;
```

### <a name="remarks"></a>Комментарии

## <a name="cmfctaskspanetaskm_uicommandid"></a><a name="m_uicommandid"></a> CMFCTasksPaneTask:: m_uiCommandID

Указывает идентификатор команды, которая выполняется, когда пользователь щелкает задачу. Если это значение не является допустимым ИДЕНТИФИКАТОРом команды, задача рассматривается как простая метка.

```
UINT m_uiCommandID;
```

### <a name="remarks"></a>Комментарии

## <a name="cmfctaskspanetasksetaccdata"></a><a name="setaccdata"></a> CMFCTasksPaneTask:: Сетаккдата

Определяет данные о специальных возможностях для текущей задачи.

```
virtual BOOL SetACCData(
    CWnd* pParent,
    CAccessibilityData& data);
```

### <a name="parameters"></a>Параметры

*ппарент*<br/>
окне Представляет родительское окно текущей задачи.

*data*<br/>
заполняет Объект типа `CAccessibilityData` , заполненный данными о специальных возможностях текущей задачи.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если параметр *данных* успешно заполнен данными о специальных возможностях текущей задачи; в противном случае — значение FALSE.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[CObject, класс](../../mfc/reference/cobject-class.md)
