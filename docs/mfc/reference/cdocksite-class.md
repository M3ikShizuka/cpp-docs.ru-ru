---
description: 'Дополнительные сведения о: CDockSite Class'
title: CDockSite Class
ms.date: 10/18/2018
f1_keywords:
- CDockSite
- AFXDOCKSITE/CDockSite
- AFXDOCKSITE/CDockSite::AddRow
- AFXDOCKSITE/CDockSite::AdjustDockingLayout
- AFXDOCKSITE/CDockSite::AdjustLayout
- AFXDOCKSITE/CDockSite::AlignDockSite
- AFXDOCKSITE/CDockSite::CalcFixedLayout
- AFXDOCKSITE/CDockSite::CanAcceptPane
- AFXDOCKSITE/CDockSite::CreateEx
- AFXDOCKSITE/CDockSite::CreateRow
- AFXDOCKSITE/CDockSite::DockPane
- AFXDOCKSITE/CDockSite::DoesAllowDynInsertBefore
- AFXDOCKSITE/CDockSite::FindRowIndex
- AFXDOCKSITE/CDockSite::FixupVirtualRects
- AFXDOCKSITE/CDockSite::GetDockSiteID
- AFXDOCKSITE/CDockSite::GetDockSiteRowsList
- AFXDOCKSITE/CDockSite::IsAccessibilityCompatible
- AFXDOCKSITE/CDockSite::IsDragMode
- AFXDOCKSITE/CDockSite::IsLastRow
- AFXDOCKSITE/CDockSite::IsRectWithinDockSite
- AFXDOCKSITE/CDockSite::IsResizable
- AFXDOCKSITE/CDockSite::MovePane
- AFXDOCKSITE/CDockSite::OnInsertRow
- AFXDOCKSITE/CDockSite::OnRemoveRow
- AFXDOCKSITE/CDockSite::OnResizeRow
- AFXDOCKSITE/CDockSite::OnSetWindowPos
- AFXDOCKSITE/CDockSite::OnShowRow
- AFXDOCKSITE/CDockSite::OnSizeParent
- AFXDOCKSITE/CDockSite::PaneFromPoint
- AFXDOCKSITE/CDockSite::DockPaneLeftOf
- AFXDOCKSITE/CDockSite::FindPaneByID
- AFXDOCKSITE/CDockSite::GetPaneList
- AFXDOCKSITE/CDockSite::RectSideFromPoint
- AFXDOCKSITE/CDockSite::RemovePane
- AFXDOCKSITE/CDockSite::RemoveRow
- AFXDOCKSITE/CDockSite::ReplacePane
- AFXDOCKSITE/CDockSite::RepositionPanes
- AFXDOCKSITE/CDockSite::ResizeDockSite
- AFXDOCKSITE/CDockSite::ResizeRow
- AFXDOCKSITE/CDockSite::ShowPane
- AFXDOCKSITE/CDockSite::ShowRow
- AFXDOCKSITE/CDockSite::SwapRows
helpviewer_keywords:
- CDockSite [MFC], AddRow
- CDockSite [MFC], AdjustDockingLayout
- CDockSite [MFC], AdjustLayout
- CDockSite [MFC], AlignDockSite
- CDockSite [MFC], CalcFixedLayout
- CDockSite [MFC], CanAcceptPane
- CDockSite [MFC], CreateEx
- CDockSite [MFC], CreateRow
- CDockSite [MFC], DockPane
- CDockSite [MFC], DoesAllowDynInsertBefore
- CDockSite [MFC], FindRowIndex
- CDockSite [MFC], FixupVirtualRects
- CDockSite [MFC], GetDockSiteID
- CDockSite [MFC], GetDockSiteRowsList
- CDockSite [MFC], IsAccessibilityCompatible
- CDockSite [MFC], IsDragMode
- CDockSite [MFC], IsLastRow
- CDockSite [MFC], IsRectWithinDockSite
- CDockSite [MFC], IsResizable
- CDockSite [MFC], MovePane
- CDockSite [MFC], OnInsertRow
- CDockSite [MFC], OnRemoveRow
- CDockSite [MFC], OnResizeRow
- CDockSite [MFC], OnSetWindowPos
- CDockSite [MFC], OnShowRow
- CDockSite [MFC], OnSizeParent
- CDockSite [MFC], PaneFromPoint
- CDockSite [MFC], DockPaneLeftOf
- CDockSite [MFC], FindPaneByID
- CDockSite [MFC], GetPaneList
- CDockSite [MFC], RectSideFromPoint
- CDockSite [MFC], RemovePane
- CDockSite [MFC], RemoveRow
- CDockSite [MFC], ReplacePane
- CDockSite [MFC], RepositionPanes
- CDockSite [MFC], ResizeDockSite
- CDockSite [MFC], ResizeRow
- CDockSite [MFC], ShowPane
- CDockSite [MFC], ShowRow
- CDockSite [MFC], SwapRows
ms.assetid: 0fcfff79-5f50-4281-b2de-a55653bbea40
ms.openlocfilehash: e8d56ed3d343f68215f6c1f053cd045cf37fe064
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185002"
---
# <a name="cdocksite-class"></a>CDockSite Class

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

Предоставляет функциональные возможности для упорядочения областей, которые являются производными от [CPane Class](../../mfc/reference/cpane-class.md) , в наборы строк.

## <a name="syntax"></a>Синтаксис

```
class CDockSite: public CBasePane
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CDockSite::AddRow](#addrow)||
|[CDockSite::AdjustDockingLayout](#adjustdockinglayout)|(Переопределяет [CBasePane:: аджустдоккинглайаут](../../mfc/reference/cbasepane-class.md#adjustdockinglayout).)|
|[CDockSite::AdjustLayout](#adjustlayout)|(Переопределяет [CBasePane:: аджустлайаут](../../mfc/reference/cbasepane-class.md#adjustlayout).)|
|[CDockSite::AlignDockSite](#aligndocksite)||
|[CDockSite::CalcFixedLayout](#calcfixedlayout)|(Переопределяет [CBasePane:: калкфикседлайаут](../../mfc/reference/cbasepane-class.md#calcfixedlayout).)|
|[CDockSite::CanAcceptPane](#canacceptpane)|(Переопределяет [CBasePane:: канакцептпане](../../mfc/reference/cbasepane-class.md#canacceptpane).)|
|[CDockSite::CreateEx](#createex)|(Переопределяет [CBasePane:: креатикс](../../mfc/reference/cbasepane-class.md#createex).)|
|[CDockSite::CreateRow](#createrow)||
|[CDockSite::DockPane](#dockpane)|(Переопределяет [CBasePane::D оккпане](../../mfc/reference/cbasepane-class.md#dockpane).)|
|[CDockSite::DoesAllowDynInsertBefore](#doesallowdyninsertbefore)|(Переопределяет [CBasePane::D оесалловдининсертбефоре](../../mfc/reference/cbasepane-class.md#doesallowdyninsertbefore).)|
|[CDockSite::FindRowIndex](#findrowindex)||
|[CDockSite::FixupVirtualRects](#fixupvirtualrects)||
|[CDockSite::GetDockSiteID](#getdocksiteid)||
|[CDockSite::GetDockSiteRowsList](#getdocksiterowslist)||
|[CDockSite::IsAccessibilityCompatible](#isaccessibilitycompatible)|(Переопределяет `CBasePane::IsAccessibilityCompatible`.)|
|[CDockSite::IsDragMode](#isdragmode)||
|[CDockSite::IsLastRow](#islastrow)||
|[CDockSite::IsRectWithinDockSite](#isrectwithindocksite)||
|[CDockSite::IsResizable](#isresizable)|(Переопределяет [CBasePane:: исресизабле](../../mfc/reference/cbasepane-class.md#isresizable).)|
|[CDockSite::MovePane](#movepane)||
|[CDockSite::OnInsertRow](#oninsertrow)||
|[CDockSite::OnRemoveRow](#onremoverow)||
|[CDockSite::OnResizeRow](#onresizerow)||
|[CDockSite::OnSetWindowPos](#onsetwindowpos)||
|[CDockSite::OnShowRow](#onshowrow)||
|[CDockSite::OnSizeParent](#onsizeparent)||
|[CDockSite::PaneFromPoint](#panefrompoint)|Возвращает область, закрепленную на сайте закрепления в точке, указанной данным параметром.|
|[CDockSite::DockPaneLeftOf](#dockpaneleftof)|Закрепляет область слева от другой области.|
|[CDockSite:: Финдпанебид](#findpanebyid)|Возвращает область, определенную по заданному идентификатору.|
|[CDockSite::GetPaneList](#getpanelist)|Возвращает список областей, которые закреплены на сайте закрепления.|
|[CDockSite::RectSideFromPoint](#rectsidefrompoint)||
|[CDockSite::RemovePane](#removepane)||
|[CDockSite::RemoveRow](#removerow)||
|[CDockSite::ReplacePane](#replacepane)||
|[CDockSite::RepositionPanes](#repositionpanes)||
|[CDockSite::ResizeDockSite](#resizedocksite)||
|[CDockSite::ResizeRow](#resizerow)||
|[CDockSite::ShowPane](#showpane)|Отображает область.|
|[CDockSite::ShowRow](#showrow)||
|[CDockSite::SwapRows](#swaprows)||

## <a name="remarks"></a>Комментарии

Платформа автоматически создает `CDockSite` объекты при вызове [CFrameWndEx:: енабледоккинг](../../mfc/reference/cframewndex-class.md#enabledocking). Окна сайта закрепления располагаются на границе области клиента в главном окне фрейма.

Обычно нет необходимости вызывать службы, предоставляемые сайтом DOCKER, так как [Класс CFrameWndEx](../../mfc/reference/cframewndex-class.md) обрабатывает эти службы.

## <a name="example"></a>Пример

В следующем примере показывается, как создать объект класса `CDockSite`.

[!code-cpp[NVC_MFC_RibbonApp#27](../../mfc/reference/codesnippet/cpp/cdocksite-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)\
└ &nbsp; [От CCmdTarget](../../mfc/reference/ccmdtarget-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [CWnd](../../mfc/reference/cwnd-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [CBasePane](../../mfc/reference/cbasepane-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [CDockSite](../../mfc/reference/cdocksite-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксдокксите. h

## <a name="cdocksiteaddrow"></a><a name="addrow"></a> CDockSite:: AddRow

```
CDockingPanesRow* AddRow(
    POSITION pos,
    int nHeight);
```

### <a name="parameters"></a>Параметры

окне *POS-терминал*<br/>

окне *нхеигхт*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteadjustdockinglayout"></a><a name="adjustdockinglayout"></a> CDockSite:: Аджустдоккинглайаут

```
virtual void AdjustDockingLayout();
```

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteadjustlayout"></a><a name="adjustlayout"></a> CDockSite:: Аджустлайаут

```
virtual void AdjustLayout();
```

### <a name="remarks"></a>Комментарии

## <a name="cdocksitealigndocksite"></a><a name="aligndocksite"></a> CDockSite:: Алигндокксите

```cpp
void AlignDockSite(
    const CRect& rectToAlignBy,
    CRect& rectResult,
    BOOL bMoveImmediately);
```

### <a name="parameters"></a>Параметры

окне *ректтоалигнби*<br/>

окне *ректресулт*<br/>

окне *бмовеиммедиатели*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cdocksitecalcfixedlayout"></a><a name="calcfixedlayout"></a> CDockSite:: Калкфикседлайаут

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

## <a name="cdocksitecanacceptpane"></a><a name="canacceptpane"></a> CDockSite:: Канакцептпане

```
virtual BOOL CanAcceptPane(const CBasePane* pBar) const;
```

### <a name="parameters"></a>Параметры

окне *пбар*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksitecreateex"></a><a name="createex"></a> CDockSite:: Креатикс

```
virtual BOOL CreateEx(
    DWORD dwStyleEx,
    DWORD dwStyle,
    const RECT& rect,
    CWnd* pParentWnd,
    DWORD dwControlBarStyle,
    CCreateContext* pContext = NULL);
```

### <a name="parameters"></a>Параметры

окне *двстиликс*<br/>

окне *двстиле*<br/>

[in] *rect*<br/>

окне *ппарентвнд*<br/>

окне *двконтролбарстиле*<br/>

окне *пконтекст*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksitecreaterow"></a><a name="createrow"></a> CDockSite:: Креатеров

```
virtual CDockingPanesRow* CreateRow(
    CDockSite* pParentDockBar,
    int nOffset,
    int nRowHeight);
```

### <a name="parameters"></a>Параметры

окне *ппарентдоккбар*<br/>

окне *ноффсет*<br/>

окне *нровхеигхт*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksitedockpane"></a><a name="dockpane"></a> CDockSite::D Оккпане

```
virtual void DockPane(
    CPane* pWnd,
    AFX_DOCK_METHOD dockMethod,
    LPCRECT lpRect = NULL);
```

### <a name="parameters"></a>Параметры

окне *приводится*<br/>

окне *доккмесод*<br/>

окне *лпрект*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cdocksitedockpaneleftof"></a><a name="dockpaneleftof"></a> CDockSite::D Оккпанелефтоф

Закрепляет область слева от другой области.

```
virtual BOOL DockPaneLeftOf(
    CPane* pBarToDock,
    CPane* pTargetBar);
```

### <a name="parameters"></a>Параметры

*пбартодокк*<br/>
[вход, выход] Указатель на область, которая должна быть закреплена слева от *птаржетбар*.

*птаржетбар*<br/>
[вход, выход] Указатель на целевую область.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если панель закреплена успешно; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cdocksitedoesallowdyninsertbefore"></a><a name="doesallowdyninsertbefore"></a> CDockSite::D Оесалловдининсертбефоре

```
virtual BOOL DoesAllowDynInsertBefore() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksitefindpanebyid"></a><a name="findpanebyid"></a> CDockSite:: Финдпанебид

Возвращает панель с заданным ИДЕНТИФИКАТОРом.

```
CPane* FindPaneByID(UINT nID);
```

### <a name="parameters"></a>Параметры

*nID*<br/>
окне Идентификатор команды для поиска.

### <a name="return-value"></a>Возвращаемое значение

Указатель на область с указанным ИДЕНТИФИКАТОРом команды или значение NULL, если панель не найдена.

### <a name="remarks"></a>Комментарии

## <a name="cdocksitefindrowindex"></a><a name="findrowindex"></a> CDockSite:: Финдровиндекс

```
int FindRowIndex(CDockingPanesRow* pRow);
```

### <a name="parameters"></a>Параметры

окне *пров*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksitefixupvirtualrects"></a><a name="fixupvirtualrects"></a> CDockSite:: Фиксупвиртуалректс

```
virtual void FixupVirtualRects();
```

### <a name="remarks"></a>Комментарии

## <a name="cdocksitegetdocksiteid"></a><a name="getdocksiteid"></a> CDockSite:: Жетдоккситеид

```
virtual UINT GetDockSiteID() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksitegetdocksiterowslist"></a><a name="getdocksiterowslist"></a> CDockSite:: Жетдоккситеровслист

```
const CObList& GetDockSiteRowsList() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksitegetpanelist"></a><a name="getpanelist"></a> CDockSite:: копанель

Возвращает список панелей, закрепленных на сайте закрепления.

```
const CObList& GetPaneList() const;
```

### <a name="return-value"></a>Возвращаемое значение

Доступная только для чтения ссылка на список панелей, которые в данный момент закреплены на закрепленной панели.

## <a name="cdocksiteisaccessibilitycompatible"></a><a name="isaccessibilitycompatible"></a> CDockSite:: Исакцессибилитикомпатибле

```
virtual BOOL IsAccessibilityCompatible();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteisdragmode"></a><a name="isdragmode"></a> CDockSite:: Исдрагмоде

```
virtual BOOL IsDragMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteislastrow"></a><a name="islastrow"></a> CDockSite:: Исластров

```
bool IsLastRow(CDockingPanesRow* pRow) const;
```

### <a name="parameters"></a>Параметры

окне *пров*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteisrectwithindocksite"></a><a name="isrectwithindocksite"></a> CDockSite:: Исректвисиндокксите

```
BOOL IsRectWithinDockSite(
    CRect rect,
    CPoint& ptDelta);
```

### <a name="parameters"></a>Параметры

[in] *rect*<br/>

окне *птделта*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteisresizable"></a><a name="isresizable"></a> CDockSite:: Исресизабле

```
virtual BOOL IsResizable() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksitemovepane"></a><a name="movepane"></a> CDockSite:: Мовепане

```
virtual BOOL MovePane(
    CPane* pWnd,
    UINT nFlags,
    CPoint ptOffset);
```

### <a name="parameters"></a>Параметры

окне *приводится*<br/>

окне *нфлагс*<br/>

окне *птоффсет*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteoninsertrow"></a><a name="oninsertrow"></a> CDockSite:: Онинсертров

```
virtual void OnInsertRow(POSITION pos);
```

### <a name="parameters"></a>Параметры

окне *POS-терминал*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteonremoverow"></a><a name="onremoverow"></a> CDockSite:: Онремоверов

```
virtual void OnRemoveRow(
    POSITION pos,
    BOOL bByShow = FALSE);
```

### <a name="parameters"></a>Параметры

окне *POS-терминал*<br/>

окне *ббишов*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteonresizerow"></a><a name="onresizerow"></a> CDockSite:: Онресизеров

```
virtual int OnResizeRow(
    CDockingPanesRow* pRowToResize,
    int nOffset);
```

### <a name="parameters"></a>Параметры

окне *провторесизе*<br/>

окне *ноффсет*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteonsizeparent"></a><a name="onsizeparent"></a> CDockSite:: Онсизепарент

```
virtual void OnSizeParent(
    CRect& rectAvailable,
    UINT nSide,
    BOOL bExpand,
    int nOffset);
```

### <a name="parameters"></a>Параметры

окне *ректаваилабле*<br/>

окне *нсиде*<br/>

окне *бекспанд*<br/>

окне *ноффсет*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteonsetwindowpos"></a><a name="onsetwindowpos"></a> CDockSite:: Онсетвиндовпос

```
virtual BOOL OnSetWindowPos(
    const CWnd* pWndInsertAfter,
    const CRect& rectWnd,
    UINT nFlags);
```

### <a name="parameters"></a>Параметры

окне *пвндинсертафтер*<br/>

окне *ректвнд*<br/>

окне *нфлагс*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteonshowrow"></a><a name="onshowrow"></a> CDockSite:: Оншовров

```
virtual void OnShowRow(
    POSITION pos,
    BOOL bShow);
```

### <a name="parameters"></a>Параметры

окне *POS-терминал*<br/>

окне *бшов*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cdocksitepanefrompoint"></a><a name="panefrompoint"></a> CDockSite::P Анефромпоинт

Возвращает область, закрепленную на сайте закрепления в точке, указанной данным параметром.

```
virtual CPane* PaneFromPoint(CPoint pt);
```

### <a name="parameters"></a>Параметры

*пт*<br/>
окне Точка, в координатах экрана, для извлекаемой области.

### <a name="return-value"></a>Возвращаемое значение

Указатель на область, расположенную в указанной точке, или значение NULL, если в указанной точке отсутствует область.

### <a name="remarks"></a>Комментарии

## <a name="cdocksiterectsidefrompoint"></a><a name="rectsidefrompoint"></a> CDockSite:: Ректсидефромпоинт

```
static int __stdcall RectSideFromPoint(
    const CRect& rect,
    const CPoint& point);
```

### <a name="parameters"></a>Параметры

[in] *rect*<br/>

окне *точка*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteremovepane"></a><a name="removepane"></a> CDockSite:: Ремовепане

```
virtual void RemovePane(
    CPane* pWnd,
    AFX_DOCK_METHOD dockMethod);
```

### <a name="parameters"></a>Параметры

окне *приводится*<br/>

окне *доккмесод*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteremoverow"></a><a name="removerow"></a> CDockSite:: RemoveRow

```cpp
void RemoveRow(CDockingPanesRow* pRow);
```

### <a name="parameters"></a>Параметры

окне *пров*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cdocksitereplacepane"></a><a name="replacepane"></a> CDockSite:: Реплацепане

```
BOOL ReplacePane(
    CPane* pOldBar,
    CPane* pNewBar);
```

### <a name="parameters"></a>Параметры

окне *полдбар*<br/>

окне *пневбар*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksiterepositionpanes"></a><a name="repositionpanes"></a> CDockSite:: Репоситионпанес

```
virtual void RepositionPanes(CRect& rectNewClientArea);
```

### <a name="parameters"></a>Параметры

окне *ректневклиентареа*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteresizedocksite"></a><a name="resizedocksite"></a> CDockSite:: Ресизедокксите

```cpp
void ResizeDockSite(
    int nNewWidth,
    int nNewHeight);
```

### <a name="parameters"></a>Параметры

окне *нневвидс*<br/>

окне *нневхеигхт*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteresizerow"></a><a name="resizerow"></a> CDockSite:: Ресизеров

```
int ResizeRow(
    CDockingPanesRow* pRow,
    int nNewSize,
    BOOL bAdjustLayout = TRUE);
```

### <a name="parameters"></a>Параметры

окне *пров*<br/>

окне *нневсизе*<br/>

окне *баджустлайаут*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteshowpane"></a><a name="showpane"></a> CDockSite:: Шовпане

Отображает область.

```
virtual BOOL ShowPane(
    CBasePane* pBar,
    BOOL bShow,
    BOOL bDelay,
    BOOL bActivate);
```

### <a name="parameters"></a>Параметры

*пбар*<br/>
[вход, выход] Указатель на панель, которую необходимо отобразить или скрыть.

*bShow*<br/>
окне Значение TRUE, чтобы указать, что область должна отображаться; Значение FALSE, чтобы указать, что панель должна быть скрыта.

*бделай*<br/>
окне Значение TRUE, чтобы указать, что макет области должен быть отложен до отображения панели. в противном случае — значение FALSE.

*bActivate*<br/>
окне Этот параметр не используется.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если панель была успешно отображена или скрыта. Значение FALSE, если указанная панель не принадлежит этому сайту закрепления.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы показать или скрыть закрепленные панели. Как правило, необязательно вызывать `CDockSite::ShowPane` напрямую, так как он вызывается родительским окном фрейма или базовой панелью.

## <a name="cdocksiteshowrow"></a><a name="showrow"></a> CDockSite:: Шовров

```cpp
void ShowRow(
    CDockingPanesRow* pRow,
    BOOL bShow,
    BOOL bAdjustLayout);
```

### <a name="parameters"></a>Параметры

окне *пров*<br/>

окне *бшов*<br/>

окне *баджустлайаут*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cdocksiteswaprows"></a><a name="swaprows"></a> CDockSite:: Свапровс

```cpp
void SwapRows(
    CDockingPanesRow* pFirstRow,
    CDockingPanesRow* pSecondRow);
```

### <a name="parameters"></a>Параметры

окне *пфирстров*<br/>

окне *псекондров*<br/>

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CBasePane](../../mfc/reference/cbasepane-class.md)
