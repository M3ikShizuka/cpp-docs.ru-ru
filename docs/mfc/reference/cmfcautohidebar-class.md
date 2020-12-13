---
description: 'Дополнительные сведения о: CMFCAutoHideBar Class'
title: Класс CMFCAutoHideBar
ms.date: 10/18/2018
f1_keywords:
- CMFCAutoHideBar
- AFXAUTOHIDEBAR/CMFCAutoHideBar
- AFXAUTOHIDEBAR/CMFCAutoHideBar::CMFCAutoHideBar
- AFXAUTOHIDEBAR/CMFCAutoHideBar::AddAutoHideWindow
- AFXAUTOHIDEBAR/CMFCAutoHideBar::AllowShowOnPaneMenu
- AFXAUTOHIDEBAR/CMFCAutoHideBar::CalcFixedLayout
- AFXAUTOHIDEBAR/CMFCAutoHideBar::Create
- AFXAUTOHIDEBAR/CMFCAutoHideBar::GetFirstAHWindow
- AFXAUTOHIDEBAR/CMFCAutoHideBar::GetVisibleCount
- AFXAUTOHIDEBAR/CMFCAutoHideBar::OnShowControlBarMenu
- AFXAUTOHIDEBAR/CMFCAutoHideBar::RemoveAutoHideWindow
- AFXAUTOHIDEBAR/CMFCAutoHideBar::SetActiveInGroup
- AFXAUTOHIDEBAR/CMFCAutoHideBar::SetRecentVisibleState
- AFXAUTOHIDEBAR/CMFCAutoHideBar::ShowAutoHideWindow
- AFXAUTOHIDEBAR/CMFCAutoHideBar::StretchPane
- AFXAUTOHIDEBAR/CMFCAutoHideBar::UnSetAutoHideMode
- AFXAUTOHIDEBAR/CMFCAutoHideBar::UpdateVisibleState
- AFXAUTOHIDEBAR/CMFCAutoHideBar::m_nShowAHWndDelay
helpviewer_keywords:
- CMFCAutoHideBar [MFC], CMFCAutoHideBar
- CMFCAutoHideBar [MFC], AddAutoHideWindow
- CMFCAutoHideBar [MFC], AllowShowOnPaneMenu
- CMFCAutoHideBar [MFC], CalcFixedLayout
- CMFCAutoHideBar [MFC], Create
- CMFCAutoHideBar [MFC], GetFirstAHWindow
- CMFCAutoHideBar [MFC], GetVisibleCount
- CMFCAutoHideBar [MFC], OnShowControlBarMenu
- CMFCAutoHideBar [MFC], RemoveAutoHideWindow
- CMFCAutoHideBar [MFC], SetActiveInGroup
- CMFCAutoHideBar [MFC], SetRecentVisibleState
- CMFCAutoHideBar [MFC], ShowAutoHideWindow
- CMFCAutoHideBar [MFC], StretchPane
- CMFCAutoHideBar [MFC], UnSetAutoHideMode
- CMFCAutoHideBar [MFC], UpdateVisibleState
- CMFCAutoHideBar [MFC], m_nShowAHWndDelay
ms.assetid: 54c8d84f-de64-4efd-8a47-3ea0ade40a70
ms.openlocfilehash: d7cea85a71b8390520d1345e12000aa700026269
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336596"
---
# <a name="cmfcautohidebar-class"></a>Класс CMFCAutoHideBar

Класс `CMFCAutoHideBar` — это специальный класс панели инструментов, реализующий возможность автоматического скрытия.

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```
class CMFCAutoHideBar : public CPane
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMFCAutoHideBar::CMFCAutoHideBar](#cmfcautohidebar)||

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCAutoHideBar::AddAutoHideWindow](#addautohidewindow)||
|[CMFCAutoHideBar::AllowShowOnPaneMenu](#allowshowonpanemenu)|(Переопределяет `CPane::AllowShowOnPaneMenu`.)|
|[CMFCAutoHideBar::CalcFixedLayout](#calcfixedlayout)|(Переопределяет [CBasePane:: калкфикседлайаут](../../mfc/reference/cbasepane-class.md#calcfixedlayout).)|
|[CMFCAutoHideBar::Create](#create)|Создает панель элементов управления и прикрепляет ее к объекту [CPane](../../mfc/reference/cpane-class.md) . (Переопределяет [CPane:: Create](../../mfc/reference/cpane-class.md#create).)|
|[CMFCAutoHideBar::GetFirstAHWindow](#getfirstahwindow)||
|[CMFCAutoHideBar::GetVisibleCount](#getvisiblecount)||
|[CMFCAutoHideBar::OnShowControlBarMenu](#onshowcontrolbarmenu)|Вызывается платформой непосредственно перед отображением меню особой панели. (Переопределяет [CPane:: оншовконтролбармену](../../mfc/reference/cpane-class.md#onshowcontrolbarmenu).)|
|[CMFCAutoHideBar::RemoveAutoHideWindow](#removeautohidewindow)||
|[CMFCAutoHideBar::SetActiveInGroup](#setactiveingroup)|(Переопределяет [CPane:: сетактивеинграуп](../../mfc/reference/cpane-class.md#setactiveingroup).)|
|[CMFCAutoHideBar::SetRecentVisibleState](#setrecentvisiblestate)||
|[CMFCAutoHideBar::ShowAutoHideWindow](#showautohidewindow)||
|[CMFCAutoHideBar::StretchPane](#stretchpane)|Растягивает панель по вертикали или горизонтали. (Переопределяет [CBasePane:: стретчпане](../../mfc/reference/cbasepane-class.md#stretchpane).)|
|[CMFCAutoHideBar::UnSetAutoHideMode](#unsetautohidemode)||
|[CMFCAutoHideBar::UpdateVisibleState](#updatevisiblestate)||

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|[CMFCAutoHideBar::m_nShowAHWndDelay](#m_nshowahwnddelay)|Время задержки между моментом, когда пользователь наводит указатель мыши на [Класс CMFCAutoHideButton](../../mfc/reference/cmfcautohidebutton-class.md) и в момент, когда платформа отображает связанное окно.|

## <a name="remarks"></a>Комментарии

Когда пользователь переключает область закрепления в режим автоматического скрытия, платформа автоматически создает объект `CMFCAutoHideBar`. Он также создает необходимые объекты [CAutoHideDockSite](../../mfc/reference/cautohidedocksite-class.md) и [CMFCAutoHideButton](../../mfc/reference/cmfcautohidebutton-class.md) . Каждый объект `CAutoHideDockSite` связан с определенным объектом `CMFCAutoHideButton`.

Класс `CMFCAutoHideBar` реализует отображение объекта `CAutoHideDockSite`, когда пользователь наводит указатель мыши на объект `CMFCAutoHideButton`. Когда панель инструментов получает сообщение WM_MOUSEMOVE, объект `CMFCAutoHideBar` запускает таймер. Когда отсчет завершается, панели инструментов отправляется уведомление о событии WM_TIMER. Панель инструментов обрабатывает это событие, проверяя, расположен ли указатель мыши на той же кнопке автоматического скрытия, на которой он находился при запуске таймера. В случае положительного результата отображается прикрепленный объект `CAutoHideDockSite`.

Длительность задержки таймера можно регулировать с помощью параметра `m_nShowAHWndDelay`. Значение по умолчанию составляет 400 мс.

## <a name="example"></a>Пример

В этом примере демонстрируется создание объекта `CMFCAutoHideBar` и использование его метода `GetDockSiteRow`.

[!code-cpp[NVC_MFC_RibbonApp#26](../../mfc/reference/codesnippet/cpp/cmfcautohidebar-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CBasePane](../../mfc/reference/cbasepane-class.md)

[CPane](../../mfc/reference/cpane-class.md)

[CMFCAutoHideBar](../../mfc/reference/cmfcautohidebar-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** afxautohidebar.h

## <a name="cmfcautohidebaraddautohidewindow"></a><a name="addautohidewindow"></a> CMFCAutoHideBar:: Аддаутохидевиндов

Добавляет в окно `CDockablePane` функциональные возможности, которые позволяют ему выполнять автоматическое скрытие.

```
CMFCAutoHideButton* AddAutoHideWindow(
    CDockablePane* pAutoHideWnd,
    DWORD dwAlignment);
```

### <a name="parameters"></a>Параметры

*паутохидевнд*<br/>
окне Окно, которое необходимо скрыть.

*двалигнмент*<br/>
окне Значение, указывающее выравнивание кнопки автоматического скрытия с окном приложения.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Параметр *двалигнмент* указывает, где находится кнопка автоматического скрытия в приложении. Параметру может быть присвоено одно из следующих значений:

- CBRS_ALIGN_LEFT

- CBRS_ALIGN_RIGHT

- CBRS_ALIGN_TOP

- CBRS_ALIGN_BOTTOM

## <a name="cmfcautohidebarallowshowonpanemenu"></a><a name="allowshowonpanemenu"></a> CMFCAutoHideBar:: Алловшовонпанемену

```
virtual BOOL AllowShowOnPaneMenu() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebarcalcfixedlayout"></a><a name="calcfixedlayout"></a> CMFCAutoHideBar:: Калкфикседлайаут

```
virtual CSize CalcFixedLayout(
    BOOL bStretch,
    BOOL bHorz);
```

### <a name="parameters"></a>Параметры

окне *бстретч*<br/>

окне *бхорз*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebarcmfcautohidebar"></a><a name="cmfcautohidebar"></a> CMFCAutoHideBar:: CMFCAutoHideBar

Создает объект CMFCAutoHideBar.

```
CMFCAutoHideBar();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebarcreate"></a><a name="create"></a> CMFCAutoHideBar:: Create

```
virtual BOOL Create(
    LPCTSTR lpszClassName,
    DWORD dwStyle,
    const RECT& rect,
    CWnd* pParentWnd,
    UINT nID,
    DWORD dwControlBarStyle = AFX_DEFAULT_PANE_STYLE,
    CCreateContext* pContext = NULL);
```

### <a name="parameters"></a>Параметры

*лпсзкласснаме*<br/>

*двстиле*<br/>

*rect*<br/>

*ппарентвнд*<br/>

*nID*<br/>

*двконтролбарстиле*<br/>

*pContext*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebargetfirstahwindow"></a><a name="getfirstahwindow"></a> CMFCAutoHideBar:: Жетфирстахвиндов

Возвращает указатель на первое окно автоматического скрытия в приложении.

```
CDockablePane* GetFirstAHWindow();
```

### <a name="return-value"></a>Возвращаемое значение

Первое окно автоматического скрытия в приложении или значение NULL, если его не существует.

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebargetvisiblecount"></a><a name="getvisiblecount"></a> CMFCAutoHideBar:: Жетвисиблекаунт

Получает количество видимых кнопок автоматического скрытия.

```
int GetVisibleCount();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает количество видимых кнопок автоматического скрытия.

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebarm_nshowahwnddelay"></a><a name="m_nshowahwnddelay"></a> CMFCAutoHideBar:: m_nShowAHWndDelay

Время задержки между моментом, когда пользователь наводит указатель мыши на [Класс CMFCAutoHideButton](../../mfc/reference/cmfcautohidebutton-class.md) и в момент, когда платформа отображает связанное окно.

```
int CMFCAutoHideBar::m_nShowAHWndDelay = 400;
```

### <a name="remarks"></a>Комментарии

Когда пользователь наводит указатель мыши на, возникает `CMFCAutoHideButton` небольшая задержка, прежде чем платформа отобразит связанное окно. Этот параметр определяет продолжительность задержки в миллисекундах.

## <a name="cmfcautohidebaronshowcontrolbarmenu"></a><a name="onshowcontrolbarmenu"></a> CMFCAutoHideBar:: Оншовконтролбармену

```
virtual BOOL OnShowControlBarMenu(CPoint);
```

### <a name="parameters"></a>Параметры

[in] *CPoint*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebarremoveautohidewindow"></a><a name="removeautohidewindow"></a> CMFCAutoHideBar:: Ремовеаутохидевиндов

Удаляет и уничтожает окно автоматического скрытия.

```
    BOOL RemoveAutoHideWindow(CDockablePane* pAutoHideWnd);
```

### <a name="parameters"></a>Параметры

CDockablePane * *паутохидевнд* . окно автоматического скрытия для удаления.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если успешно; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebarsetactiveingroup"></a><a name="setactiveingroup"></a> CMFCAutoHideBar:: Сетактивеинграуп

Помечает строку автоматического скрытия как активную.

```
virtual void SetActiveInGroup(BOOL bActive);
```

### <a name="parameters"></a>Параметры

окне BOOL *бактиве* true для установки в активное значение; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

См. раздел [CPane::SetActiveInGroup](../../mfc/reference/cpane-class.md#setactiveingroup).

## <a name="cmfcautohidebarsetrecentvisiblestate"></a><a name="setrecentvisiblestate"></a> CMFCAutoHideBar:: Сетрецентвисиблестате

```cpp
void SetRecentVisibleState(BOOL bState);
```

### <a name="parameters"></a>Параметры

*bState*<br/>
окне Заданное состояние.

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebarshowautohidewindow"></a><a name="showautohidewindow"></a> CMFCAutoHideBar:: Шоваутохидевиндов

Показывает окно автоматического скрытия.

```
BOOL ShowAutoHideWindow(
    CDockablePane* pAutoHideWnd,
    BOOL bShow,
    BOOL bDelay);
```

### <a name="parameters"></a>Параметры

*паутохидевнд*<br/>
окне Отображаемое окно.

*bShow*<br/>
окне Значение TRUE, чтобы отобразить окно.

*бделай*<br/>
окне Этот параметр не учитывается.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если успешно; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebarstretchpane"></a><a name="stretchpane"></a> CMFCAutoHideBar:: Стретчпане

Изменение размеров строки автоматического скрытия в свернутом состоянии в соответствии с размерами объекта `CMFCAutoHideButton` .

```
virtual CSize StretchPane(
    int nLength,
    BOOL bVert);
```

### <a name="parameters"></a>Параметры

*нленгс*<br/>
окне Значение не используется в базовой реализации. В производных реализациях это значение используется для указания длины панели, размер которой был изменен.

*бверт*<br/>
окне Значение не используется в базовой реализации. В производных реализациях используйте TRUE, чтобы обойти случай, когда полоса автоматического скрытия сворачивается по вертикали, и FALSE для случая, когда полоса автоматического скрытия свернута по горизонтали.

### <a name="return-value"></a>Возвращаемое значение

Размер, полученный в результате изменения размера панели.

### <a name="remarks"></a>Комментарии

Производные классы могут переопределять этот метод для настройки поведения.

## <a name="cmfcautohidebarunsetautohidemode"></a><a name="unsetautohidemode"></a> CMFCAutoHideBar:: Унсетаутохидемоде

Отключает режим автоматического скрытия для группы строк автоматического скрытия.

```cpp
void UnSetAutoHideMode(CDockablePane* pFirstBarInGroup)
```

### <a name="parameters"></a>Параметры

[in] Пфирстбаринграуп указатель на первую полосу автоматического скрытия в группе.

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebarupdatevisiblestate"></a><a name="updatevisiblestate"></a> CMFCAutoHideBar:: Упдатевисиблестате

Вызывается платформой при необходимости перерисовать строку автоматического скрытия.

```cpp
void UpdateVisibleState();
```

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CPane](../../mfc/reference/cpane-class.md)<br/>
[Класс CAutoHideDockSite](../../mfc/reference/cautohidedocksite-class.md)<br/>
[Класс CMFCAutoHideButton](../../mfc/reference/cmfcautohidebutton-class.md)
