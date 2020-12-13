---
description: 'Дополнительные сведения о: CMFCVisualManagerVS2005 Class'
title: Класс CMFCVisualManagerVS2005
ms.date: 11/04/2016
f1_keywords:
- CMFCVisualManagerVS2005
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::GetDockingTabsBordersSize
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::GetMDITabsBordersSize
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::GetPropertyGridGroupColor
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::GetTabFrameColors
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::HasOverlappedAutoHideButtons
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::OnDrawAutoHideButtonBorder
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::OnDrawCaptionButton
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::OnDrawPaneCaption
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::OnDrawSeparator
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::OnDrawTab
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::OnDrawToolBoxFrame
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::OnEraseTabsArea
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::OnFillAutoHideButtonBackground
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::OnFillHighlightedArea
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::OnFillMiniFrameCaption
- AFXVISUALMANAGERVS2005/CMFCVisualManagerVS2005::OnUpdateSystemColors
helpviewer_keywords:
- CMFCVisualManagerVS2005 [MFC], GetDockingTabsBordersSize
- CMFCVisualManagerVS2005 [MFC], GetMDITabsBordersSize
- CMFCVisualManagerVS2005 [MFC], GetPropertyGridGroupColor
- CMFCVisualManagerVS2005 [MFC], GetTabFrameColors
- CMFCVisualManagerVS2005 [MFC], HasOverlappedAutoHideButtons
- CMFCVisualManagerVS2005 [MFC], OnDrawAutoHideButtonBorder
- CMFCVisualManagerVS2005 [MFC], OnDrawCaptionButton
- CMFCVisualManagerVS2005 [MFC], OnDrawPaneCaption
- CMFCVisualManagerVS2005 [MFC], OnDrawSeparator
- CMFCVisualManagerVS2005 [MFC], OnDrawTab
- CMFCVisualManagerVS2005 [MFC], OnDrawToolBoxFrame
- CMFCVisualManagerVS2005 [MFC], OnEraseTabsArea
- CMFCVisualManagerVS2005 [MFC], OnFillAutoHideButtonBackground
- CMFCVisualManagerVS2005 [MFC], OnFillHighlightedArea
- CMFCVisualManagerVS2005 [MFC], OnFillMiniFrameCaption
- CMFCVisualManagerVS2005 [MFC], OnUpdateSystemColors
ms.assetid: ea39b9ae-327e-4a51-bce7-dc84c78f005b
ms.openlocfilehash: 74192e1c0e4c7189a64d872bcc1761cf21e5365d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331644"
---
# <a name="cmfcvisualmanagervs2005-class"></a>Класс CMFCVisualManagerVS2005

`CMFCVisualManagerVS2005` предоставляет приложению внешний вид Microsoft Visual Studio 2005.

## <a name="syntax"></a>Синтаксис

```
class CMFCVisualManagerVS2005 : public CMFCVisualManagerOffice2003
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCVisualManagerVS2005:: Жетдоккингтабсбордерссизе](#getdockingtabsborderssize)|Платформа вызывает этот метод при рисовании закрепленной области и вкладки. (Переопределяет [CMFCVisualManager:: жетдоккингтабсбордерссизе](../../mfc/reference/cmfcvisualmanager-class.md#getdockingtabsborderssize).)|
|[CMFCVisualManagerVS2005:: Жетмдитабсбордерссизе](#getmditabsborderssize)|Платформа вызывает этот метод, чтобы определить размер границы окна Мдитабс перед рисованием окна. (Переопределяет [CMFCVisualManager:: жетмдитабсбордерссизе](../../mfc/reference/cmfcvisualmanager-class.md#getmditabsborderssize).)|
|[CMFCVisualManagerVS2005:: Жетпропертигридграупколор](#getpropertygridgroupcolor)|(Переопределяет [CMFCVisualManagerOffice2003:: жетпропертигридграупколор](../../mfc/reference/cmfcvisualmanageroffice2003-class.md#getpropertygridgroupcolor).)|
|[CMFCVisualManagerVS2005:: Жеттабфрамеколорс](#gettabframecolors)|(Переопределяет [CMFCVisualManagerOffice2003:: жеттабфрамеколорс](../../mfc/reference/cmfcvisualmanageroffice2003-class.md#gettabframecolors).)|
|[CMFCVisualManagerVS2005:: Хасоверлаппедаутохидебуттонс](#hasoverlappedautohidebuttons)|Возвращает значение, определяющее, перекрываются ли кнопки автоматического скрытия в текущем визуальном диспетчере. (Переопределяет [CMFCVisualManager:: хасоверлаппедаутохидебуттонс](../../mfc/reference/cmfcvisualmanager-class.md#hasoverlappedautohidebuttons).)|
|[CMFCVisualManagerVS2005:: Ондраваутохидебуттонбордер](#ondrawautohidebuttonborder)|(Переопределяет [CMFCVisualManagerOffice2003:: ондраваутохидебуттонбордер](../../mfc/reference/cmfcvisualmanageroffice2003-class.md#ondrawautohidebuttonborder).)|
|[CMFCVisualManagerVS2005:: Ондравкаптионбуттон](#ondrawcaptionbutton)|(Переопределяет `CMFCVisualManagerOfficeXP::OnDrawCaptionButton`.)|
|[CMFCVisualManagerVS2005:: Ондравпанекаптион](#ondrawpanecaption)|(Переопределяет [CMFCVisualManagerOffice2003:: ондравпанекаптион](../../mfc/reference/cmfcvisualmanageroffice2003-class.md#ondrawpanecaption).)|
|[CMFCVisualManagerVS2005:: Ондравсепаратор](#ondrawseparator)|(Переопределяет [CMFCVisualManagerOffice2003:: ондравсепаратор](../../mfc/reference/cmfcvisualmanageroffice2003-class.md#ondrawseparator).)|
|[CMFCVisualManagerVS2005:: Ондравтаб](#ondrawtab)|(Переопределяет [CMFCVisualManagerOffice2003:: ондравтаб](../../mfc/reference/cmfcvisualmanageroffice2003-class.md#ondrawtab).)|
|[CMFCVisualManagerVS2005:: Ондравтулбоксфраме](#ondrawtoolboxframe)|(Переопределяет [CMFCVisualManager:: ондравтулбоксфраме](../../mfc/reference/cmfcvisualmanager-class.md#ondrawtoolboxframe).)|
|[CMFCVisualManagerVS2005:: Онерасетабсареа](#onerasetabsarea)|(Переопределяет [CMFCVisualManagerOffice2003:: онерасетабсареа](../../mfc/reference/cmfcvisualmanageroffice2003-class.md#onerasetabsarea).)|
|[CMFCVisualManagerVS2005:: Онфиллаутохидебуттонбаккграунд](#onfillautohidebuttonbackground)|(Переопределяет [CMFCVisualManagerOffice2003:: онфиллаутохидебуттонбаккграунд](../../mfc/reference/cmfcvisualmanageroffice2003-class.md#onfillautohidebuttonbackground).)|
|[CMFCVisualManagerVS2005:: Онфиллхигхлигхтедареа](#onfillhighlightedarea)|(Переопределяет [CMFCVisualManagerOffice2003:: онфиллхигхлигхтедареа](../../mfc/reference/cmfcvisualmanageroffice2003-class.md#onfillhighlightedarea).)|
|[CMFCVisualManagerVS2005:: Онфиллминифрамекаптион](#onfillminiframecaption)|(Переопределяет `CMFCVisualManagerOfficeXP::OnFillMiniFrameCaption`.)|
|[CMFCVisualManagerVS2005:: Онупдатесистемколорс](#onupdatesystemcolors)|(Переопределяет [CMFCVisualManagerOffice2003:: онупдатесистемколорс](../../mfc/reference/cmfcvisualmanageroffice2003-class.md#onupdatesystemcolors).)|

## <a name="remarks"></a>Комментарии

Используйте класс CMFCVisualManagerVS2005, чтобы изменить внешний вид приложения так, чтобы он наглядел примерно так: Microsoft Visual Studio 2005.

Все члены этого класса являются виртуальными функциями, производными от предка этого класса, [класса CMFCVisualManager](../../mfc/reference/cmfcvisualmanager-class.md).

## <a name="example"></a>Пример

В следующем примере показано, как использовать Visual Manager и 2005. Этот фрагмент кода является частью [демонстрационного примера оповещения Desktop](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_DesktopAlertDemo#9](../../mfc/reference/codesnippet/cpp/cmfcvisualmanagervs2005-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[кмфкбасевисуалманажер](../../mfc/reference/cmfcbasevisualmanager-class.md)

[CMFCVisualManager](../../mfc/reference/cmfcvisualmanager-class.md)

[CMFCVisualManagerOfficeXP](../../mfc/reference/cmfcvisualmanagerofficexp-class.md)

[CMFCVisualManagerOffice2003](../../mfc/reference/cmfcvisualmanageroffice2003-class.md)

[CMFCVisualManagerVS2005](../../mfc/reference/cmfcvisualmanagervs2005-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** afxvisualmanagervs2005. h

## <a name="cmfcvisualmanagervs2005getdockingtabsborderssize"></a><a name="getdockingtabsborderssize"></a> CMFCVisualManagerVS2005:: Жетдоккингтабсбордерссизе

```
virtual int GetDockingTabsBordersSize();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005getmditabsborderssize"></a><a name="getmditabsborderssize"></a> CMFCVisualManagerVS2005:: Жетмдитабсбордерссизе

```
virtual int GetMDITabsBordersSize();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005getpropertygridgroupcolor"></a><a name="getpropertygridgroupcolor"></a> CMFCVisualManagerVS2005:: Жетпропертигридграупколор

```
virtual COLORREF GetPropertyGridGroupColor(CMFCPropertyGridCtrl* pPropList);
```

### <a name="parameters"></a>Параметры

окне *ппроплист*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005gettabframecolors"></a><a name="gettabframecolors"></a> CMFCVisualManagerVS2005:: Жеттабфрамеколорс

```
virtual void GetTabFrameColors(
    const CMFCBaseTabCtrl* pTabWnd,
    COLORREF& clrDark,
    COLORREF& clrBlack,
    COLORREF& clrHighlight,
    COLORREF& clrFace,
    COLORREF& clrDarkShadow,
    COLORREF& clrLight,
    CBrush*& pbrFace,
    CBrush*& pbrBlack);
```

### <a name="parameters"></a>Параметры

окне *птабвнд*<br/>
окне *клрдарк*<br/>
окне *клрблакк*<br/>
окне *клрхигхлигхт*<br/>
окне *клрфаце*<br/>
окне *клрдаркшадов*<br/>
окне *клрлигхт*<br/>
окне *пбрфаце*<br/>
окне *пбрблакк*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005hasoverlappedautohidebuttons"></a><a name="hasoverlappedautohidebuttons"></a> CMFCVisualManagerVS2005:: Хасоверлаппедаутохидебуттонс

```
virtual BOOL HasOverlappedAutoHideButtons() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005ondrawautohidebuttonborder"></a><a name="ondrawautohidebuttonborder"></a> CMFCVisualManagerVS2005:: Ондраваутохидебуттонбордер

```
virtual void OnDrawAutoHideButtonBorder(
    CDC* pDC,
    CRect rectBounds,
    CRect rectBorderSize,
    CMFCAutoHideButton* pButton);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>
окне *ректбаундс*<br/>
окне *ректбордерсизе*<br/>
окне *пбуттон*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005ondrawcaptionbutton"></a><a name="ondrawcaptionbutton"></a> CMFCVisualManagerVS2005:: Ондравкаптионбуттон

```
virtual void OnDrawCaptionButton(
    CDC* pDC,
    CMFCCaptionButton* pButton,
    BOOL bActive,
    BOOL bHorz,
    BOOL bMaximized,
    BOOL bDisabled,
    int nImageID = -1);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>
окне *пбуттон*<br/>
окне *бактиве*<br/>
окне *бхорз*<br/>
окне *бмаксимизед*<br/>
окне *бдисаблед*<br/>
окне *нимажеид*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005ondrawpanecaption"></a><a name="ondrawpanecaption"></a> CMFCVisualManagerVS2005:: Ондравпанекаптион

```
virtual COLORREF OnDrawPaneCaption(
    CDC* pDC,
    CDockablePane* pBar,
    BOOL bActive,
    CRect rectCaption,
    CRect rectButtons);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>
окне *пбар*<br/>
окне *бактиве*<br/>
окне *ректкаптион*<br/>
окне *ректбуттонс*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005ondrawseparator"></a><a name="ondrawseparator"></a> CMFCVisualManagerVS2005:: Ондравсепаратор

```
virtual void OnDrawSeparator(
    CDC* pDC,
    CBasePane* pBar,
    CRect rect,
    BOOL bIsHoriz);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>
окне *пбар*<br/>
[in] *rect*<br/>
окне *бишориз*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005ondrawtab"></a><a name="ondrawtab"></a> CMFCVisualManagerVS2005:: Ондравтаб

```
virtual void OnDrawTab(
    CDC* pDC,
    CRect rectTab,
    int iTab,
    BOOL bIsActive,
    const CMFCBaseTabCtrl* pTabWnd);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>
окне *ректтаб*<br/>
[in] *iTab*<br/>
окне *бисактиве*<br/>
окне *птабвнд*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005ondrawtoolboxframe"></a><a name="ondrawtoolboxframe"></a> CMFCVisualManagerVS2005:: Ондравтулбоксфраме

```
virtual void OnDrawToolBoxFrame(
    CDC* pDC,
    const CRect& rect);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>
[in] *rect*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005onerasetabsarea"></a><a name="onerasetabsarea"></a> CMFCVisualManagerVS2005:: Онерасетабсареа

```
virtual void OnEraseTabsArea(
    CDC* pDC,
    CRect rect,
    const CMFCBaseTabCtrl* pTabWnd);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>
[in] *rect*<br/>
окне *птабвнд*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005onfillautohidebuttonbackground"></a><a name="onfillautohidebuttonbackground"></a> CMFCVisualManagerVS2005:: Онфиллаутохидебуттонбаккграунд

```
virtual void OnFillAutoHideButtonBackground(
    CDC* pDC,
    CRect rect,
    CMFCAutoHideButton* pButton);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>
[in] *rect*<br/>
окне *пбуттон*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005onfillhighlightedarea"></a><a name="onfillhighlightedarea"></a> CMFCVisualManagerVS2005:: Онфиллхигхлигхтедареа

```
virtual void OnFillHighlightedArea(
    CDC* pDC,
    CRect rect,
    CBrush* pBrush,
    CMFCToolBarButton* pButton);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>
[in] *rect*<br/>
окне *пбруш*<br/>
окне *пбуттон*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005onfillminiframecaption"></a><a name="onfillminiframecaption"></a> CMFCVisualManagerVS2005:: Онфиллминифрамекаптион

```
virtual COLORREF OnFillMiniFrameCaption(
    CDC* pDC,
    CRect rectCaption,
    CPaneFrameWnd* pFrameWnd,
    BOOL bActive);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>
окне *ректкаптион*<br/>
окне *пфрамевнд*<br/>
окне *бактиве*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagervs2005onupdatesystemcolors"></a><a name="onupdatesystemcolors"></a> CMFCVisualManagerVS2005:: Онупдатесистемколорс

```
virtual void OnUpdateSystemColors();
```

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCVisualManager](../../mfc/reference/cmfcvisualmanager-class.md)<br/>
[Класс CMFCVisualManagerOfficeXP](../../mfc/reference/cmfcvisualmanagerofficexp-class.md)<br/>
[Класс Кмфквисуалманажервиндовс](../../mfc/reference/cmfcvisualmanagerwindows-class.md)<br/>
[Класс CMFCVisualManagerOffice2003](../../mfc/reference/cmfcvisualmanageroffice2003-class.md)
