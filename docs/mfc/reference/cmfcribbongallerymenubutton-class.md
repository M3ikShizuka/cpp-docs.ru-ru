---
description: 'Дополнительные сведения о: Кмфкриббонгаллерименубуттон Class'
title: Класс Кмфкриббонгаллерименубуттон
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonGalleryMenuButton
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGalleryMenuButton
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGalleryMenuButton::CMFCRibbonGalleryMenuButton
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGalleryMenuButton::CopyFrom
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGalleryMenuButton::CreatePopupMenu
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGalleryMenuButton::GetPalette
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGalleryMenuButton::HasButton
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGalleryMenuButton::IsEmptyMenuAllowed
helpviewer_keywords:
- CMFCRibbonGalleryMenuButton [MFC], CMFCRibbonGalleryMenuButton
- CMFCRibbonGalleryMenuButton [MFC], CopyFrom
- CMFCRibbonGalleryMenuButton [MFC], CreatePopupMenu
- CMFCRibbonGalleryMenuButton [MFC], GetPalette
- CMFCRibbonGalleryMenuButton [MFC], HasButton
- CMFCRibbonGalleryMenuButton [MFC], IsEmptyMenuAllowed
ms.assetid: 4d459d9b-8b1a-4371-92f6-dc4ce6cc42c8
ms.openlocfilehash: ee527178ba90b968b1968ae0c06dbd8629d8d1e9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321856"
---
# <a name="cmfcribbongallerymenubutton-class"></a>Класс Кмфкриббонгаллерименубуттон

Реализует кнопку меню ленты, которая содержит коллекцию лент.
Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonGalleryMenuButton : public CMFCToolBarMenuButton
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMFCRibbonGalleryMenuButton::CMFCRibbonGalleryMenuButton](#cmfcribbongallerymenubutton)|Создает и инициализирует объект `CMFCRibbonGalleryMenuButton`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCRibbonGalleryMenuButton::CopyFrom](#copyfrom)|(Переопределяет [кмфктулбарменубуттон:: CopyFrom](../../mfc/reference/cmfctoolbarmenubutton-class.md#copyfrom).)|
|[CMFCRibbonGalleryMenuButton::CreatePopupMenu](#createpopupmenu)|(Переопределяет [кмфктулбарменубуттон:: креатепопупмену](../../mfc/reference/cmfctoolbarmenubutton-class.md#createpopupmenu).)|
|[CMFCRibbonGalleryMenuButton::GetPalette](#getpalette)||
|[CMFCRibbonGalleryMenuButton::HasButton](#hasbutton)|(Переопределяет `CMFCToolBarMenuButton::HasButton`.)|
|[CMFCRibbonGalleryMenuButton::IsEmptyMenuAllowed](#isemptymenuallowed)|(Переопределяет [кмфктулбарменубуттон:: исемптименуалловед](../../mfc/reference/cmfctoolbarmenubutton-class.md#isemptymenuallowed).)|

### <a name="remarks"></a>Комментарии

Кнопка коллекции отображается в качестве всплывающего меню со стрелкой. Когда пользователь нажимает эту кнопку, открывается коллекция изображений. При создании кнопки коллекции необходимо задать список необходимых изображений.

## <a name="example"></a>Пример

В этом примере демонстрируется, как можно отобразить коллекцию маркеров с помощью кнопки меню:

```cpp
BOOL CMainFrame::OnShowPopupMenu (CMFCPopupMenu* pMenuPopup)
{
    int nBulletIndex = pMenuBar->CommandToIndex (ID_PARA_BULLETS);

    if (nBulletIndex>= 0)
    {
        CMFCToolBarButton* pExButton =
        pMenuBar->GetButton(nBulletIndex);
        ASSERT_VALID (pExButton);

        CMFCRibbonGalleryMenuButton paletteBullet (
        pExButton->m_nID,
        pExButton->GetImage (),
        pExButton->m_strText);

        InitBulletPalette (&paletteBullet.GetPalette ());

        pMenuBar->ReplaceButton (ID_PARA_BULLETS,
        paletteBullet);
    }
}
```

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)\
└ &nbsp; [CMFCToolBarButton](../../mfc/reference/cmfctoolbarbutton-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [Кмфктулбарменубуттон](../../mfc/reference/cmfctoolbarmenubutton-class.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└ &nbsp; [Кмфкриббонгаллерименубуттон](../../mfc/reference/cmfcribbongallerymenubutton-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонпалеттегаллери. h

## <a name="cmfcribbongallerymenubuttoncopyfrom"></a><a name="copyfrom"></a> Кмфкриббонгаллерименубуттон:: CopyFrom

```
virtual void CopyFrom(const CMFCToolBarButton& src);
```

### <a name="parameters"></a>Параметры

окне *src*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbongallerymenubuttoncmfcribbongallerymenubutton"></a><a name="cmfcribbongallerymenubutton"></a> Кмфкриббонгаллерименубуттон:: Кмфкриббонгаллерименубуттон

Создает и инициализирует объект [кмфкриббонгаллерименубуттон](../../mfc/reference/cmfcribbongallerymenubutton-class.md) .

```
CMFCRibbonGalleryMenuButton(
    UINT uiID,
    int iImage,
    LPCTSTR lpszText,
    CMFCToolBarImages& imagesPalette);

CMFCRibbonGalleryMenuButton(
    UINT uiID,
    int iImage,
    LPCTSTR lpszText,
    UINT uiImagesPaletteResID = 0,
    int cxPaletteImage = 0);
```

### <a name="parameters"></a>Параметры

*uiID*<br/>
Идентификатор команды для кнопки. Это значение, отправляемое в WM_COMMAND сообщение, когда пользователь нажимает эту кнопку.

*иимаже*<br/>
Индекс изображения, отображаемого с помощью кнопки меню "Коллекция". Изображения хранятся в параметре *имажеспалетте* .

*lpszText*<br/>
Текст, отображаемый в кнопке меню.

*имажеспалетте*<br/>
Содержит список изображений, отображаемых в коллекции.

*уиимажеспалеттересид*<br/>
Идентификатор ресурса списка изображений, отображаемых в коллекции.

*ккспалеттеимаже*<br/>
Задает ширину изображения, отображаемого в коллекции (в пикселях).

### <a name="remarks"></a>Комментарии

Кнопка меню Коллекция отображается как всплывающее меню со стрелкой. Когда пользователь нажимает эту кнопку, открывается коллекция изображений.

### <a name="example"></a>Пример

В следующем примере показано, как использовать конструктор `CMFCRibbonGalleryMenuButton` класса. Этот фрагмент кода является частью [демонстрационного примера MS Office 2007](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_MSOffice2007Demo#8](../../mfc/reference/codesnippet/cpp/cmfcribbongallerymenubutton-class_1.cpp)]

## <a name="cmfcribbongallerymenubuttoncreatepopupmenu"></a><a name="createpopupmenu"></a> Кмфкриббонгаллерименубуттон:: Креатепопупмену

```
virtual CMFCPopupMenu* CreatePopupMenu();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbongallerymenubuttongetpalette"></a><a name="getpalette"></a> Кмфкриббонгаллерименубуттон:: "Palette"

```
CMFCRibbonGallery& GetPalette();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbongallerymenubuttonhasbutton"></a><a name="hasbutton"></a> Кмфкриббонгаллерименубуттон:: Хасбуттон

```
virtual BOOL HasButton() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbongallerymenubuttonisemptymenuallowed"></a><a name="isemptymenuallowed"></a> Кмфкриббонгаллерименубуттон:: Исемптименуалловед

```
virtual BOOL IsEmptyMenuAllowed() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфктулбарменубуттон](../../mfc/reference/cmfctoolbarmenubutton-class.md)<br/>
[Класс Кмфкриббонгаллери](../../mfc/reference/cmfcribbongallery-class.md)
