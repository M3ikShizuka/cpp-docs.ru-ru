---
description: 'Дополнительные сведения о: Крецентдоккситеинфо Class'
title: Класс Крецентдоккситеинфо
ms.date: 11/04/2016
f1_keywords:
- CRecentDockSiteInfo
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::CleanUp
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::GetRecentDefaultPaneDivider
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::GetRecentDockedPercent
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::GetRecentDockedRect
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::GetRecentListOfPanes
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::GetRecentPaneContainer
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::GetRecentTabContainer
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::Init
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::IsRecentLeftPane
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::SaveListOfRecentPanes
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::SetInfo
- AFXRECENTDOCKSITEINFO/CRecentDockSiteInfo::StoreDockInfo
helpviewer_keywords:
- CRecentDockSiteInfo [MFC], CleanUp
- CRecentDockSiteInfo [MFC], GetRecentDefaultPaneDivider
- CRecentDockSiteInfo [MFC], GetRecentDockedPercent
- CRecentDockSiteInfo [MFC], GetRecentDockedRect
- CRecentDockSiteInfo [MFC], GetRecentListOfPanes
- CRecentDockSiteInfo [MFC], GetRecentPaneContainer
- CRecentDockSiteInfo [MFC], GetRecentTabContainer
- CRecentDockSiteInfo [MFC], Init
- CRecentDockSiteInfo [MFC], IsRecentLeftPane
- CRecentDockSiteInfo [MFC], SaveListOfRecentPanes
- CRecentDockSiteInfo [MFC], SetInfo
- CRecentDockSiteInfo [MFC], StoreDockInfo
ms.assetid: 2dd14f95-d5a2-4461-a7a5-2c6c36a3a165
ms.openlocfilehash: e33ef48be2b091477200f15a31c194d845693399
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97343101"
---
# <a name="crecentdocksiteinfo-class"></a>Класс Крецентдоккситеинфо

`CRecentDockSiteInfo`Класс является вспомогательным классом, в котором хранятся последние сведения о состоянии для [класса CPane](../../mfc/reference/cpane-class.md).

## <a name="syntax"></a>Синтаксис

```
class CRecentDockSiteInfo : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CRecentDockSiteInfo::CRecentDockSiteInfo`|Конструктор по умолчанию.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CRecentDockSiteInfo::CleanUp](#cleanup)||
|[CRecentDockSiteInfo::GetRecentDefaultPaneDivider](#getrecentdefaultpanedivider)||
|[CRecentDockSiteInfo::GetRecentDockedPercent](#getrecentdockedpercent)||
|[CRecentDockSiteInfo::GetRecentDockedRect](#getrecentdockedrect)||
|[CRecentDockSiteInfo::GetRecentListOfPanes](#getrecentlistofpanes)||
|[CRecentDockSiteInfo::GetRecentPaneContainer](#getrecentpanecontainer)||
|[CRecentDockSiteInfo::GetRecentTabContainer](#getrecenttabcontainer)||
|[CRecentDockSiteInfo::Init](#init)||
|[CRecentDockSiteInfo::IsRecentLeftPane](#isrecentleftpane)||
|[Крецентдоккситеинфо:: operator =](#operator_eq)||
|[CRecentDockSiteInfo::SaveListOfRecentPanes](#savelistofrecentpanes)||
|[CRecentDockSiteInfo::SetInfo](#setinfo)||
|[CRecentDockSiteInfo::StoreDockInfo](#storedockinfo)||

## <a name="remarks"></a>Комментарии

Класс `CRecentDockSiteInfo` предназначен для управления данными. Он отслеживает последнее состояние объекта `CPane` при переходе от закрепленного режима к плавающему. Когда пользователь дважды щелкает плавающую закрепляемую панель, она становится закрепленной. Дважды щелкнув закрепленную панель, можно вернуть ее на прежнее место, с прежним размером и состоянием. Аналогичным образом повторное закрепление возвращает панель на предыдущее место закрепления. Именно этот класс данных открывает эту возможность. Поскольку члены этого класса хранят сведения о состоянии закрепленной панели, они не должны напрямую изменяться вашим приложением.

Объект `CRecentDockSiteInfo` создается при каждом создании панели. Каждый `CPane` объект имеет переменную-член [CPane:: m_recentDockInfo](../../mfc/reference/cpane-class.md#m_recentdockinfo)для хранения этих сведений.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CRecentDockSiteInfo](../../mfc/reference/crecentdocksiteinfo-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксрецентдоккситеинфо. h

## <a name="crecentdocksiteinfocleanup"></a><a name="cleanup"></a> Крецентдоккситеинфо:: CleanUp

```cpp
void CleanUp();
```

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfocrecentdocksiteinfo"></a><a name="crecentdocksiteinfo"></a> Крецентдоккситеинфо:: Крецентдоккситеинфо

```
CRecentDockSiteInfo(CPane* pBar);
```

### <a name="parameters"></a>Параметры

окне *пбар*<br/>

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfogetrecentdefaultpanedivider"></a><a name="getrecentdefaultpanedivider"></a> Крецентдоккситеинфо:: Жетрецентдефаултпанедивидер

```
CPaneDivider* GetRecentDefaultPaneDivider();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfogetrecentdockedpercent"></a><a name="getrecentdockedpercent"></a> Крецентдоккситеинфо:: Жетрецентдоккедперцент

```
int GetRecentDockedPercent(BOOL bForSlider);
```

### <a name="parameters"></a>Параметры

окне *бфорслидер*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfogetrecentdockedrect"></a><a name="getrecentdockedrect"></a> Крецентдоккситеинфо:: Жетрецентдоккедрект

```
CRect& GetRecentDockedRect(BOOL bForSlider);
```

### <a name="parameters"></a>Параметры

окне *бфорслидер*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfogetrecentlistofpanes"></a><a name="getrecentlistofpanes"></a> Крецентдоккситеинфо:: Жетрецентлистофпанес

```
CList<HWND, HWND>& GetRecentListOfPanes(BOOL bForSlider);
```

### <a name="parameters"></a>Параметры

окне *бфорслидер*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfogetrecentpanecontainer"></a><a name="getrecentpanecontainer"></a> Крецентдоккситеинфо:: Жетрецентпанеконтаинер

```
CPaneContainer* GetRecentPaneContainer(BOOL bForSlider);
```

### <a name="parameters"></a>Параметры

окне *бфорслидер*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfogetrecenttabcontainer"></a><a name="getrecenttabcontainer"></a> Крецентдоккситеинфо:: Жетреценттабконтаинер

```
CPaneContainer* GetRecentTabContainer(BOOL bForSlider);
```

### <a name="parameters"></a>Параметры

окне *бфорслидер*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfoinit"></a><a name="init"></a> Крецентдоккситеинфо:: init

```cpp
void Init();
```

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfoisrecentleftpane"></a><a name="isrecentleftpane"></a> Крецентдоккситеинфо:: Исрецентлефтпане

```
BOOL IsRecentLeftPane(BOOL bForSlider);
```

### <a name="parameters"></a>Параметры

окне *бфорслидер*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfooperator-"></a><a name="operator_eq"></a> Крецентдоккситеинфо:: operator =

```
CRecentDockSiteInfo& operator=(CRecentDockSiteInfo& src);
```

### <a name="parameters"></a>Параметры

окне *src*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfosavelistofrecentpanes"></a><a name="savelistofrecentpanes"></a> Крецентдоккситеинфо:: Савелистофрецентпанес

```cpp
void SaveListOfRecentPanes(CList<HWND,
    HWND>& lstOrg,
    BOOL bForSlider);
```

### <a name="parameters"></a>Параметры

окне *CList<HWND*<br/>
окне *лсторг*<br/>
окне *бфорслидер*<br/>

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfosetinfo"></a><a name="setinfo"></a> Крецентдоккситеинфо:: Сетинфо

```
virtual void SetInfo(
    BOOL bForSlider,
    CRecentDockSiteInfo& srcInfo);
```

### <a name="parameters"></a>Параметры

окне *бфорслидер*<br/>
окне *срЦинфо*<br/>

### <a name="remarks"></a>Комментарии

## <a name="crecentdocksiteinfostoredockinfo"></a><a name="storedockinfo"></a> Крецентдоккситеинфо:: Сторедоккинфо

```
virtual void StoreDockInfo(
    CPaneContainer* pRecentContainer,
    CDockablePane* pTabbedBar = NULL);
```

### <a name="parameters"></a>Параметры

окне *прецентконтаинер*<br/>
окне *птаббедбар*<br/>

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CDockSite](../../mfc/reference/cdocksite-class.md)
