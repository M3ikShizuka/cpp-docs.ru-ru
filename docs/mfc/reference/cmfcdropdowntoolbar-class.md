---
description: 'Дополнительные сведения о: Кмфкдропдовнтулбар Class'
title: Класс Кмфкдропдовнтулбар
ms.date: 11/19/2018
f1_keywords:
- CMFCDropDownToolBar
- AFXDROPDOWNTOOLBAR/CMFCDropDownToolBar
- AFXDROPDOWNTOOLBAR/CMFCDropDownToolBar::AllowShowOnPaneMenu
- AFXDROPDOWNTOOLBAR/CMFCDropDownToolBar::LoadBitmap
- AFXDROPDOWNTOOLBAR/CMFCDropDownToolBar::LoadToolBar
- AFXDROPDOWNTOOLBAR/CMFCDropDownToolBar::OnLButtonUp
- AFXDROPDOWNTOOLBAR/CMFCDropDownToolBar::OnMouseMove
- AFXDROPDOWNTOOLBAR/CMFCDropDownToolBar::OnSendCommand
- AFXDROPDOWNTOOLBAR/CMFCDropDownToolBar::OnUpdateCmdUI
helpviewer_keywords:
- CMFCDropDownToolBar [MFC], AllowShowOnPaneMenu
- CMFCDropDownToolBar [MFC], LoadBitmap
- CMFCDropDownToolBar [MFC], LoadToolBar
- CMFCDropDownToolBar [MFC], OnLButtonUp
- CMFCDropDownToolBar [MFC], OnMouseMove
- CMFCDropDownToolBar [MFC], OnSendCommand
- CMFCDropDownToolBar [MFC], OnUpdateCmdUI
ms.assetid: 78818ec5-83ce-42fa-a0d4-2d9d5ecc8770
ms.openlocfilehash: 158562829cb5bbebfb9a858d34751c56bdf46ed8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97293993"
---
# <a name="cmfcdropdowntoolbar-class"></a>Класс Кмфкдропдовнтулбар

Панель инструментов, которая появляется, когда пользователь нажимает и удерживает кнопку верхнего уровня панели инструментов.

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```
class CMFCDropDownToolBar : public CMFCToolBar
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкдропдовнтулбар:: Алловшовонпанемену](#allowshowonpanemenu)|(Переопределяет `CPane::AllowShowOnPaneMenu`.)|
|[Кмфкдропдовнтулбар:: Лоадбитмап](#loadbitmap)|(Переопределяет [CMFCToolBar:: лоадбитмап](../../mfc/reference/cmfctoolbar-class.md#loadbitmap).)|
|[Кмфкдропдовнтулбар:: Лоадтулбар](#loadtoolbar)|(Переопределяет [CMFCToolBar:: лоадтулбар](../../mfc/reference/cmfctoolbar-class.md#loadtoolbar).)|
|[Кмфкдропдовнтулбар:: Онлбуттонуп](#onlbuttonup)||
|[Кмфкдропдовнтулбар:: OnMouseMove](#onmousemove)||
|[Кмфкдропдовнтулбар:: Онсендкомманд](#onsendcommand)|(Переопределяет `CMFCToolBar::OnSendCommand`.)|
|[Кмфкдропдовнтулбар:: Онупдатекмдуи](#onupdatecmdui)|(Переопределяет [CMFCToolBar:: онупдатекмдуи](cmfctoolbar-class.md).|

### <a name="remarks"></a>Комментарии

`CMFCDropDownToolBar`Объект сочетает визуальный вид панели инструментов с поведением всплывающего меню. Когда пользователь нажимает и удерживает кнопку раскрывающегося списка на панели инструментов (см. [класс кмфкдропдовнтулбарбуттон](../../mfc/reference/cmfcdropdowntoolbarbutton-class.md)), появляется раскрывающийся список панелей инструментов, и пользователь может выбрать кнопку из раскрывающейся панели инструментов, прокрутите ее и отпустив кнопку мыши. После того как пользователь нажмет кнопку на раскрывающейся панели инструментов, эта кнопка отображается как текущая кнопка на панели инструментов верхнего уровня.

Раскрывающийся список инструментов нельзя настроить или закрепить, и он не имеет состояния разрыва.

На следующем рисунке показан `CMFCDropDownToolBar` объект:

![Пример CMFCDropDownToolbar](../../mfc/reference/media/cmfcdropdown.png "Пример CMFCDropDownToolbar")

`CMFCDropDownToolBar`Объект создается так же, как и обычная панель инструментов (см. раздел [Класс CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md)).

Чтобы вставить раскрывающийся список инструментов в родительскую панель инструментов, сделайте следующее:

1. Зарезервируйте идентификатор фиктивного ресурса для кнопки на родительском ресурсе панели инструментов.

2. Создайте `CMFCDropDownToolBarButton` объект, содержащий раскрывающуюся панель инструментов (Дополнительные сведения см. в разделе [кмфкдропдовнтулбарбуттон:: кмфкдропдовнтулбарбуттон](../../mfc/reference/cmfcdropdowntoolbarbutton-class.md#cmfcdropdowntoolbarbutton)).

3. Замените фиктивную кнопку на объект с `CMFCDropDownToolBarButton` помощью [CMFCToolBar:: реплацебуттон](../../mfc/reference/cmfctoolbar-class.md#replacebutton).

Дополнительные сведения о кнопках панели инструментов см. [в разделе Пошаговое руководство. размещение элементов управления на панелях инструментов](../../mfc/walkthrough-putting-controls-on-toolbars.md). Пример раскрывающейся панели инструментов см. в примере проекта Висуалстудиодемо.

## <a name="example"></a>Пример

В следующем примере показано, как использовать `Create` метод в `CMFCDropDownToolBar` классе. Этот фрагмент кода является частью [демонстрационного примера Visual Studio](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_VisualStudioDemo#29](../../mfc/codesnippet/cpp/cmfcdropdowntoolbar-class_1.h)]
[!code-cpp[NVC_MFC_VisualStudioDemo#30](../../mfc/codesnippet/cpp/cmfcdropdowntoolbar-class_2.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CBasePane](../../mfc/reference/cbasepane-class.md)

[CPane](../../mfc/reference/cpane-class.md)

[кмфкбасетулбар](../../mfc/reference/cmfcbasetoolbar-class.md)

[CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md)

[CMFCDropDownToolBar](../../mfc/reference/cmfcdropdowntoolbar-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** afxdropdowntoolbar.h

## <a name="cmfcdropdowntoolbarallowshowonpanemenu"></a><a name="allowshowonpanemenu"></a> Кмфкдропдовнтулбар:: Алловшовонпанемену

```
virtual BOOL AllowShowOnPaneMenu() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcdropdowntoolbarloadbitmap"></a><a name="loadbitmap"></a> Кмфкдропдовнтулбар:: Лоадбитмап

Загружает изображения значков панели инструментов из ресурсов приложения.

```
virtual BOOL LoadBitmap(
    UINT uiResID,
    UINT uiColdResID=0,
    UINT uiMenuResID=0,
    BOOL bLocked=FALSE,
    UINT uiDisabledResID=0,
    UINT uiMenuDisabledResID=0);
```

### <a name="parameters"></a>Параметры

*уиресид*<br/>
окне Идентификатор ресурса точечного рисунка, который ссылается на изображения горячих панелей инструментов.

*уиколдресид*<br/>
окне Идентификатор ресурса точечного рисунка, который относится к изображениям холодный панели инструментов.

*уименуресид*<br/>
окне Идентификатор ресурса точечного рисунка, который ссылается на обычные изображения меню.

*Блокирует*<br/>
окне Значение TRUE, чтобы заблокировать панель инструментов; в противном случае — FALSE.

*уидисабледресид*<br/>
окне Идентификатор ресурса точечного рисунка, который ссылается на отключенные изображения панели инструментов.

*уименудисабледресид*<br/>
окне Идентификатор ресурса точечного рисунка, который относится к отключенным образам меню.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если метод выполнен успешно; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Метод [CMFCToolBar::LoadToolBarEx](../../mfc/reference/cmfctoolbar-class.md#loadtoolbarex) вызывает этот метод, чтобы загрузить изображения, связанные с панелью инструментов. Переопределите этот метод для выполнения пользовательской загрузки графических ресурсов.

Вызовите метод `LoadBitmapEx` , чтобы загрузить дополнительные изображения после создания панели инструментов.

## <a name="cmfcdropdowntoolbarloadtoolbar"></a><a name="loadtoolbar"></a> Кмфкдропдовнтулбар:: Лоадтулбар

```
virtual BOOL LoadToolBar(
    UINT uiResID,
    UINT uiColdResID = 0,
    UINT uiMenuResID = 0,
    BOOL = FALSE,
    UINT uiDisabledResID = 0,
    UINT uiMenuDisabledResID = 0,
    UINT uiHotResID = 0);
```

### <a name="parameters"></a>Параметры

окне *уиресид*<br/>

окне *уиколдресид*<br/>

окне *уименуресид*<br/>

окне *Bool (логическое* )<br/>

окне *уидисабледресид*<br/>

окне *уименудисабледресид*<br/>

окне *уихотресид*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcdropdowntoolbaronlbuttonup"></a><a name="onlbuttonup"></a> Кмфкдропдовнтулбар:: Онлбуттонуп

```
afx_msg void OnLButtonUp(
    UINT nFlags,
    CPoint point);
```

### <a name="parameters"></a>Параметры

окне *нфлагс*<br/>

окне *точка*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcdropdowntoolbaronmousemove"></a><a name="onmousemove"></a> Кмфкдропдовнтулбар:: OnMouseMove

```
afx_msg void OnMouseMove(
    UINT nFlags,
    CPoint point);
```

### <a name="parameters"></a>Параметры

окне *нфлагс*<br/>

окне *точка*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcdropdowntoolbaronsendcommand"></a><a name="onsendcommand"></a> Кмфкдропдовнтулбар:: Онсендкомманд

```
virtual BOOL OnSendCommand(const CMFCToolBarButton* pButton);
```

### <a name="parameters"></a>Параметры

окне *пбуттон*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcdropdowntoolbaronupdatecmdui"></a><a name="onupdatecmdui"></a> Кмфкдропдовнтулбар:: Онупдатекмдуи

```
virtual void OnUpdateCmdUI(
    CFrameWnd* pTarget,
    BOOL bDisableIfNoHndler);
```

### <a name="parameters"></a>Параметры

окне *птаржет*<br/>

окне *бдисаблеифнохндлер*<br/>

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md)<br/>
[CMFCToolBar:: Create](../../mfc/reference/cmfctoolbar-class.md#create)<br/>
[CMFCToolBar:: Реплацебуттон](../../mfc/reference/cmfctoolbar-class.md#replacebutton)<br/>
[Класс Кмфкдропдовнтулбарбуттон](../../mfc/reference/cmfcdropdowntoolbarbutton-class.md)<br/>
[Пошаговое руководство. размещение элементов управления на панелях инструментов](../../mfc/walkthrough-putting-controls-on-toolbars.md)
