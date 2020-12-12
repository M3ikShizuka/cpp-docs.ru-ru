---
description: 'Дополнительные сведения о: Кмфкколордиалог Class'
title: Класс Кмфкколордиалог
ms.date: 11/04/2016
f1_keywords:
- CMFCColorDialog
- AFXCOLORDIALOG/CMFCColorDialog
- AFXCOLORDIALOG/CMFCColorDialog::CMFCColorDialog
- AFXCOLORDIALOG/CMFCColorDialog::GetColor
- AFXCOLORDIALOG/CMFCColorDialog::GetPalette
- AFXCOLORDIALOG/CMFCColorDialog::RebuildPalette
- AFXCOLORDIALOG/CMFCColorDialog::SetCurrentColor
- AFXCOLORDIALOG/CMFCColorDialog::SetNewColor
- AFXCOLORDIALOG/CMFCColorDialog::SetPageOne
- AFXCOLORDIALOG/CMFCColorDialog::SetPageTwo
helpviewer_keywords:
- CMFCColorDialog [MFC], CMFCColorDialog
- CMFCColorDialog [MFC], GetColor
- CMFCColorDialog [MFC], GetPalette
- CMFCColorDialog [MFC], RebuildPalette
- CMFCColorDialog [MFC], SetCurrentColor
- CMFCColorDialog [MFC], SetNewColor
- CMFCColorDialog [MFC], SetPageOne
- CMFCColorDialog [MFC], SetPageTwo
ms.assetid: 235bbbbc-a3b1-46e0-801b-fb55093ec579
ms.openlocfilehash: 4279a92ef22253ce2909acce88d77428e3ed5495
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327682"
---
# <a name="cmfccolordialog-class"></a>Класс Кмфкколордиалог

`CMFCColorDialog`Класс представляет диалоговое окно выбора цвета.

## <a name="syntax"></a>Синтаксис

```
class CMFCColorDialog : public CDialogEx
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкколордиалог:: Кмфкколордиалог](#cmfccolordialog)|Формирует объект `CMFCColorDialog`.|
|`CMFCColorDialog::~CMFCColorDialog`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкколордиалог:: "Color"](#getcolor)|Возвращает текущий выбранный цвет.|
|[Кмфкколордиалог:: "Palette"](#getpalette)|Возвращает палитру цвета.|
|`CMFCColorDialog::PreTranslateMessage`|Преобразует сообщения окна до их отправки в функции Windows [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage) и [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) . Синтаксис и дополнительные сведения см. в разделе [CWnd::P ретранслатемессаже](../../mfc/reference/cwnd-class.md#pretranslatemessage). (Переопределяет `CDialogEx::PreTranslateMessage`.)|
|[Кмфкколордиалог:: Ребуилдпалетте](#rebuildpalette)|Извлекает палитру из системной палитры.|
|[Кмфкколордиалог:: Сеткуррентколор](#setcurrentcolor)|Задает текущий выбранный цвет.|
|[Кмфкколордиалог:: Сетневколор](#setnewcolor)|Задает наиболее эквивалентный цвет для указанного значения RGB.|
|[Кмфкколордиалог:: Сетпажеоне](#setpageone)|Выбирает значение RGB для первой страницы свойств.|
|[Кмфкколордиалог:: Сетпажетво](#setpagetwo)|Выбирает значение RGB для второй страницы свойств.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|`m_bIsMyPalette`|Значение TRUE, если диалоговое окно выбора цвета использует собственную цветовую палитру, или FALSE, если диалоговое окно использует палитру, указанную в `CMFCColorDialog` конструкторе.|
|`m_bPickerMode`|Значение TRUE, если пользователь выбирает цвет из диалогового окна выбора; в противном случае — значение FALSE.|
|`m_btnColorSelect`|Кнопка цвета, выбранная пользователем.|
|`m_CurrentColor`|Выбранный в данный момент цвет.|
|`m_hcurPicker`|Курсор, используемый для выбора цвета.|
|`m_NewColor`|Выбранный потенциальный цвет, который можно навсегда выбрать или вернуть к исходному цвету.|
|`m_pColourSheetOne`|Указатель на первую страницу свойств на странице свойств выбора цвета.|
|`m_pColourSheetTwo`|Указатель на вторую страницу свойств на странице свойств выбора цвета.|
|`m_pPalette`|Текущая логическая палитра.|
|`m_pPropSheet`|Указатель на страницу свойств для диалогового окна "Выбор цвета".|
|`m_wndColors`|Управляющий объект палитры цветов.|
|`m_wndStaticPlaceHolder`|Статический элемент управления, являющийся заполнителем для вкладки свойств палитры цветов.|

## <a name="remarks"></a>Комментарии

Диалоговое окно Выбор цвета отображается в виде страницы свойств с двумя страницами. На первой странице выбирается Стандартный цвет из системной палитры. на второй странице выберите пользовательский цвет.

Можно создать `CMFCColorDialog` объект в стеке, а затем вызвать `DoModal` , передав исходный цвет в качестве параметра в `CMFCColorDialog` конструктор. Затем диалоговое окно выбора цвета создает несколько объектов [класса кмфкколорпиккерктрл](../../mfc/reference/cmfccolorpickerctrl-class.md) для работы с каждой цветовой палитрой.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CDialogEx](../../mfc/reference/cdialogex-class.md)

[CMFCColorDialog](../../mfc/reference/cmfccolordialog-class.md)

## <a name="example"></a>Пример

В следующем примере показано, как настроить диалоговое окно цвета с помощью различных методов в `CMFCColorDialog` классе. В этом примере показано, как задать текущий и новые цвета диалогового окна, а также как установить красный, зеленый и синий компоненты выбранного цвета на двух страницах свойств диалогового окна цвет. Этот пример является частью [примера новых элементов управления](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_NewControls#3](../../mfc/reference/codesnippet/cpp/cmfccolordialog-class_1.cpp)]

## <a name="requirements"></a>Требования

**Заголовок:** афксколордиалог. h

## <a name="cmfccolordialogcmfccolordialog"></a><a name="cmfccolordialog"></a> Кмфкколордиалог:: Кмфкколордиалог

Формирует объект `CMFCColorDialog`.

```
CMFCColorDialog(
    COLORREF clrInit=0,
    DWORD dwFlags=0,
    CWnd* pParentWnd=NULL,
    HPALETTE hPal=NULL);
```

### <a name="parameters"></a>Параметры

*клринит*<br/>
окне Выбор цвета по умолчанию. Если значение не указано, по умолчанию используется RGB (0, 0, 0) (черный).

*dwFlags*<br/>
[in] Зарезервировано.

*ппарентвнд*<br/>
окне Указатель на родительский узел или окно-владелец диалогового окна.

*хпал*<br/>
окне Маркер цветовой палитры.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfccolordialoggetcolor"></a><a name="getcolor"></a> Кмфкколордиалог:: "Color"

Извлекает цвет, который пользователь выбирает в диалоговом окне выбора цвета.

```
COLORREF GetColor() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение [COLORREF](/windows/win32/gdi/colorref) , содержащее сведения о RGB для цвета, выбранного в диалоговом окне "цвет".

### <a name="remarks"></a>Комментарии

Вызовите эту функцию после вызова `DoModal` метода.

## <a name="cmfccolordialoggetpalette"></a><a name="getpalette"></a> Кмфкколордиалог:: "Palette"

Извлекает цветовую палитру, доступную в диалоговом окне текущий цвет.

```
CPalette* GetPalette() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на `CPalette` объект, указанный в `CMFCColorDialog` конструкторе.

### <a name="remarks"></a>Комментарии

Цветовая палитра определяет цвета, которые может выбрать пользователь.

## <a name="cmfccolordialogrebuildpalette"></a><a name="rebuildpalette"></a> Кмфкколордиалог:: Ребуилдпалетте

Извлекает палитру из системной палитры.

```cpp
void RebuildPalette();
```

## <a name="cmfccolordialogsetcurrentcolor"></a><a name="setcurrentcolor"></a> Кмфкколордиалог:: Сеткуррентколор

Задает текущий цвет диалогового окна.

```cpp
void SetCurrentColor(COLORREF rgb);
```

### <a name="parameters"></a>Параметры

*цвета*<br/>
окне Значение цвета RGB

### <a name="remarks"></a>Комментарии

## <a name="cmfccolordialogsetnewcolor"></a><a name="setnewcolor"></a> Кмфкколордиалог:: Сетневколор

Задает текущий цвет в наиболее похожем цвете в текущей палитре.

```cpp
void SetNewColor(COLORREF rgb);
```

### <a name="parameters"></a>Параметры

*цвета*<br/>
окне Объект [COLORREF](/windows/win32/gdi/colorref) , задающий цвет RGB.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolordialogsetpageone"></a><a name="setpageone"></a> Кмфкколордиалог:: Сетпажеоне

Явно определяет красный, зеленый и синий компоненты выбранного цвета на первой странице свойств диалогового окна выбора цвета.

```cpp
void SetPageOne(
    BYTE R,
    BYTE G,
    BYTE B);
```

### <a name="parameters"></a>Параметры

*R*<br/>
окне Задает красный компонент значения RGB.

*Модуле*<br/>
окне Задает зеленый компонент значения RGB.

*B*<br/>
окне Указывает синий компонент значения RGB.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolordialogsetpagetwo"></a><a name="setpagetwo"></a> Кмфкколордиалог:: Сетпажетво

Явно указывает красный, зеленый и синий компоненты выбранного цвета на второй странице свойств диалогового окна выбора цвета.

```cpp
void SetPageTwo(
    BYTE R,
    BYTE G,
    BYTE B);
```

### <a name="parameters"></a>Параметры

*R*<br/>
окне Задает красный компонент значения RGB

*Модуле*<br/>
окне Задает зеленый компонент значения RGB

*B*<br/>
окне Задает синий компонент значения RGB

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкколорпиккерктрл](../../mfc/reference/cmfccolorpickerctrl-class.md)
