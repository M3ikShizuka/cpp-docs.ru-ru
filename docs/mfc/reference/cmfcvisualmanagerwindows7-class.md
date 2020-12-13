---
description: 'Дополнительные сведения о: CMFCVisualManagerWindows7 Class'
title: Класс CMFCVisualManagerWindows7
ms.date: 03/27/2019
f1_keywords:
- CMFCVisualManagerWindows7
- AFXVISUALMANAGERWINDOWS7/CMFCVisualManagerWindows7
- AFXVISUALMANAGERWINDOWS7/CMFCVisualManagerWindows7::CMFCVisualManagerWindows7
- AFXVISUALMANAGERWINDOWS7/CMFCVisualManagerWindows7::GetRibbonEditBackgroundColor
- AFXVISUALMANAGERWINDOWS7/CMFCVisualManagerWindows7::OnFillMenuImageRect
helpviewer_keywords:
- CMFCVisualManagerWindows7 Class [MFC]
ms.assetid: e8d87df1-0c09-4b58-8ade-4e911f796e42
ms.openlocfilehash: 108d4144bbcfbfcb82d91678611435f14365302e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331635"
---
# <a name="cmfcvisualmanagerwindows7-class"></a>Класс CMFCVisualManagerWindows7

`CMFCVisualManagerWindows7`Предоставляет приложению внешний вид приложения Windows 7.

## <a name="syntax"></a>Синтаксис

```
class CMFCVisualManagerWindows7 : public CMFCVisualManagerWindows;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMFCVisualManagerWindows7::CMFCVisualManagerWindows7](#cmfcvisualmanagerwindows7)|Конструктор по умолчанию.|
|[CMFCVisualManagerWindows7:: ~ CMFCVisualManagerWindows7](#_dtorcmfcvisualmanagerwindows7)|Деструктор по умолчанию.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|`CMFCVisualManagerWindows7::CleanStyle`|Очищает текущий визуальный стиль и сбрасывает стиль оформления по умолчанию.|
|`CMFCVisualManagerWindows7::CleanUp`|Удаляет все объекты в пользовательском интерфейсе и сбрасывает меню.|
|`CMFCVisualManagerWindows7::DrawNcBtn`|Рисует кнопку в области, не являющейся клиентской, в рамке. Платформа использует этот метод для рисования кнопок сворачивания, развертывания, закрытия и восстановления в правом верхнем углу рамки окна. Этот метод вызывается только в том случае, если программа использует `Aero` тему.|
|`CMFCVisualManagerWindows7::DrawNcText`|Рисует текст в области, не являющейся клиентской, в рамке. Платформа использует этот метод, чтобы нарисовать заголовок приложения в строке заголовка в верхней части окна фрейма.|
|`CMFCVisualManagerWindows7::DrawSeparator`|Рисует разделитель для [класса CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md).|
|`CMFCVisualManagerWindows7::GetRibbonBar`|Извлекает [класс CMFCRibbonBar](../../mfc/reference/cmfcribbonbar-class.md) , связанный с пользовательским интерфейсом.|
|[CMFCVisualManagerWindows7:: Жетриббонедитбаккграундколор](#getribboneditbackgroundcolor)|Получает цвет фона поля редактирования на ленте.|
|`CMFCVisualManagerWindows7::GetRibbonPopupBorderSize`|Переопределяет [CMFCVisualManager:: жетриббонпопупбордерсизе](../../mfc/reference/cmfcvisualmanager-class.md#getribbonpopupbordersize)|
|`CMFCVisualManagerWindows7::GetRibbonQuickAccessToolBarChevronOffset`|Переопределяет [CMFCVisualManager:: жетриббонкуиккакцесстулбарчевроноффсет](../../mfc/reference/cmfcvisualmanager-class.md#getribbonquickaccesstoolbarchevronoffset)|
|`CMFCVisualManagerWindows7::GetRibbonQuickAccessToolBarRightMargin`|Переопределяет [CMFCVisualManager:: жетриббонкуиккакцесстулбарригхтмаргин](../../mfc/reference/cmfcvisualmanager-class.md#getribbonquickaccesstoolbarrightmargin)|
|`CMFCVisualManagerWindows7::IsHighlightWholeMenuItem`|Переопределяет [кмфквисуалманажервиндовс:: ишигхлигхтвхолеменуитем](../../mfc/reference/cmfcvisualmanagerwindows-class.md#ishighlightwholemenuitem)|
|`CMFCVisualManagerWindows7::IsOwnerDrawMenuCheck`|Переопределяет [CMFCVisualManager:: исовнердравменучекк](../../mfc/reference/cmfcvisualmanager-class.md#isownerdrawmenucheck)|
|`CMFCVisualManagerWindows7::IsRibbonPresent`|Определяет наличие `CMFCRibbonBar` и видимость элемента.|
|`CMFCVisualManagerWindows7::OnDrawButtonBorder`|Переопределяет [кмфквисуалманажервиндовс:: ондравбуттонбордер](../../mfc/reference/cmfcvisualmanagerwindows-class.md#ondrawbuttonborder)|
|`CMFCVisualManagerWindows7::OnDrawCheckBoxEx`|Переопределяет [кмфквисуалманажервиндовс:: ондравчеккбоксекс](../../mfc/reference/cmfcvisualmanagerwindows-class.md#ondrawcheckboxex)|
|`CMFCVisualManagerWindows7::OnDrawComboDropButton`|Переопределяет [кмфквисуалманажервиндовс:: ондравкомбодропбуттон](../../mfc/reference/cmfcvisualmanagerwindows-class.md#ondrawcombodropbutton)|
|`CMFCVisualManagerWindows7::OnDrawDefaultRibbonImage`|Переопределяет [CMFCVisualManager:: ондравдефаултриббонимаже](../../mfc/reference/cmfcvisualmanager-class.md#ondrawdefaultribbonimage)|
|`CMFCVisualManagerWindows7::OnDrawMenuBorder`|Переопределяет [кмфквисуалманажервиндовс:: ондравменубордер](../../mfc/reference/cmfcvisualmanagerwindows-class.md#ondrawmenuborder)|
|`CMFCVisualManagerWindows7::OnDrawMenuCheck`|Переопределяет [CMFCVisualManager:: ондравменучекк](../../mfc/reference/cmfcvisualmanager-class.md#ondrawmenucheck)|
|`CMFCVisualManagerWindows7::OnDrawMenuLabel`|Переопределяет [CMFCVisualManager:: ондравменулабел](../../mfc/reference/cmfcvisualmanager-class.md#ondrawmenulabel)|
|`CMFCVisualManagerWindows7::OnDrawRadioButton`|Переопределяет метод `CMFCVisualManager::OnDrawRadioButton`.|
|`CMFCVisualManagerWindows7::OnDrawRibbonApplicationButton`|Переопределяет [CMFCVisualManager:: ондравриббонаппликатионбуттон](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbonapplicationbutton)|
|`CMFCVisualManagerWindows7::OnDrawRibbonButtonBorder`|Переопределяет [CMFCVisualManager:: ондравриббонбуттонбордер](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbonbuttonborder)|
|`CMFCVisualManagerWindows7::OnDrawRibbonCaption`|Переопределяет [CMFCVisualManager:: ондравриббонкаптион](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribboncaption)|
|`CMFCVisualManagerWindows7::OnDrawRibbonCaptionButton`|Переопределяет [CMFCVisualManager:: ондравриббонкаптионбуттон](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribboncaptionbutton)|
|`CMFCVisualManagerWindows7::OnDrawRibbonCategory`|Переопределяет [CMFCVisualManager:: ондравриббонкатегори](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribboncategory)|
|`CMFCVisualManagerWindows7::OnDrawRibbonCategoryTab`|Переопределяет [CMFCVisualManager:: ондравриббонкатегоритаб](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribboncategorytab)|
|`CMFCVisualManagerWindows7::OnDrawRibbonDefaultPaneButton`|Переопределяет [CMFCVisualManager:: ондравриббондефаултпанебуттон](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbondefaultpanebutton)|
|`CMFCVisualManagerWindows7::OnDrawRibbonGalleryButton`|Переопределяет [CMFCVisualManager:: ондравриббонгаллерибуттон](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbongallerybutton)|
|`CMFCVisualManagerWindows7::OnDrawRibbonLaunchButton`|Переопределяет метод `CMFCVisualManager::OnDrawRibbonLaunchButton`.|
|`CMFCVisualManagerWindows7::OnDrawRibbonMenuCheckFrame`|Переопределяет [CMFCVisualManager:: ондравриббонменучеккфраме](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbonmenucheckframe)|
|`CMFCVisualManagerWindows7::OnDrawRibbonPanel`|Переопределяет [CMFCVisualManager:: ондравриббонпанел](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbonpanel)|
|`CMFCVisualManagerWindows7::OnDrawRibbonPanelCaption`|Переопределяет [CMFCVisualManager:: ондравриббонпанелкаптион](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbonpanelcaption)|
|`CMFCVisualManagerWindows7::OnDrawRibbonProgressBar`|Переопределяет [CMFCVisualManager:: ондравриббонпрогрессбар](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbonprogressbar)|
|`CMFCVisualManagerWindows7::OnDrawRibbonRecentFilesFrame`|Переопределяет [CMFCVisualManager:: ондравриббонрецентфилесфраме](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbonrecentfilesframe)|
|`CMFCVisualManagerWindows7::OnDrawRibbonSliderChannel`|Переопределяет [CMFCVisualManager:: ондравриббонслидерчаннел](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbonsliderchannel)|
|`CMFCVisualManagerWindows7::OnDrawRibbonSliderThumb`|Переопределяет [CMFCVisualManager:: ондравриббонслидерсумб](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbonsliderthumb)|
|`CMFCVisualManagerWindows7::OnDrawRibbonSliderZoomButton`|Переопределяет [CMFCVisualManager:: ондравриббонслидерзумбуттон](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbonsliderzoombutton)|
|`CMFCVisualManagerWindows7::OnDrawRibbonStatusBarPane`|Переопределяет [CMFCVisualManager:: ондравриббонстатусбарпане](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbonstatusbarpane)|
|`CMFCVisualManagerWindows7::OnDrawRibbonTabsFrame`|Переопределяет [CMFCVisualManager:: ондравриббонтабсфраме](../../mfc/reference/cmfcvisualmanager-class.md#ondrawribbontabsframe)|
|`CMFCVisualManagerWindows7::OnDrawStatusBarSizeBox`|Переопределяет [кмфквисуалманажервиндовс:: ондравстатусбарсизебокс](../../mfc/reference/cmfcvisualmanagerwindows-class.md#ondrawstatusbarsizebox)|
|`CMFCVisualManagerWindows7::OnFillBarBackground`|Переопределяет [кмфквисуалманажервиндовс:: онфиллбарбаккграунд](../../mfc/reference/cmfcvisualmanagerwindows-class.md#onfillbarbackground)|
|`CMFCVisualManagerWindows7::OnFillButtonInterior`|Переопределяет [кмфквисуалманажервиндовс:: онфиллбуттонинтериор](../../mfc/reference/cmfcvisualmanagerwindows-class.md#onfillbuttoninterior)|
|[CMFCVisualManagerWindows7:: Онфиллменуимажерект](#onfillmenuimagerect)|Платформа вызывает этот метод, когда он заполняет области вокруг изображений пунктов меню.|
|`CMFCVisualManagerWindows7::OnFillRibbonButton`|Переопределяет [CMFCVisualManager:: онфиллриббонбуттон](../../mfc/reference/cmfcvisualmanager-class.md#onfillribbonbutton)|
|`CMFCVisualManagerWindows7::OnFillRibbonQuickAccessToolBarPopup`|Переопределяет [CMFCVisualManager:: онфиллриббонкуиккакцесстулбарпопуп](../../mfc/reference/cmfcvisualmanager-class.md#onfillribbonquickaccesstoolbarpopup)|
|`CMFCVisualManagerWindows7::OnHighlightMenuItem`|Переопределяет [кмфквисуалманажервиндовс:: онхигхлигхтменуитем](../../mfc/reference/cmfcvisualmanagerwindows-class.md#onhighlightmenuitem)|
|`CMFCVisualManagerWindows7::OnNcActivate`|Переопределяет [CMFCVisualManager:: оннкактивате](../../mfc/reference/cmfcvisualmanager-class.md#onncactivate)|
|`CMFCVisualManagerWindows7::OnNcPaint`|Переопределяет [CMFCVisualManager:: оннкпаинт](../../mfc/reference/cmfcvisualmanager-class.md#onncpaint)|
|`CMFCVisualManagerWindows7::OnUpdateSystemColors`|Переопределяет [кмфквисуалманажервиндовс:: онупдатесистемколорс](../../mfc/reference/cmfcvisualmanagerwindows-class.md#onupdatesystemcolors)|
|`CMFCVisualManagerWindows7::SetResourceHandle`|Задает маркер ресурса, описывающий атрибуты визуального диспетчера.|
|`CMFCVisualManagerWindows7::SetStyle`|Задает цветовую схему `CMFCVisualManagerWindows7` графического пользовательского интерфейса.|

## <a name="remarks"></a>Комментарии

Используйте `CMFCVisualManagerWindows7` класс, чтобы изменить внешний вид приложения, чтобы имитировать приложение Windows 7 по умолчанию. Этот класс может быть недопустимым, если приложение работает в более ранней версии Windows, чем Windows 7. В этом сценарии приложение использует визуальный диспетчер по умолчанию, определенный в [CMFCVisualManager](../../mfc/reference/cmfcvisualmanager-class.md).

CMFCVisualManagerWindows7 наследует несколько методов от [класса кмфквисуалманажервиндовс](../../mfc/reference/cmfcvisualmanagerwindows-class.md) и `CMFCVisualManager` класса. Методы, перечисленные в предыдущем разделе, являются методами, созданными в `CMFCVisualManagerWindows7` классе.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[кмфкбасевисуалманажер](../../mfc/reference/cmfcbasevisualmanager-class.md)

[CMFCVisualManager](../../mfc/reference/cmfcvisualmanager-class.md)

[CMFCVisualManagerOfficeXP](../../mfc/reference/cmfcvisualmanagerofficexp-class.md)

[CMFCVisualManagerWindows](../../mfc/reference/cmfcvisualmanagerwindows-class.md)

`CMFCVisualManagerWindows7`

## <a name="requirements"></a>Требования

**Заголовок:** afxvisualmanagerwindows7. h

## <a name="cmfcvisualmanagerwindows7cmfcvisualmanagerwindows7"></a><a name="_dtorcmfcvisualmanagerwindows7"></a> CMFCVisualManagerWindows7:: ~ CMFCVisualManagerWindows7

Деструктор по умолчанию.

```
virtual ~CMFCVisualManagerWindows7();
```

## <a name="cmfcvisualmanagerwindows7cmfcvisualmanagerwindows7"></a><a name="cmfcvisualmanagerwindows7"></a> CMFCVisualManagerWindows7::CMFCVisualManagerWindows7

Конструктор по умолчанию.

```
CMFCVisualManagerWindows7();
```

## <a name="cmfcvisualmanagerwindows7getribboneditbackgroundcolor"></a><a name="getribboneditbackgroundcolor"></a> CMFCVisualManagerWindows7:: Жетриббонедитбаккграундколор

Получает цвет фона для поля ввода ленты.

```
virtual COLORREF GetRibbonEditBackgroundColor (
    CMFCRibbonRichEditCtrl* pEdit,
    BOOL bIsHighlighted,
    BOOL bIsPaneHighlighted,
    BOOL bIsDisabled);
```

### <a name="parameters"></a>Параметры

*педит*<br/>
окне Указатель на элемент управления "поле ввода". Это значение не может быть равно NULL.

*бишигхлигхтед*<br/>
заполняет Возвращает значение, указывающее, выделяется ли поле ленты.

*биспанехигхлигхтед*<br/>
заполняет Возвращает значение TRUE, если панель ленты, содержащая *педит* , выделяется.

*бисдисаблед*<br/>
заполняет Возвращает значение, указывающее, отключен ли *педит* .

### <a name="return-value"></a>Возвращаемое значение

Цвет фона поля редактирования *педит*.

### <a name="remarks"></a>Комментарии

## <a name="cmfcvisualmanagerwindows7onfillmenuimagerect"></a><a name="onfillmenuimagerect"></a> CMFCVisualManagerWindows7:: Онфиллменуимажерект

Платформа вызывает этот метод при заполнении области вокруг изображения пункта меню.

```
virtual void OnFillMenuImageRect(
    CDC* pDC,
    CMFCToolBarButton* pButton,
    CRect rectangle,
    CMFCVisualManager::AFX_BUTTON_STATE state);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства кнопки меню.

*пбуттон*<br/>
окне Указатель на объект `CMFCToolBarButton` . Платформа заполняет фон для этой кнопки.

*углами*<br/>
окне Прямоугольник, указывающий границы области изображения для кнопки меню.

*state*<br/>
окне Состояние кнопки.

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCVisualManager](../../mfc/reference/cmfcvisualmanager-class.md)<br/>
[Класс Кмфквисуалманажервиндовс](../../mfc/reference/cmfcvisualmanagerwindows-class.md)
