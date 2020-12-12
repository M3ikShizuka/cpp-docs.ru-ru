---
description: 'Дополнительные сведения о: Кмфкриббонколорбуттон Class'
title: класс CMFCRibbonColorButton
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonColorButton
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::CMFCRibbonColorButton
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::AddColorsGroup
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::EnableAutomaticButton
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::EnableOtherButton
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::GetAutomaticColor
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::GetColor
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::GetColorBoxSize
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::GetColumns
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::GetHighlightedColor
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::RemoveAllColorGroups
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::SetColor
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::SetColorBoxSize
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::SetColorName
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::SetColumns
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::SetDocumentColors
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::SetPalette
- AFXRIBBONCOLORBUTTON/CMFCRibbonColorButton::UpdateColor
helpviewer_keywords:
- CMFCRibbonColorButton [MFC], CMFCRibbonColorButton
- CMFCRibbonColorButton [MFC], AddColorsGroup
- CMFCRibbonColorButton [MFC], EnableAutomaticButton
- CMFCRibbonColorButton [MFC], EnableOtherButton
- CMFCRibbonColorButton [MFC], GetAutomaticColor
- CMFCRibbonColorButton [MFC], GetColor
- CMFCRibbonColorButton [MFC], GetColorBoxSize
- CMFCRibbonColorButton [MFC], GetColumns
- CMFCRibbonColorButton [MFC], GetHighlightedColor
- CMFCRibbonColorButton [MFC], RemoveAllColorGroups
- CMFCRibbonColorButton [MFC], SetColor
- CMFCRibbonColorButton [MFC], SetColorBoxSize
- CMFCRibbonColorButton [MFC], SetColorName
- CMFCRibbonColorButton [MFC], SetColumns
- CMFCRibbonColorButton [MFC], SetDocumentColors
- CMFCRibbonColorButton [MFC], SetPalette
- CMFCRibbonColorButton [MFC], UpdateColor
ms.assetid: 6b4b4ee3-8cc0-41b4-a4eb-93e8847008e1
ms.openlocfilehash: a350339559febdc9346dcf8b342d274d00bab391
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97293720"
---
# <a name="cmfcribboncolorbutton-class"></a>класс CMFCRibbonColorButton

Класс `CMFCRibbonColorButton` реализует кнопку цвета, которую можно добавить на панель ленты. Кнопка цвета ленты отображает раскрывающееся меню, содержащее одну или несколько палитр.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonColorButton : public CMFCRibbonGallery
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMFCRibbonColorButton::CMFCRibbonColorButton](#cmfcribboncolorbutton)||

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонколорбуттон:: Аддколорсграуп](#addcolorsgroup)|Добавляет группу цветов в стандартную область цветов.|
|[Кмфкриббонколорбуттон:: Енаблеаутоматикбуттон](#enableautomaticbutton)|Указывает, нажата ли кнопка **Автоматически** .|
|[Кмфкриббонколорбуттон:: Енаблеосербуттон](#enableotherbutton)|Активирует кнопку **Другие** .|
|[CMFCRibbonColorButton::GetAutomaticColor](#getautomaticcolor)||
|[Кмфкриббонколорбуттон:: "Color"](#getcolor)|Возвращает выбранный в данный момент цвет.|
|[Кмфкриббонколорбуттон:: Жетколорбокссизе](#getcolorboxsize)|Возвращает размер цветовых элементов, отображаемых на цветовой панели.|
|[CMFCRibbonColorButton::GetColumns](#getcolumns)||
|[Кмфкриббонколорбуттон:: Жесигхлигхтедколор](#gethighlightedcolor)|Возвращает цвет элемента, выбранного в данный момент во всплывающей цветовой палитре.|
|[Кмфкриббонколорбуттон:: Ремовеаллколорграупс](#removeallcolorgroups)|Удаляет все группы цветов из стандартной области цветов.|
|[Кмфкриббонколорбуттон:: Сетколор](#setcolor)|Выбирает цвет в стандартной области цветов.|
|[Кмфкриббонколорбуттон:: Сетколорбокссизе](#setcolorboxsize)|Задает размер всех цветовых элементов, отображаемых на цветовой панели.|
|[CMFCRibbonColorButton::SetColorName](#setcolorname)||
|[CMFCRibbonColorButton::SetColumns](#setcolumns)||
|[Кмфкриббонколорбуттон:: Сетдокументколорс](#setdocumentcolors)|Задает список значений RGB, которые должны отображаться в области цветов документа.|
|[CMFCRibbonColorButton::SetPalette](#setpalette)||
|[CMFCRibbonColorButton::UpdateColor](#updatecolor)||

## <a name="remarks"></a>Комментарии

Когда пользователь нажимает кнопку цвета на ленте, отображается цветовая панель. По умолчанию эта панель содержит палитру выбора цвета, называемую стандартной областью цветов. Помимо этого, цветовая панель может содержать кнопку **Автоматически** , которая позволяет пользователю выбрать цвет по умолчанию, и кнопку **Другие** , которая позволяет открыть всплывающую цветовую палитру с дополнительными цветами.

## <a name="example"></a>Пример

В приведенном ниже примере демонстрируется использование различных методов класса `CMFCRibbonColorButton` . В нем показано, как создать объект `CMFCRibbonColorButton` , задать большое изображение, активировать кнопку **Автоматически** , активировать кнопку **Другие** , задать число столбцов, задать размер всех цветовых элементов, отображаемых на цветовой панели, добавить группу цветов в стандартную область цветов и указать список значений RGB, которые должны отображаться в области цветов документа. Этот фрагмент кода входит в состав [примера Draw Client](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_DrawClient#3](../../mfc/reference/codesnippet/cpp/cmfcribboncolorbutton-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)

[CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)

[CMFCRibbonGallery](../../mfc/reference/cmfcribbongallery-class.md)

[CMFCRibbonColorButton](../../mfc/reference/cmfcribboncolorbutton-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** afxribboncolorbutton.h

## <a name="cmfcribboncolorbuttonaddcolorsgroup"></a><a name="addcolorsgroup"></a> Кмфкриббонколорбуттон:: Аддколорсграуп

Добавляет группу цветов в стандартную область цветов.

```cpp
void AddColorsGroup(
    LPCTSTR lpszName,
    const CList<COLORREF,COLORREF>& lstColors,
    BOOL bContiguousColumns=FALSE);
```

### <a name="parameters"></a>Параметры

*лпсзнаме*<br/>
окне Имя группы.

*лстколорс*<br/>
окне Список цветов.

*бконтигуаусколумнс*<br/>
окне Управляет отображением элементов цвета в группе. Если значение равно TRUE, элементы цвета рисуются без вертикальных пробелов. Если значение равно FALSE, элементы цвета рисуются с помощью вертикального пробела.

### <a name="remarks"></a>Комментарии

Используйте эту функцию, чтобы во всплывающем окне цвета отображалось несколько групп цветов. Можно управлять отображением цветов в группе.

## <a name="cmfcribboncolorbuttoncmfcribboncolorbutton"></a><a name="cmfcribboncolorbutton"></a> Кмфкриббонколорбуттон:: Кмфкриббонколорбуттон

Формирует объект `CMFCRibbonColorButton`.

```
CMFCRibbonColorButton();

CMFCRibbonColorButton(
    UINT nID,
    LPCTSTR lpszText,
    int nSmallImageIndex,
    COLORREF color = RGB(0, 0, 0));

CMFCRibbonColorButton(
    UINT nID,
    LPCTSTR lpszText,
    BOOL bSimpleButtonLook,
    int nSmallImageIndex,
    int nLargeImageIndex,
    COLORREF color = RGB(0, 0, 0));
```

### <a name="parameters"></a>Параметры

*nID*<br/>
окне Указывает идентификатор команды, выполняемой при нажатии пользователем кнопки.

*lpszText*<br/>
окне Задает текст, отображаемый на кнопке.

*нсмаллимажеиндекс*<br/>
окне Отсчитываемый от нуля индекс мелкого изображения, отображаемого на кнопке.

*color*<br/>
окне Цвет кнопки (по умолчанию — черный).

*бсимплебуттонлук*<br/>
окне Если значение равно TRUE, кнопка рисуется как простой прямоугольник.

*нларжеимажеиндекс*<br/>
окне Отсчитываемый от нуля индекс крупного изображения, отображаемого на кнопке.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncolorbuttonenableautomaticbutton"></a><a name="enableautomaticbutton"></a> Кмфкриббонколорбуттон:: Енаблеаутоматикбуттон

Указывает, нажата ли кнопка **Автоматически** .

```cpp
void EnableAutomaticButton(
    LPCTSTR lpszLabel,
    COLORREF colorAutomatic,
    BOOL bEnable=TRUE,
    LPCTSTR lpszToolTip=NULL,
    BOOL bOnTop=TRUE,
    BOOL bDrawBorder=FALSE);
```

### <a name="parameters"></a>Параметры

*лпсзлабел*<br/>
окне Метка для кнопки " **автоматически** ".

*колораутоматик*<br/>
окне Значение RGB, указывающее цвет по умолчанию для кнопки **автоматически** .

*bEnable*<br/>
окне Значение TRUE, если включена **Автоматическая** кнопка. Значение FALSE, если оно отключено.

*lpszToolTip*<br/>
окне Всплывающая подсказка кнопки **автоматически** .

*бонтоп*<br/>
окне Указывает, находится ли **Автоматическая** кнопка сверху, перед цветовой палитрой.

*бдравбордер*<br/>
окне Значение TRUE, если приложение рисует границу вокруг цветовой полосы на кнопке цвета ленты. Цветовая строка отображает выбранный в данный момент цвет. FALSE, если приложение не рисует границу

## <a name="cmfcribboncolorbuttonenableotherbutton"></a><a name="enableotherbutton"></a> Кмфкриббонколорбуттон:: Енаблеосербуттон

Активирует кнопку **Другие** .

```cpp
void EnableOtherButton(
    LPCTSTR lpszLabel,
    LPCTSTR lpszToolTip=NULL);
```

### <a name="parameters"></a>Параметры

*лпсзлабел*<br/>
Метка кнопки.

*lpszToolTip*<br/>
Текст подсказки для **другой** кнопки.

### <a name="remarks"></a>Комментарии

**Вторая** кнопка отображается под группой цветов. При **нажатии пользователем кнопки отображается** диалоговое окно выбора цвета.

## <a name="cmfcribboncolorbuttongetautomaticcolor"></a><a name="getautomaticcolor"></a> Кмфкриббонколорбуттон:: Жетаутоматикколор

Извлекает текущий цвет автоматической кнопки.

```
COLORREF GetAutomaticColor() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение цвета RGB, представляющее текущий цвет автоматической кнопки.

### <a name="remarks"></a>Комментарии

Цвет автоматической кнопки задается `colorAutomatic` параметром, передаваемым `CMFCRibbonColorButton::EnableAutomaticButton` методу.

## <a name="cmfcribboncolorbuttongetcolor"></a><a name="getcolor"></a> Кмфкриббонколорбуттон:: "Color"

Возвращает выбранный в данный момент цвет.

```
COLORREF GetColor() const;
```

### <a name="return-value"></a>Возвращаемое значение

Цвет, выбранный при нажатии кнопки.

## <a name="cmfcribboncolorbuttongetcolorboxsize"></a><a name="getcolorboxsize"></a> Кмфкриббонколорбуттон:: Жетколорбокссизе

Возвращает размер цветовых элементов, отображаемых на цветовой панели.

```
CSize GetColorBoxSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Размер кнопок цвета в раскрывающейся палитре цветов.

## <a name="cmfcribboncolorbuttongetcolumns"></a><a name="getcolumns"></a> Кмфкриббонколорбуттон:: DataColumn

Возвращает число элементов в строке галереи на кнопке цвета ленты.

```
int GetColumns() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает количество значков в каждой строке.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncolorbuttongethighlightedcolor"></a><a name="gethighlightedcolor"></a> Кмфкриббонколорбуттон:: Жесигхлигхтедколор

Возвращает цвет выбранного в данный момент элемента в палитре цветов во всплывающем окне.

```
COLORREF GetHighlightedColor() const;
```

### <a name="return-value"></a>Возвращаемое значение

Цвет выбранного в данный момент элемента во всплывающей палитре цветов.

## <a name="cmfcribboncolorbuttonremoveallcolorgroups"></a><a name="removeallcolorgroups"></a> Кмфкриббонколорбуттон:: Ремовеаллколорграупс

Удаляет все группы цветов из стандартной области цветов.

```cpp
void RemoveAllColorGroups();
```

## <a name="cmfcribboncolorbuttonsetcolor"></a><a name="setcolor"></a> Кмфкриббонколорбуттон:: Сетколор

Выбирает цвет в стандартной области цветов.

```cpp
void SetColor(COLORREF color);
```

### <a name="parameters"></a>Параметры

*color*<br/>
окне Заданный цвет.

## <a name="cmfcribboncolorbuttonsetcolorboxsize"></a><a name="setcolorboxsize"></a> Кмфкриббонколорбуттон:: Сетколорбокссизе

Задает размер всех цветовых элементов, отображаемых на цветовой панели.

```cpp
void SetColorBoxSize(CSize sizeBox);
```

### <a name="parameters"></a>Параметры

*сизебокс*<br/>
окне Новый размер кнопок цвета в палитре цветов.

## <a name="cmfcribboncolorbuttonsetcolorname"></a><a name="setcolorname"></a> Кмфкриббонколорбуттон:: Сетколорнаме

Задает новое имя для указанного цвета.

```
static void __stdcall SetColorName(
    COLORREF color,
    const CString& strName);
```

### <a name="parameters"></a>Параметры

*color*<br/>
окне Значение RGB цвета.

*strName*<br/>
окне Новое имя для указанного цвета.

### <a name="remarks"></a>Комментарии

Так как он вызывает `CMFCColorBar::SetColorName` , этот метод изменяет имя указанного цвета во всех `CMFCColorBar` объектах приложения.

## <a name="cmfcribboncolorbuttonsetcolumns"></a><a name="setcolumns"></a> Кмфкриббонколорбуттон:: SetColumns

Задает число столбцов, отображаемых в таблице цветов, которые отображаются пользователю в процессе выбора цвета пользователем.

```cpp
void SetColumns(int nColumns);
```

### <a name="parameters"></a>Параметры

*nColumns*<br/>
окне Количество цветных значков, отображаемых в каждой строке.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncolorbuttonsetdocumentcolors"></a><a name="setdocumentcolors"></a> Кмфкриббонколорбуттон:: Сетдокументколорс

Задает список значений RGB, которые должны отображаться в области цветов документа.

```cpp
void SetDocumentColors(
    LPCTSTR lpszLabel,
    CList<COLORREF,COLORREF>& lstColors);
```

### <a name="parameters"></a>Параметры

*лпсзлабел*<br/>
окне Текст, отображаемый с цветами документа.

*лстколорс*<br/>
окне Ссылка на список значений RGB.

## <a name="cmfcribboncolorbuttonsetpalette"></a><a name="setpalette"></a> Кмфкриббонколорбуттон:: Сетпалетте

Задает стандартные цвета, отображаемые в таблице цветов, которая отображается на кнопке Color (цвет).

```cpp
void SetPalette(CPalette* pPalette);
```

### <a name="parameters"></a>Параметры

*ппалетте*<br/>
окне Указатель на цветовую палитру.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboncolorbuttonupdatecolor"></a><a name="updatecolor"></a> Кмфкриббонколорбуттон:: Упдатеколор

Вызывается структурой, когда пользователь выбирает цвет из таблицы цветов, отображаемой при нажатии пользователем кнопки выбора цвета.

```cpp
void UpdateColor(COLORREF color);
```

### <a name="parameters"></a>Параметры

*color*<br/>
окне Цвет, выбранный пользователем.

### <a name="remarks"></a>Комментарии

`CMFCRibbonColorButton::UpdateColor`Метод изменяет цвет выбранной кнопки и уведомляет его родителя, отправляя WM_COMMAND сообщение с BN_CLICKED стандартным уведомлением. Чтобы получить выбранный цвет, используйте метод [кмфкриббонколорбуттон::](#getcolor) WebMethod.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкриббонгаллери](../../mfc/reference/cmfcribbongallery-class.md)
