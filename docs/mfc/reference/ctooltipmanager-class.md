---
description: 'Дополнительные сведения о: Ктултипманажер Class'
title: Класс Ктултипманажер
ms.date: 11/04/2016
f1_keywords:
- CTooltipManager
- AFXTOOLTIPMANAGER/CTooltipManager
- AFXTOOLTIPMANAGER/CTooltipManager::CreateToolTip
- AFXTOOLTIPMANAGER/CTooltipManager::DeleteToolTip
- AFXTOOLTIPMANAGER/CTooltipManager::SetTooltipParams
- AFXTOOLTIPMANAGER/CTooltipManager::SetTooltipText
- AFXTOOLTIPMANAGER/CTooltipManager::UpdateTooltips
helpviewer_keywords:
- CTooltipManager [MFC], CreateToolTip
- CTooltipManager [MFC], DeleteToolTip
- CTooltipManager [MFC], SetTooltipParams
- CTooltipManager [MFC], SetTooltipText
- CTooltipManager [MFC], UpdateTooltips
ms.assetid: c71779d7-8b6e-47ef-8500-d4552731fe86
ms.openlocfilehash: 0ec6d691abbceb7026fe9656c17ff899f1d07759
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318550"
---
# <a name="ctooltipmanager-class"></a>Класс Ктултипманажер

Хранит сведения среды выполнения о подсказках. Экземпляр класса `CTooltipManager` создается один раз для каждого приложения.

## <a name="syntax"></a>Синтаксис

```
class CTooltipManager : public CObject
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CTooltipManager::CreateToolTip](#createtooltip)|Создает элемент управления "Всплывающая подсказка" для указанных типов  элементов управления Windows.|
|[CTooltipManager::DeleteToolTip](#deletetooltip)|Удаляет элемент управления "Всплывающая подсказка".|
|[CTooltipManager::SetTooltipParams](#settooltipparams)|Настраивает внешний вид элемента управления "Всплывающая подсказка" для указанных типов элементов управления Windows.|
|[CTooltipManager::SetTooltipText](#settooltiptext)|Задает текст и описание для элемента управления "Всплывающая подсказка".|
|[CTooltipManager::UpdateTooltips](#updatetooltips)||

## <a name="remarks"></a>Комментарии

Используйте [класс кмфктултипктрл](../../mfc/reference/cmfctooltipctrl-class.md), `CMFCToolTipInfo` и `CTooltipManager` вместе, чтобы реализовать настраиваемые подсказки в приложении. Пример использования этих классов подсказок см. в разделе [класс кмфктултипктрл](../../mfc/reference/cmfctooltipctrl-class.md) .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CTooltipManager](../../mfc/reference/ctooltipmanager-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкстултипманажер. h

## <a name="ctooltipmanagercreatetooltip"></a><a name="createtooltip"></a> Ктултипманажер:: Креатетултип

Создает элемент управления ToolTip.

```
static BOOL CreateToolTip(
    CToolTipCtrl*& pToolTip,
    CWnd* pWndParent,
    UINT nType);
```

### <a name="parameters"></a>Параметры

*птултип*<br/>
заполняет Ссылка на указатель подсказки. Он указывает на только что созданную подсказку, когда функция возвращает значение.

*пвндпарент*<br/>
окне Родительский элемент подсказки.

*nType*<br/>
окне Тип подсказки.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если подсказка успешно создана.

### <a name="remarks"></a>Комментарии

Необходимо вызвать метод [ктултипманажер::D елететултип](#deletetooltip) , чтобы удалить элемент управления ToolTip, который передается обратно в *птултип*.

[Ктултипманажер](../../mfc/reference/ctooltipmanager-class.md) задает параметры визуального отображения каждой создаваемой всплывающей подсказки на основе типа подсказки, которую *nуведомления* указывает. Чтобы изменить параметры для одного или нескольких типов подсказок, вызовите метод [ктултипманажер:: сеттултиппарамс](#settooltipparams).

Допустимые типы подсказок перечислены в следующей таблице.

|Тип подсказки|Категория элемента управления|Примеры типов|
|------------------|----------------------|-------------------|
|AFX_TOOLTIP_TYPE_BUTTON|Кнопка.|CMFCButton|
|AFX_TOOLTIP_TYPE_CAPTIONBAR|Заголовок.|CMFCCaptionBar|
|AFX_TOOLTIP_TYPE_DEFAULT|Любой элемент управления, не помещается в другую категорию.|Отсутствует.|
|AFX_TOOLTIP_TYPE_DOCKBAR|Закрепляемая область.|CDockablePane|
|AFX_TOOLTIP_TYPE_EDIT|Текстовое поле.|Отсутствует.|
|AFX_TOOLTIP_TYPE_MINIFRAME|Плавающего.|CPaneFrameWnd|
|AFX_TOOLTIP_TYPE_PLANNER|Планировщик.|Отсутствует.|
|AFX_TOOLTIP_TYPE_RIBBON|Панель ленты.|CMFCRibbonBar, Кмфкриббонпанелменубар|
|AFX_TOOLTIP_TYPE_TAB|Элемент управления "Вкладка".|CMFCTabCtrl|
|AFX_TOOLTIP_TYPE_TOOLBAR|Панель инструментов.|CMFCToolBar, CMFCPopupMenuBar|
|AFX_TOOLTIP_TYPE_TOOLBOX|Панель элементов.|Отсутствует.|

## <a name="ctooltipmanagerdeletetooltip"></a><a name="deletetooltip"></a> Ктултипманажер::D Елететултип

Удаляет элемент управления "Всплывающая подсказка".

```
static void DeleteToolTip(CToolTipCtrl*& pToolTip);
```

### <a name="parameters"></a>Параметры

*птултип*<br/>
[вход, выход] Ссылка на указатель на подсказку, которую необходимо уничтожить.

### <a name="remarks"></a>Комментарии

Вызывайте этот метод для каждого [класса CToolTipCtrl](../../mfc/reference/ctooltipctrl-class.md) , созданного с помощью [Ктултипманажер:: креатетултип](#createtooltip). Родительский элемент управления должен вызывать этот метод из своего `OnDestroy` обработчика. Это необходимо для правильного удаления всплывающей подсказки из платформы. Этот метод задает для *птултип* значение null перед возвратом.

## <a name="ctooltipmanagersettooltipparams"></a><a name="settooltipparams"></a> Ктултипманажер:: Сеттултиппарамс

Настраивает внешний вид элемента управления ToolTip для указанных типов элементов управления Windows.

```cpp
void SetTooltipParams(
    UINT nTypes,
    CRuntimeClass* pRTC=RUNTIME_CLASS(CMFCToolTipCtrl),
    CMFCToolTipInfo* pParams=NULL);
```

### <a name="parameters"></a>Параметры

*нтипес*<br/>
окне Задает типы элементов управления.

*pRTC*<br/>
окне Класс среды выполнения пользовательской подсказки.

*ппарамс*<br/>
окне Параметры подсказки.

### <a name="remarks"></a>Комментарии

Этот метод задает класс среды выполнения и начальные параметры, используемые [ктултипманажер](../../mfc/reference/ctooltipmanager-class.md) при создании подсказок. Когда элемент управления вызывает [ктултипманажер:: креатетултип](#createtooltip) и передает тип подсказки, который является одним из типов, указанных в *нтипес*, диспетчер подсказок создает элемент управления ToolTip, который является экземпляром класса среды выполнения, заданным *пртк* , и передает параметры, указанные в *ппарамс* , в новую подсказку.

При вызове этого метода все существующие владельцы подсказок получают AFX_WM_UPDATETOOLTIPS сообщение и должны повторно создавать свои подсказки с помощью [ктултипманажер:: креатетултип](#createtooltip).

*нтипес* может быть любым сочетанием допустимых типов подсказок, которые используются [Ктултипманажер:: креатетултип](#createtooltip) или могут быть AFX_TOOLTIP_TYPE_ALL. При передаче AFX_TOOLTIP_TYPE_ALL затрагиваются все типы всплывающих подсказок.

### <a name="example"></a>Пример

В следующем примере показано, как использовать `SetTooltipParams` метод `CTooltipManager` класса. Этот фрагмент кода входит в состав [примера Draw Client](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_DrawClient#11](../../mfc/reference/codesnippet/cpp/ctooltipmanager-class_1.cpp)]

## <a name="ctooltipmanagersettooltiptext"></a><a name="settooltiptext"></a> Ктултипманажер:: Сеттултиптекст

Задает текст и описание всплывающей подсказки.

```
static void SetTooltipText(
    TOOLINFO* pTI,
    CToolTipCtrl* pToolTip,
    UINT nType,
    const CString strText,
    LPCTSTR lpszDescr=NULL);
```

### <a name="parameters"></a>Параметры

*пти*<br/>
окне Указатель на объект ТУЛИНФО.

*птултип*<br/>
[вход, выход] Указатель на элемент управления ToolTip, для которого необходимо задать текст и описание.

*nType*<br/>
окне Задает тип элемента управления, с которым связана эта подсказка.

*стртекст*<br/>
окне Текст, заданный в качестве текста подсказки.

*лпсздескр*<br/>
окне Указатель на описание подсказки. Может иметь значение NULL.

### <a name="remarks"></a>Комментарии

Значение параметра *nуведомления* должно совпадать с параметром *nуведомления* в [ктултипманажер:: креатетултип](#createtooltip) при создании подсказки.

## <a name="ctooltipmanagerupdatetooltips"></a><a name="updatetooltips"></a> Ктултипманажер:: Упдатетултипс

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```cpp
void UpdateTooltips();
```

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфктултипктрл](../../mfc/reference/cmfctooltipctrl-class.md)<br/>
[Класс Кмфктултипинфо](../../mfc/reference/cmfctooltipinfo-class.md)
