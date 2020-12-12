---
description: 'Дополнительные сведения о: Кмфкколорменубуттон Class'
title: Класс Кмфкколорменубуттон
ms.date: 11/04/2016
f1_keywords:
- CMFCColorMenuButton
- AFXCOLORMENUBUTTON/CMFCColorMenuButton
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::CMFCColorMenuButton
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::EnableAutomaticButton
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::EnableDocumentColors
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::EnableOtherButton
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::EnableTearOff
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::GetAutomaticColor
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::GetColor
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::GetColorByCmdID
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::OnChangeParentWnd
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::OpenColorDialog
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::SetColor
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::SetColorByCmdID
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::SetColorName
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::SetColumnsNumber
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::CopyFrom
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::CreatePopupMenu
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::IsEmptyMenuAllowed
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::OnDraw
- AFXCOLORMENUBUTTON/CMFCColorMenuButton::OnDrawOnCustomizeList
helpviewer_keywords:
- CMFCColorMenuButton [MFC], CMFCColorMenuButton
- CMFCColorMenuButton [MFC], EnableAutomaticButton
- CMFCColorMenuButton [MFC], EnableDocumentColors
- CMFCColorMenuButton [MFC], EnableOtherButton
- CMFCColorMenuButton [MFC], EnableTearOff
- CMFCColorMenuButton [MFC], GetAutomaticColor
- CMFCColorMenuButton [MFC], GetColor
- CMFCColorMenuButton [MFC], GetColorByCmdID
- CMFCColorMenuButton [MFC], OnChangeParentWnd
- CMFCColorMenuButton [MFC], OpenColorDialog
- CMFCColorMenuButton [MFC], SetColor
- CMFCColorMenuButton [MFC], SetColorByCmdID
- CMFCColorMenuButton [MFC], SetColorName
- CMFCColorMenuButton [MFC], SetColumnsNumber
- CMFCColorMenuButton [MFC], CopyFrom
- CMFCColorMenuButton [MFC], CreatePopupMenu
- CMFCColorMenuButton [MFC], IsEmptyMenuAllowed
- CMFCColorMenuButton [MFC], OnDraw
- CMFCColorMenuButton [MFC], OnDrawOnCustomizeList
ms.assetid: 42685704-e994-4f7b-9553-62283c27b754
ms.openlocfilehash: 4ba0934e872adc4e4b33c2ae5700ecb0fc46e6d8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327668"
---
# <a name="cmfccolormenubutton-class"></a>Класс Кмфкколорменубуттон

`CMFCColorMenuButton`Класс поддерживает команду меню или кнопку на панели инструментов, которая запускает диалоговое окно выбора цвета.

## <a name="syntax"></a>Синтаксис

```
class CMFCColorMenuButton : public CMFCToolBarMenuButton
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкколорменубуттон:: Кмфкколорменубуттон](#cmfccolormenubutton)|Формирует объект `CMFCColorMenuButton`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкколорменубуттон:: Енаблеаутоматикбуттон](#enableautomaticbutton)|Включает и отключает кнопку "автоматически", расположенную над обычными кнопками цвета. (Стандартная системная автоматическая кнопка помечена как **Автоматическая**.)|
|[Кмфкколорменубуттон:: Енабледокументколорс](#enabledocumentcolors)|Включает отображение цветов, относящихся к документу, а не системных цветов.|
|[Кмфкколорменубуттон:: Енаблеосербуттон](#enableotherbutton)|Включает и отключает кнопку "другое", расположенную под обычными кнопками цвета. (Стандартная системная кнопка "Other" помечена **дополнительными цветами**.)|
|[Кмфкколорменубуттон:: Енаблетеарофф](#enabletearoff)|Позволяет прервать цветовую панель.|
|[Кмфкколорменубуттон:: Жетаутоматикколор](#getautomaticcolor)|Извлекает текущий автоматический цвет.|
|[Кмфкколорменубуттон:: "Color"](#getcolor)|Извлекает цвет текущей кнопки.|
|[Кмфкколорменубуттон:: Жетколорбикмдид](#getcolorbycmdid)|Возвращает цвет, соответствующий указанному ИДЕНТИФИКАТОРу команды.|
|[Кмфкколорменубуттон:: Ончанжепарентвнд](#onchangeparentwnd)|Вызывается структурой при изменении родительского окна.|
|[Кмфкколорменубуттон:: Опенколордиалог](#opencolordialog)|Открывает диалоговое окно выбора цвета.|
|[Кмфкколорменубуттон:: Сетколор](#setcolor)|Задает цвет кнопки текущего цвета.|
|[Кмфкколорменубуттон:: Сетколорбикмдид](#setcolorbycmdid)|Задает цвет для кнопки меню указанного цвета.|
|[Кмфкколорменубуттон:: Сетколорнаме](#setcolorname)|Задает новое имя для указанного цвета.|
|[Кмфкколорменубуттон:: Сетколумнснумбер](#setcolumnsnumber)|Задает количество столбцов, отображаемых `CMFCColorBar` объектом.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Кмфкколорменубуттон:: CopyFrom](#copyfrom)|Копирует другую кнопку панели инструментов на текущую кнопку.|
|[Кмфкколорменубуттон:: Креатепопупмену](#createpopupmenu)|Создает диалоговое окно «Палитра цветов».|
|[Кмфкколорменубуттон:: Исемптименуалловед](#isemptymenuallowed)|Указывает, поддерживаются ли пустые меню.|
|[Кмфкколорменубуттон:: OnDraw](#ondraw)|Вызывается платформой для вывода изображения на кнопку.|
|[Кмфкколорменубуттон:: Ондравонкустомизелист](#ondrawoncustomizelist)|Вызывается структурой перед `CMFCColorMenuButton` отображением объекта в списке диалогового окна настройки панели инструментов.|

## <a name="remarks"></a>Комментарии

Чтобы заменить исходную команду меню или кнопку панели инструментов на `CMFCColorMenuButton` объект, создайте `CMFCColorMenuButton` объект, задайте соответствующие стили [класса кмфкколорбар](../../mfc/reference/cmfccolorbar-class.md) , а затем вызовите `ReplaceButton` метод класса [класса CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md) . При настройке панели инструментов вызовите метод [кмфктулбарскустомизедиалог:: реплацебуттон](../../mfc/reference/cmfctoolbarscustomizedialog-class.md#replacebutton) .

Диалоговое окно Палитра цветов создается во время обработки обработчика событий [кмфкколорменубуттон:: креатепопупмену](#createpopupmenu) . Обработчик событий уведомляет родительский фрейм с WM_COMMAND сообщением. `CMFCColorMenuButton`Объект ОТПРАВЛЯЕТ идентификатор элемента управления, назначенный исходной команде меню или кнопке панели инструментов.

## <a name="example"></a>Пример

В следующем примере показано, как создать и настроить кнопку меню цвета с помощью различных методов в `CMFCColorMenuButton` классе. В этом примере `CPalette` сначала создается объект, который затем используется для создания объекта `CMFCColorMenuButton` класса. `CMFCColorMenuButton`Затем объект настраивается путем включения автоматических и других кнопок, а также для задания его цвета и количества столбцов. Этот код является частью [примера Word Pad](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_WordPad#5](../../mfc/reference/codesnippet/cpp/cmfccolormenubutton-class_1.h)]
[!code-cpp[NVC_MFC_WordPad#6](../../mfc/reference/codesnippet/cpp/cmfccolormenubutton-class_2.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCToolBarButton](../../mfc/reference/cmfctoolbarbutton-class.md)

[CMFCToolBarMenuButton](../../mfc/reference/cmfctoolbarmenubutton-class.md)

[CMFCColorMenuButton](../../mfc/reference/cmfccolormenubutton-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксколорменубуттон. h

## <a name="cmfccolormenubuttoncmfccolormenubutton"></a><a name="cmfccolormenubutton"></a> Кмфкколорменубуттон:: Кмфкколорменубуттон

Формирует объект `CMFCColorMenuButton`.

```
CMFCColorMenuButton();

CMFCColorMenuButton(
    UINT uiCmdID,
    LPCTSTR lpszText,
    CPalette* pPalette=NULL);
```

### <a name="parameters"></a>Параметры

*уикмдид*<br/>
окне Идентификатор команды кнопки.

*lpszText*<br/>
окне Текст кнопки.

*ппалетте*<br/>
окне Указатель на цветовую палитру кнопки.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Первый конструктор является конструктором по умолчанию. Текущий цвет и автоматический цвет объекта инициализируются черным (RGB (0, 0, 0)).

Второй конструктор инициализирует кнопку до цвета, соответствующего указанному ИДЕНТИФИКАТОРу команды.

## <a name="cmfccolormenubuttoncopyfrom"></a><a name="copyfrom"></a> Кмфкколорменубуттон:: CopyFrom

Копирует один производный от [класса кмфктулбарменубуттон](../../mfc/reference/cmfctoolbarmenubutton-class.md)объект в другой.

```
virtual void CopyFrom(const CMFCToolBarButton& src);
```

### <a name="parameters"></a>Параметры

*src*<br/>
окне Кнопка источника для копирования.

### <a name="remarks"></a>Комментарии

Переопределите этот метод, чтобы скопировать объекты, производные от `CMFCColorMenuButton` объекта.

## <a name="cmfccolormenubuttoncreatepopupmenu"></a><a name="createpopupmenu"></a> Кмфкколорменубуттон:: Креатепопупмену

Создает диалоговое окно «Палитра цветов».

```
virtual CMFCPopupMenu* CreatePopupMenu();
```

### <a name="return-value"></a>Возвращаемое значение

Объект, представляющий диалоговое окно «Палитра цветов».

### <a name="remarks"></a>Комментарии

Этот метод вызывается платформой, когда пользователь нажимает кнопку меню цвета.

## <a name="cmfccolormenubuttonenableautomaticbutton"></a><a name="enableautomaticbutton"></a> Кмфкколорменубуттон:: Енаблеаутоматикбуттон

Включает и отключает кнопку "автоматически", расположенную над обычными кнопками цвета. (Стандартная системная автоматическая кнопка помечена как **Автоматическая**.)

```cpp
void EnableAutomaticButton(
    LPCTSTR lpszLabel,
    COLORREF colorAutomatic,
    BOOL bEnable=TRUE);
```

### <a name="parameters"></a>Параметры

*лпсзлабел*<br/>
окне Указывает текст кнопки, который отображается, когда кнопка становится автоматическим.

*колораутоматик*<br/>
окне Задает новый автоматический цвет.

*bEnable*<br/>
окне Указывает, является ли кнопка автоматической.

### <a name="remarks"></a>Комментарии

Кнопка автоматически применяет текущий цвет по умолчанию.

## <a name="cmfccolormenubuttonenabledocumentcolors"></a><a name="enabledocumentcolors"></a> Кмфкколорменубуттон:: Енабледокументколорс

Включает отображение цветов, относящихся к документу, а не системных цветов.

```cpp
void EnableDocumentColors(
    LPCTSTR lpszLabel,
    BOOL bEnable=TRUE);
```

### <a name="parameters"></a>Параметры

*лпсзлабел*<br/>
окне Указывает текст кнопки.

*bEnable*<br/>
окне Значение TRUE, чтобы отображать цвета, относящиеся к документу, или значение FALSE для вывода системных цветов.

### <a name="remarks"></a>Комментарии

Этот метод используется для вывода цветов текущего документа или цветов системной палитры при нажатии пользователем кнопки меню цвета.

## <a name="cmfccolormenubuttonenableotherbutton"></a><a name="enableotherbutton"></a> Кмфкколорменубуттон:: Енаблеосербуттон

Включает и отключает кнопку "другое", расположенную под обычными кнопками цвета. (Стандартная системная кнопка "Other" помечена **дополнительными цветами**.)

```cpp
void EnableOtherButton(
    LPCTSTR lpszLabel,
    BOOL bAltColorDlg=TRUE,
    BOOL bEnable=TRUE);
```

### <a name="parameters"></a>Параметры

*лпсзлабел*<br/>
окне Указывает текст кнопки.

*балтколордлг*<br/>
окне Укажите значение TRUE, чтобы отобразить `CMFCColorDialog` диалоговое окно, или false для вывода диалогового окна стандартный системный цвет.

*bEnable*<br/>
окне Укажите значение TRUE, чтобы отобразить кнопку "другое". в противном случае — значение FALSE. Значение по умолчанию — TRUE.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolormenubuttonenabletearoff"></a><a name="enabletearoff"></a> Кмфкколорменубуттон:: Енаблетеарофф

Позволяет прервать цветовую панель.

```cpp
void EnableTearOff(
    UINT uiID,
    int nVertDockColumns=-1,
    int nHorzDockRows=-1);
```

### <a name="parameters"></a>Параметры

*uiID*<br/>
окне Указывает идентификатор для области разрыва.

*нвертдоккколумнс*<br/>
окне Указывает число столбцов в области вертикально закрепленного цвета в состоянии разрыва.

*нхорздоккровс*<br/>
окне Указывает число строк для горизонтально закрепленного цвета панели, находясь в состоянии разрыва.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы включить функцию отрыва для цветовой панели, которая появляется при `CMFCColorMenuButton` нажатии кнопки.

## <a name="cmfccolormenubuttongetautomaticcolor"></a><a name="getautomaticcolor"></a> Кмфкколорменубуттон:: Жетаутоматикколор

Извлекает текущий автоматический цвет.

```
COLORREF GetAutomaticColor() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение цвета RGB, представляющее текущий автоматический цвет.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы получить автоматический цвет, заданный [кмфкколорменубуттон:: енаблеаутоматикбуттон](#enableautomaticbutton).

## <a name="cmfccolormenubuttongetcolor"></a><a name="getcolor"></a> Кмфкколорменубуттон:: "Color"

Извлекает цвет текущей кнопки.

```
COLORREF GetColor() const;
```

### <a name="return-value"></a>Возвращаемое значение

Цвет кнопки.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolormenubuttongetcolorbycmdid"></a><a name="getcolorbycmdid"></a> Кмфкколорменубуттон:: Жетколорбикмдид

Возвращает цвет, соответствующий указанному ИДЕНТИФИКАТОРу команды.

```
static COLORREF GetColorByCmdID(UINT uiCmdID);
```

### <a name="parameters"></a>Параметры

*уикмдид*<br/>
окне Идентификатор команды.

### <a name="return-value"></a>Возвращаемое значение

Цвет, соответствующий указанному ИДЕНТИФИКАТОРу команды.

### <a name="remarks"></a>Комментарии

Используйте этот метод при наличии нескольких кнопок цвета в приложении. Когда пользователь нажимает кнопку цвета, кнопка отправляет идентификатор своей команды в WM_COMMAND сообщение родительскому элементу. `GetColorByCmdID`Метод использует идентификатор команды для получения соответствующего цвета.

## <a name="cmfccolormenubuttonisemptymenuallowed"></a><a name="isemptymenuallowed"></a> Кмфкколорменубуттон:: Исемптименуалловед

Указывает, поддерживаются ли пустые меню.

```
virtual BOOL IsEmptyMenuAllowed() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если пустые меню разрешены; в противном случае — нуль.

### <a name="remarks"></a>Комментарии

По умолчанию поддерживаются пустые меню. Переопределите этот метод, чтобы изменить это поведение в производном классе.

## <a name="cmfccolormenubuttononchangeparentwnd"></a><a name="onchangeparentwnd"></a> Кмфкколорменубуттон:: Ончанжепарентвнд

Вызывается структурой при изменении родительского окна.

```
virtual void OnChangeParentWnd(CWnd* pWndParent);
```

### <a name="parameters"></a>Параметры

*пвндпарент*<br/>
окне Указатель на новое родительское окно.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolormenubuttonondraw"></a><a name="ondraw"></a> Кмфкколорменубуттон:: OnDraw

Вызывается платформой для вывода изображения на кнопку.

```
virtual void OnDraw(
    CDC* pDC,
    const CRect& rect,
    CMFCToolBarImages* pImages,
    BOOL bHorz=TRUE,
    BOOL bCustomizeMode=FALSE,
    BOOL bHighlight=FALSE,
    BOOL bDrawBorder=TRUE,
    BOOL bGrayDisabledButtons=TRUE);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*rect*<br/>
окне Прямоугольник, ограничивающий перерисовку области.

*пимажес*<br/>
окне Указывает на список изображений панели инструментов.

*бхорз*<br/>
окне Значение TRUE, чтобы указать, что панель инструментов находится в закрепленном состоянии по горизонтали; в противном случае — значение FALSE. Значение по умолчанию — TRUE.

*бкустомиземоде*<br/>
окне Значение TRUE, чтобы указать, что приложение находится в режиме настройки; в противном случае — значение FALSE. Значение по умолчанию — FALSE.

*бхигхлигхт*<br/>
окне Значение TRUE, чтобы указать, что кнопка будет выделена; в противном случае — значение FALSE. Значение по умолчанию — FALSE.

*бдравбордер*<br/>
окне Значение TRUE, чтобы указать, что граница кнопки отображается; в противном случае — значение FALSE. Значение по умолчанию — TRUE.

*бграйдисабледбуттонс*<br/>
окне Значение TRUE указывает, что отключенные кнопки являются неактивными (затемнены). в противном случае — значение FALSE. Значение по умолчанию — TRUE.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolormenubuttonondrawoncustomizelist"></a><a name="ondrawoncustomizelist"></a> Кмфкколорменубуттон:: Ондравонкустомизелист

Вызывается структурой перед `CMFCColorMenuButton` отображением объекта в списке диалогового окна настройки панели инструментов.

```
virtual int OnDrawOnCustomizeList(
    CDC* pDC,
    const CRect& rect,
    BOOL bSelected);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*rect*<br/>
окне Прямоугольник, ограничивающий рисуемую кнопку.

*бселектед*<br/>
окне Значение TRUE указывает, что кнопка находится в выбранном состоянии; в противном случае — значение FALSE.

### <a name="return-value"></a>Возвращаемое значение

Ширина кнопки.

### <a name="remarks"></a>Комментарии

Этот метод вызывается платформой при `CMFCColorMenuButton` отображении объекта в списке во время процесса настройки панели инструментов.

## <a name="cmfccolormenubuttonopencolordialog"></a><a name="opencolordialog"></a> Кмфкколорменубуттон:: Опенколордиалог

Открывает диалоговое окно выбора цвета.

```
virtual BOOL OpenColorDialog(
    const COLORREF colorDefault,
    COLORREF& colorRes);
```

### <a name="parameters"></a>Параметры

*колордефаулт*<br/>
окне Цвет по умолчанию, выбранный в диалоговом окне «цвет».

*колоррес*<br/>
заполняет Возвращает цвет, который пользователь выбирает в диалоговом окне «цвет».

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если пользователь выбирает новый цвет; в противном случае — нуль.

### <a name="remarks"></a>Комментарии

При нажатии кнопки меню вызовите этот метод, чтобы открыть диалоговое окно "цвет". Если возвращаемое значение не равно нулю, то цвет, выбираемый пользователем, сохраняется в параметре *колоррес* . Используйте метод [кмфкколорменубуттон:: енаблеосербуттон](#enableotherbutton) , чтобы переключаться между диалоговым окном Стандартный цвет и диалоговым окном [класс кмфкколордиалог](../../mfc/reference/cmfccolordialog-class.md) .

## <a name="cmfccolormenubuttonsetcolor"></a><a name="setcolor"></a> Кмфкколорменубуттон:: Сетколор

Задает цвет кнопки текущего цвета.

```
virtual void SetColor(
    COLORREF clr,
    BOOL bNotify=TRUE);
```

### <a name="parameters"></a>Параметры

*среду*<br/>
окне Значение цвета RGB.

*бнотифи*<br/>
окне Значение TRUE, чтобы применить цвет параметра *среды CLR* ко всем связанным кнопкам меню или кнопке панели инструментов; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы изменить цвет кнопки текущего цвета. Если значение параметра *бнотифи* не равно нулю, то цвет соответствующей кнопки во всех связанных всплывающих меню или на панели инструментов изменится на цвет, заданный параметром *CLR* .

## <a name="cmfccolormenubuttonsetcolorbycmdid"></a><a name="setcolorbycmdid"></a> Кмфкколорменубуттон:: Сетколорбикмдид

Задает цвет для кнопки меню указанного цвета.

```
static void SetColorByCmdID(
    UINT uiCmdID,
    COLORREF color);
```

### <a name="parameters"></a>Параметры

*уикмдид*<br/>
окне Идентификатор ресурса для кнопки меню цвета.

*color*<br/>
окне Значение цвета RGB.

## <a name="cmfccolormenubuttonsetcolorname"></a><a name="setcolorname"></a> Кмфкколорменубуттон:: Сетколорнаме

Задает новое имя для указанного цвета.

```
static void SetColorName(
    COLORREF color,
    const CString& strName);
```

### <a name="parameters"></a>Параметры

*color*<br/>
окне Значение RGB цвета, имя которого изменяется.

*strName*<br/>
окне Новое имя цвета.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolormenubuttonsetcolumnsnumber"></a><a name="setcolumnsnumber"></a> Кмфкколорменубуттон:: Сетколумнснумбер

Задает число столбцов, отображаемых в элементе управления выбора цвета (объект [кмфкколорбар](../../mfc/reference/cmfccolorbar-class.md) ).

```cpp
void SetColumnsNumber(int nColumns);
```

### <a name="parameters"></a>Параметры

*nColumns*<br/>
окне Число отображаемых столбцов.

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкколорбар](../../mfc/reference/cmfccolorbar-class.md)<br/>
[Класс CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md)<br/>
[Класс Кмфктулбарскустомизедиалог](../../mfc/reference/cmfctoolbarscustomizedialog-class.md)<br/>
[Класс Кмфкколорбуттон](../../mfc/reference/cmfccolorbutton-class.md)
