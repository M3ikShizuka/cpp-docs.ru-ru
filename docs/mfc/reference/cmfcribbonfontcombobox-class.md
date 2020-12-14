---
description: 'Дополнительные сведения о: Кмфкриббонфонткомбобокс Class'
title: Класс Кмфкриббонфонткомбобокс
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonFontComboBox
- AFXRIBBONCOMBOBOX/CMFCRibbonFontComboBox
- AFXRIBBONCOMBOBOX/CMFCRibbonFontComboBox::CMFCRibbonFontComboBox
- AFXRIBBONCOMBOBOX/CMFCRibbonFontComboBox::BuildFonts
- AFXRIBBONCOMBOBOX/CMFCRibbonFontComboBox::GetCharSet
- AFXRIBBONCOMBOBOX/CMFCRibbonFontComboBox::GetFontDesc
- AFXRIBBONCOMBOBOX/CMFCRibbonFontComboBox::GetFontType
- AFXRIBBONCOMBOBOX/CMFCRibbonFontComboBox::GetPitchAndFamily
- AFXRIBBONCOMBOBOX/CMFCRibbonFontComboBox::RebuildFonts
- AFXRIBBONCOMBOBOX/CMFCRibbonFontComboBox::SetFont
helpviewer_keywords:
- CMFCRibbonFontComboBox [MFC], CMFCRibbonFontComboBox
- CMFCRibbonFontComboBox [MFC], BuildFonts
- CMFCRibbonFontComboBox [MFC], GetCharSet
- CMFCRibbonFontComboBox [MFC], GetFontDesc
- CMFCRibbonFontComboBox [MFC], GetFontType
- CMFCRibbonFontComboBox [MFC], GetPitchAndFamily
- CMFCRibbonFontComboBox [MFC], RebuildFonts
- CMFCRibbonFontComboBox [MFC], SetFont
ms.assetid: 33b4db50-df4f-45fa-8f05-2e6e73c31435
ms.openlocfilehash: 8a91f13f4e478512dfab3b9fcb942f96be0b9d9b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333475"
---
# <a name="cmfcribbonfontcombobox-class"></a>Класс Кмфкриббонфонткомбобокс

Реализует поле со списком, содержащее список шрифтов. Необходимо задать поле со списком на панели ленты.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonFontComboBox : public CMFCRibbonComboBox
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CMFCRibbonFontComboBox::~CMFCRibbonFontComboBox`|Деструктор.|

### <a name="protected-constructors"></a>Защищенные конструкторы

|Имя|Описание|
|----------|-----------------|
|[CMFCRibbonFontComboBox::CMFCRibbonFontComboBox](#cmfcribbonfontcombobox)|Создает и инициализирует объект `CMFCRibbonFontComboBox`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCRibbonFontComboBox::BuildFonts](#buildfonts)|Заполняет поле со списком шрифтов на ленте на основе таких заданных параметров, как тип и семейство шрифтов, а также кодировка и шаг.|
|`CMFCRibbonFontComboBox::CreateObject`|Используется платформой для создания динамического экземпляра этого типа класса.|
|[CMFCRibbonFontComboBox::GetCharSet](#getcharset)|Возвращает указанный набор символов.|
|[CMFCRibbonFontComboBox::GetFontDesc](#getfontdesc)||
|[CMFCRibbonFontComboBox::GetFontType](#getfonttype)|Возвращает типы шрифтов, отображаемые в поле со списком. Допустимые значения: DEVICE_FONTTYPE, RASTER_FONTTYPE и TRUETYPE_FONTTYPE, а также любые их битовые комбинации.|
|[CMFCRibbonFontComboBox::GetPitchAndFamily](#getpitchandfamily)|Возвращает шаг и семейство шрифтов, отображаемых в поле со списком.|
|`CMFCRibbonFontComboBox::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|
|[CMFCRibbonFontComboBox::RebuildFonts](#rebuildfonts)|Заполняет поле со списком шрифтов на ленте на основе таких ранее заданных параметров, как тип и семейство шрифтов, а также кодировка и шаг.|
|[CMFCRibbonFontComboBox::SetFont](#setfont)|Выбирает указанный шрифт в поле со списком.|

## <a name="remarks"></a>Комментарии

После создания `CMFCRibbonFontComboBox` объекта добавьте его на панель ленты, вызвав [CMFCRibbonPanel:: Add](../../mfc/reference/cmfcribbonpanel-class.md#add).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)

[CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)

[CMFCRibbonEdit](../../mfc/reference/cmfcribbonedit-class.md)

[CMFCRibbonComboBox](../../mfc/reference/cmfcribboncombobox-class.md)

[CMFCRibbonFontComboBox](../../mfc/reference/cmfcribbonfontcombobox-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонкомбобокс. h

## <a name="cmfcribbonfontcomboboxbuildfonts"></a><a name="buildfonts"></a> Кмфкриббонфонткомбобокс:: Буилдфонтс

Заполняет поле со списком на ленте с помощью шрифтов.

```cpp
void BuildFonts(
    int nFontType = DEVICE_FONTTYPE | RASTER_FONTTYPE | TRUETYPE_FONTTYPE,
    BYTE nCharSet = DEFAULT_CHARSET,
    BYTE nPitchAndFamily = DEFAULT_PITCH);
```

### <a name="parameters"></a>Параметры

*нфонттипе*<br/>
окне Указывает тип шрифта для добавляемых шрифтов.

*Тип nChar*<br/>
окне Задает набор символов добавляемых шрифтов.

*нпитчандфамили*<br/>
окне Задает шаг и семейство шрифтов для добавления.

## <a name="cmfcribbonfontcomboboxcmfcribbonfontcombobox"></a><a name="cmfcribbonfontcombobox"></a> Кмфкриббонфонткомбобокс:: Кмфкриббонфонткомбобокс

Создает и инициализирует объект [кмфкриббонфонткомбобокс](../../mfc/reference/cmfcribbonfontcombobox-class.md) .

```
CMFCRibbonFontComboBox(
    UINT nID,
    int nFontType = DEVICE_FONTTYPE | RASTER_FONTTYPE | TRUETYPE_FONTTYPE,
    BYTE nCharSet = DEFAULT_CHARSET,
    BYTE nPitchAndFamily = DEFAULT_PITCH,
    int nWidth = -1);
```

### <a name="parameters"></a>Параметры

*nID*<br/>
окне Идентификатор команды, которая выполняется, когда пользователь выбирает элемент из поля со списком.

*нфонттипе*<br/>
окне Указывает, какие типы шрифтов должны отображаться в поле со списком. Допустимые значения: DEVICE_FONTTYPE, RASTER_FONTTYPE и TRUETYPE_FONTTYPE, а также любые их битовые комбинации.

*Тип nChar*<br/>
окне Фильтрует шрифты в поле со списком, чтобы они принадлежали к указанной кодировке.

*нпитчандфамили*<br/>
окне Задает шаг и семейство шрифтов, отображаемых в поле со списком.

*нвидс*<br/>
окне Задает ширину (в пикселях) поля со списком.

### <a name="remarks"></a>Комментарии

Дополнительные сведения о возможных значениях параметров *нфонттипе* см. в разделе [енумфонтфампрок](/previous-versions/dd162621\(v=vs.85\)) в документации по Windows SDK.

Дополнительные сведения о допустимых кодировках, которые можно присвоить параметру *nchar*, а также допустимые значения, которые могут быть назначены *нпитчандфамили*, см. в разделе [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfontw) в документации по Windows SDK.

## <a name="cmfcribbonfontcomboboxgetfontdesc"></a><a name="getfontdesc"></a> Кмфкриббонфонткомбобокс:: Жетфонтдеск

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
const CMFCFontInfo* GetFontDesc(int iIndex = -1) const;
```

### <a name="parameters"></a>Параметры

окне *ииндекс*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonfontcomboboxrebuildfonts"></a><a name="rebuildfonts"></a> Кмфкриббонфонткомбобокс:: Ребуилдфонтс

Заполняет поле со списком на ленте шрифтами ранее указанного типа шрифта, набора символов и числа и семейства.

```cpp
void RebuildFonts();
```

### <a name="remarks"></a>Комментарии

Можно указать тип шрифта, набор символов и высоту и семейство шрифтов для включения в поле со списком шрифтов ленты в [конструкторе](#cmfcribbonfontcombobox) для этого класса или путем вызова [Кмфкриббонфонткомбобокс:: буилдфонтс](#buildfonts).

## <a name="cmfcribbonfontcomboboxsetfont"></a><a name="setfont"></a> Кмфкриббонфонткомбобокс:: Сетфонт

Выбирает указанный шрифт в поле со списком.

```
BOOL SetFont(
    LPCTSTR lpszName,
    BYTE nCharSet = DEFAULT_CHARSET,
    BOOL bExact = FALSE);
```

### <a name="parameters"></a>Параметры

' Лпсзнаме * задает имя выбранного шрифта.

*Тип nChar*<br/>
Задает кодировку для выбранного шрифта.

*бексакт*<br/>
Значение TRUE, чтобы указать, что кодировка должна совпадать при выборе шрифта; Значение FALSE, чтобы указать, что кодировка может игнорироваться при выборе шрифта.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если указанный шрифт найден и выбран. в противном случае — нуль.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonfontcomboboxgetcharset"></a><a name="getcharset"></a> Кмфкриббонфонткомбобокс:: charset

Возвращает указанный набор символов.

```
BYTE GetCharSet() const;
```

### <a name="return-value"></a>Возвращаемое значение

Кодировка (см. раздел LOGFONT в документации по Windows SDK).

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonfontcomboboxgetfonttype"></a><a name="getfonttype"></a> Кмфкриббонфонткомбобокс:: Жетфонттипе

Возвращает типы шрифтов, отображаемые в поле со списком. Допустимые значения: DEVICE_FONTTYPE, RASTER_FONTTYPE и TRUETYPE_FONTTYPE, а также любые их битовые комбинации.

```
int GetFontType() const;
```

### <a name="return-value"></a>Возвращаемое значение

Типы шрифтов (см. раздел Енумфонтфампрок в документации по Windows SDK).

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonfontcomboboxgetpitchandfamily"></a><a name="getpitchandfamily"></a> Кмфкриббонфонткомбобокс:: Жетпитчандфамили

Возвращает шаг и семейство шрифтов, отображаемых в поле со списком.

```
BYTE GetPitchAndFamily() const;
```

### <a name="return-value"></a>Возвращаемое значение

Шаг и семейство (см. раздел LOGFONT в документации по Windows SDK).

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкриббонкомбобокс](../../mfc/reference/cmfcribboncombobox-class.md)
