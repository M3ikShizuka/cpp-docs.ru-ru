---
description: 'Дополнительные сведения о: Кглобалутилс Class'
title: Класс Кглобалутилс
ms.date: 10/18/2018
f1_keywords:
- CGlobalUtils
- AFXGLOBALUTILS/CGlobalUtils
- AFXGLOBALUTILS/CGlobalUtils::AdjustRectToWorkArea
- AFXGLOBALUTILS/CGlobalUtils::CalcExpectedDockedRect
- AFXGLOBALUTILS/CGlobalUtils::CanBeAttached
- AFXGLOBALUTILS/CGlobalUtils::CanPaneBeInFloatingMultiPaneFrameWnd
- AFXGLOBALUTILS/CGlobalUtils::CheckAlignment
- AFXGLOBALUTILS/CGlobalUtils::CyFromString
- AFXGLOBALUTILS/CGlobalUtils::DecimalFromString
- AFXGLOBALUTILS/CGlobalUtils::FlipRect
- AFXGLOBALUTILS/CGlobalUtils::ForceAdjustLayout
- AFXGLOBALUTILS/CGlobalUtils::GetDockingManager
- AFXGLOBALUTILS/CGlobalUtils::GetOppositeAlignment
- AFXGLOBALUTILS/CGlobalUtils::GetPaneAndAlignFromPoint
- AFXGLOBALUTILS/CGlobalUtils::GetWndIcon
- AFXGLOBALUTILS/CGlobalUtils::SetNewParent
- AFXGLOBALUTILS/CGlobalUtils::StringFromCy
- AFXGLOBALUTILS/CGlobalUtils::StringFromDecimal
helpviewer_keywords:
- CGlobalUtils [MFC], AdjustRectToWorkArea
- CGlobalUtils [MFC], CalcExpectedDockedRect
- CGlobalUtils [MFC], CanBeAttached
- CGlobalUtils [MFC], CanPaneBeInFloatingMultiPaneFrameWnd
- CGlobalUtils [MFC], CheckAlignment
- CGlobalUtils [MFC], CyFromString
- CGlobalUtils [MFC], DecimalFromString
- CGlobalUtils [MFC], FlipRect
- CGlobalUtils [MFC], ForceAdjustLayout
- CGlobalUtils [MFC], GetDockingManager
- CGlobalUtils [MFC], GetOppositeAlignment
- CGlobalUtils [MFC], GetPaneAndAlignFromPoint
- CGlobalUtils [MFC], GetWndIcon
- CGlobalUtils [MFC], SetNewParent
- CGlobalUtils [MFC], StringFromCy
- CGlobalUtils [MFC], StringFromDecimal
ms.assetid: 2c5bd1a6-f80c-4e79-a476-b4ceebabfb2f
ms.openlocfilehash: d1e2f096825d34a907afbcdb022c550b94476906
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97184105"
---
# <a name="cglobalutils-class"></a>Класс Кглобалутилс

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```
class CGlobalUtils
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CGlobalUtils::AdjustRectToWorkArea](#adjustrecttoworkarea)||
|[CGlobalUtils::CalcExpectedDockedRect](#calcexpecteddockedrect)||
|[CGlobalUtils::CanBeAttached](#canbeattached)||
|[CGlobalUtils::CanPaneBeInFloatingMultiPaneFrameWnd](#canpanebeinfloatingmultipaneframewnd)||
|[CGlobalUtils::CheckAlignment](#checkalignment)||
|[CGlobalUtils::CyFromString](#cyfromstring)||
|[CGlobalUtils::DecimalFromString](#decimalfromstring)||
|[CGlobalUtils::FlipRect](#fliprect)||
|[CGlobalUtils::ForceAdjustLayout](#forceadjustlayout)||
|[CGlobalUtils::GetDockingManager](#getdockingmanager)||
|[CGlobalUtils::GetOppositeAlignment](#getoppositealignment)||
|[CGlobalUtils::GetPaneAndAlignFromPoint](#getpaneandalignfrompoint)||
|[CGlobalUtils::GetWndIcon](#getwndicon)||
|[CGlobalUtils::SetNewParent](#setnewparent)||
|[CGlobalUtils::StringFromCy](#stringfromcy)||
|[CGlobalUtils::StringFromDecimal](#stringfromdecimal)||

## <a name="remarks"></a>Комментарии

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CGlobalUtils](../../mfc/reference/cglobalutils-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксглобалутилс. h

## <a name="cglobalutilsadjustrecttoworkarea"></a><a name="adjustrecttoworkarea"></a> Кглобалутилс:: Аджустректтоворкареа

```cpp
void AdjustRectToworkArea(
    CRect& rect,
    CRect* pRectDelta = NULL);
```

### <a name="parameters"></a>Параметры

[вход, выход] *Rect*<br/>
окне *пректделта*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilscalcexpecteddockedrect"></a><a name="calcexpecteddockedrect"></a> Кглобалутилс:: Калцекспектеддоккедрект

```cpp
void CalcExpectedDockedRect(
    CPaneContainerManager& barContainerManager,
    CWnd* pWndTodock,
    CPoint ptMouse,
    CRect& rectResult,
    BOOL& bDrawTab,
    CDockablePane** ppTargetBar);
```

### <a name="parameters"></a>Параметры

окне *барконтаинерманажер*<br/>

окне *пвндтодокк*<br/>

окне *птмаусе*<br/>

заполняет *ректресулт*<br/>

заполняет *бдравтаб*<br/>

заполняет *пптаржетбар*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilscanbeattached"></a><a name="canbeattached"></a> Кглобалутилс:: Канбеаттачед

```
BOOL CanBeAttached(CWnd* pWnd) const;
```

### <a name="parameters"></a>Параметры

окне *приводится*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilscanpanebeinfloatingmultipaneframewnd"></a><a name="canpanebeinfloatingmultipaneframewnd"></a> Кглобалутилс:: Канпанебеинфлоатингмултипанефрамевнд

```
BOOL CanPaneBeInFloatingMultiPaneFrameWnd(CWnd* pWnd) const;
```

### <a name="parameters"></a>Параметры

окне *приводится*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilscheckalignment"></a><a name="checkalignment"></a> Кглобалутилс:: Чеккалигнмент

```
BOOL CheckAlignment(
    CPoint point,
    CBasePane* pBar,
    int nSensitivity,
    const CDockingManager* pDockManager,
    BOOL bOuterEdge,
    DWORD& dwAlignment,
    DWORD dwEnabledDockBars = CBRS_ALIGN_ANY,
    LPCRECT lpRectBounds = NULL) const;
```

### <a name="parameters"></a>Параметры

окне *точка*<br/>

окне *пбар*<br/>

окне *нсенситивити*<br/>

окне *пдоккманажер*<br/>

окне *баутередже*<br/>

заполняет *двалигнмент*<br/>

окне *двенабледдоккбарс*<br/>

окне *лпректбаундс*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilscyfromstring"></a><a name="cyfromstring"></a> Кглобалутилс:: Цифромстринг

```
BOOL CyFromString(
    CY& cy,
    LPCTSTR psz);
```

### <a name="parameters"></a>Параметры

заполняет *CY*<br/>

окне *ПСЗ*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilsdecimalfromstring"></a><a name="decimalfromstring"></a> Кглобалутилс::D ЕЦималфромстринг

```
BOOL DecimalFromString(
    DECIMAL& decimal,
    LPCTSTR psz);
```

### <a name="parameters"></a>Параметры

заполняет *десятичное число*<br/>

окне *ПСЗ*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilsfliprect"></a><a name="fliprect"></a> Кглобалутилс:: Флипрект

```cpp
void FlipRect(
    CRect& rect,
    int nDegrees);
```

### <a name="parameters"></a>Параметры

[вход, выход] *Rect*<br/>
окне *ндегрис*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilsforceadjustlayout"></a><a name="forceadjustlayout"></a> Кглобалутилс:: Форцеаджустлайаут

```cpp
void ForceAdjustLayout(
    CDockingManager* pDockManager,
    BOOL bForce = FALSE,
    BOOL bForceInvisible = FALSE);
```

### <a name="parameters"></a>Параметры

[вход, выход] *пдоккманажер*<br/>

окне *бфорце*<br/>

окне *бфорцеинвисибле*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilsgetdockingmanager"></a><a name="getdockingmanager"></a> Кглобалутилс:: Жетдоккингманажер

```
CDockingManager* GetDockingManager(CWnd* pWnd);
```

### <a name="parameters"></a>Параметры

окне *приводится*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilsgetoppositealignment"></a><a name="getoppositealignment"></a> Кглобалутилс:: Жетоппоситеалигнмент

```
DWORD GetOppositeAlignment(DWORD dwAlign);
```

### <a name="parameters"></a>Параметры

окне *двалигн*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilsgetpaneandalignfrompoint"></a><a name="getpaneandalignfrompoint"></a> Кглобалутилс:: Жетпанеандалигнфромпоинт

```
BOOL GetPaneAndAlignFromPoint(
    CPaneContainerManager& barContainerManager,
    CPoint pt,
    CDockablePane** ppTargetControlBar,
    DWORD& dwAlignment,
    BOOL& bTabArea,
    BOOL& bCaption);
```

### <a name="parameters"></a>Параметры

окне *барконтаинерманажер*<br/>

окне *пт*<br/>

заполняет *пптаржетконтролбар*<br/>

заполняет *двалигнмент*<br/>

заполняет *бтабареа*<br/>

заполняет *бкаптион*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilsgetwndicon"></a><a name="getwndicon"></a> Кглобалутилс:: Жетвндикон

```
HICON GetWndIcon(CWnd* pWnd);
```

### <a name="parameters"></a>Параметры

окне *приводится*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilssetnewparent"></a><a name="setnewparent"></a> Кглобалутилс:: Сетневпарент

```cpp
void SetNewParent(
    CObList& lstControlBars,
    CWnd* pNewParent,
    BOOL bCheckVisibility = TRUE);
```

### <a name="parameters"></a>Параметры

окне *лстконтролбарс*<br/>

окне *пневпарент*<br/>

окне *бчекквисибилити*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilsstringfromcy"></a><a name="stringfromcy"></a> Кглобалутилс:: Стрингфромци

```
BOOL StringFromCy(
    CString& str,
    CY& cy);
```

### <a name="parameters"></a>Параметры

заполняет *str*<br/>

окне *CY*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cglobalutilsstringfromdecimal"></a><a name="stringfromdecimal"></a> Кглобалутилс:: СтрингфромдеЦимал

```
BOOL StringFromDecimal(
    CString& str,
    DECIMAL& decimal);
```

### <a name="parameters"></a>Параметры

заполняет *str*<br/>

окне *десятичное число*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)
