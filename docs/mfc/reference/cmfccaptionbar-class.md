---
description: 'Дополнительные сведения о: CMFCCaptionBar Class'
title: Класс CMFCCaptionBar
ms.date: 11/04/2016
f1_keywords:
- CMFCCaptionBar
- AFXCAPTIONBAR/CMFCCaptionBar
- AFXCAPTIONBAR/CMFCCaptionBar::Create
- AFXCAPTIONBAR/CMFCCaptionBar::DoesAllowDynInsertBefore
- AFXCAPTIONBAR/CMFCCaptionBar::EnableButton
- AFXCAPTIONBAR/CMFCCaptionBar::GetAlignment
- AFXCAPTIONBAR/CMFCCaptionBar::GetBorderSize
- AFXCAPTIONBAR/CMFCCaptionBar::GetButtonRect
- AFXCAPTIONBAR/CMFCCaptionBar::GetMargin
- AFXCAPTIONBAR/CMFCCaptionBar::IsMessageBarMode
- AFXCAPTIONBAR/CMFCCaptionBar::RemoveBitmap
- AFXCAPTIONBAR/CMFCCaptionBar::RemoveButton
- AFXCAPTIONBAR/CMFCCaptionBar::RemoveIcon
- AFXCAPTIONBAR/CMFCCaptionBar::RemoveText
- AFXCAPTIONBAR/CMFCCaptionBar::SetBitmap
- AFXCAPTIONBAR/CMFCCaptionBar::SetBorderSize
- AFXCAPTIONBAR/CMFCCaptionBar::SetButton
- AFXCAPTIONBAR/CMFCCaptionBar::SetButtonPressed
- AFXCAPTIONBAR/CMFCCaptionBar::SetButtonToolTip
- AFXCAPTIONBAR/CMFCCaptionBar::SetFlatBorder
- AFXCAPTIONBAR/CMFCCaptionBar::SetIcon
- AFXCAPTIONBAR/CMFCCaptionBar::SetImageToolTip
- AFXCAPTIONBAR/CMFCCaptionBar::SetMargin
- AFXCAPTIONBAR/CMFCCaptionBar::SetText
- AFXCAPTIONBAR/CMFCCaptionBar::OnDrawBackground
- AFXCAPTIONBAR/CMFCCaptionBar::OnDrawBorder
- AFXCAPTIONBAR/CMFCCaptionBar::OnDrawButton
- AFXCAPTIONBAR/CMFCCaptionBar::OnDrawImage
- AFXCAPTIONBAR/CMFCCaptionBar::OnDrawText
- AFXCAPTIONBAR/CMFCCaptionBar::m_clrBarBackground
- AFXCAPTIONBAR/CMFCCaptionBar::m_clrBarBorder
- AFXCAPTIONBAR/CMFCCaptionBar::m_clrBarText
helpviewer_keywords:
- CMFCCaptionBar [MFC], Create
- CMFCCaptionBar [MFC], DoesAllowDynInsertBefore
- CMFCCaptionBar [MFC], EnableButton
- CMFCCaptionBar [MFC], GetAlignment
- CMFCCaptionBar [MFC], GetBorderSize
- CMFCCaptionBar [MFC], GetButtonRect
- CMFCCaptionBar [MFC], GetMargin
- CMFCCaptionBar [MFC], IsMessageBarMode
- CMFCCaptionBar [MFC], RemoveBitmap
- CMFCCaptionBar [MFC], RemoveButton
- CMFCCaptionBar [MFC], RemoveIcon
- CMFCCaptionBar [MFC], RemoveText
- CMFCCaptionBar [MFC], SetBitmap
- CMFCCaptionBar [MFC], SetBorderSize
- CMFCCaptionBar [MFC], SetButton
- CMFCCaptionBar [MFC], SetButtonPressed
- CMFCCaptionBar [MFC], SetButtonToolTip
- CMFCCaptionBar [MFC], SetFlatBorder
- CMFCCaptionBar [MFC], SetIcon
- CMFCCaptionBar [MFC], SetImageToolTip
- CMFCCaptionBar [MFC], SetMargin
- CMFCCaptionBar [MFC], SetText
- CMFCCaptionBar [MFC], OnDrawBackground
- CMFCCaptionBar [MFC], OnDrawBorder
- CMFCCaptionBar [MFC], OnDrawButton
- CMFCCaptionBar [MFC], OnDrawImage
- CMFCCaptionBar [MFC], OnDrawText
- CMFCCaptionBar [MFC], m_clrBarBackground
- CMFCCaptionBar [MFC], m_clrBarBorder
- CMFCCaptionBar [MFC], m_clrBarText
ms.assetid: acb54d5f-14ff-4c96-aeb3-7717cf566d9a
ms.openlocfilehash: a5dd5f968c52268935b6176115e8723a9d82e8a1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327743"
---
# <a name="cmfccaptionbar-class"></a>Класс CMFCCaptionBar

`CMFCCaptionBar`Объект — это панель элементов управления, которая может отображать три элемента: кнопку, метку текста и точечный рисунок. Она может содержать только один элемент каждого типа одновременно. Можно выровнять каждый элемент по левому или правому краю элемента управления или по центру. Также можно применить плоский или трехмерный стиль к верхним и нижним границам заголовка окна.

## <a name="syntax"></a>Синтаксис

```
class CMFCCaptionBar : public CPane
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCCaptionBar:: Create](#create)|Создает элемент управления "заголовок заголовка" и прикрепляет его к `CMFCCaptionBar` объекту.|
|[CMFCCaptionBar::DoesAllowDynInsertBefore](#doesallowdyninsertbefore)|Указывает, можно ли динамически вставлять другую панель между заголовком и ее родительским фреймом. (Переопределяет [CBasePane::D оесалловдининсертбефоре](../../mfc/reference/cbasepane-class.md#doesallowdyninsertbefore).)|
|[CMFCCaptionBar:: Енаблебуттон](#enablebutton)|Включает или отключает кнопку в строке заголовка.|
|[CMFCCaptionBar:: Alignment](#getalignment)|Возвращает выравнивание указанного элемента.|
|[CMFCCaptionBar:: Жетбордерсизе](#getbordersize)|Возвращает размер границы заголовка.|
|[CMFCCaptionBar:: Жетбуттонрект](#getbuttonrect)|Извлекает ограничивающий прямоугольник кнопки в строке заголовка.|
|[CMFCCaptionBar:: Margin](#getmargin)|Возвращает расстояние между границей элементов строки заголовка и границей элемента управления "заголовок".|
|[CMFCCaptionBar:: Исмессажебармоде](#ismessagebarmode)|Указывает, находится ли строка заголовка в режиме панели сообщений.|
|[CMFCCaptionBar:: Ремовебитмап](#removebitmap)|Удаляет растровое изображение из строки заголовка.|
|[CMFCCaptionBar:: Ремовебуттон](#removebutton)|Удаляет кнопку из строки заголовка.|
|[CMFCCaptionBar:: Ремовеикон](#removeicon)|Удаляет значок из строки заголовка.|
|[CMFCCaptionBar:: Ремоветекст](#removetext)|Удаляет текстовую метку из строки заголовка.|
|[CMFCCaptionBar:: Сетбитмап](#setbitmap)|Задает точечный рисунок для заголовка.|
|[CMFCCaptionBar:: Сетбордерсизе](#setbordersize)|Задает размер границы заголовка.|
|[CMFCCaptionBar:: Сетбуттон](#setbutton)|Задает кнопку для строки заголовка.|
|[CMFCCaptionBar:: Сетбуттонпрессед](#setbuttonpressed)|Указывает, оставалась ли нажата кнопка.|
|[CMFCCaptionBar:: Сетбуттонтултип](#setbuttontooltip)|Задает подсказку для кнопки.|
|[CMFCCaptionBar:: Сетфлатбордер](#setflatborder)|Задает стиль границы заголовка.|
|[CMFCCaptionBar:: Сетикон](#seticon)|Задает значок для строки заголовка.|
|[CMFCCaptionBar:: Сетимажетултип](#setimagetooltip)|Задает подсказку для изображения в строке заголовка.|
|[CMFCCaptionBar:: Сетмаргин](#setmargin)|Задает расстояние между границей элемента заголовка и границей элемента управления "заголовок".|
|[CMFCCaptionBar:: SetText](#settext)|Задает текстовую метку для строки заголовка.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[CMFCCaptionBar:: Ондравбаккграунд](#ondrawbackground)|Вызывается платформой для заполнения фона строки заголовка.|
|[CMFCCaptionBar:: Ондравбордер](#ondrawborder)|Вызывается платформой для отрисовки границы заголовка.|
|[CMFCCaptionBar:: Ондравбуттон](#ondrawbutton)|Вызывается структурой для рисования кнопки строки заголовка.|
|[CMFCCaptionBar:: Ондравимаже](#ondrawimage)|Вызывается структурой для отрисовки изображения в строке заголовка.|
|[CMFCCaptionBar:: Ондравтекст](#ondrawtext)|Вызывается платформой для рисования текста строки заголовка.|

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|[CMFCCaptionBar:: m_clrBarBackground](#m_clrbarbackground)|Цвет фона строки заголовка.|
|[CMFCCaptionBar:: m_clrBarBorder](#m_clrbarborder)|Цвет границы заголовка.|
|[CMFCCaptionBar:: m_clrBarText](#m_clrbartext)|Цвет текста заголовка.|

## <a name="remarks"></a>Комментарии

Чтобы создать заголовок, выполните следующие действия.

1. Создайте `CMFCCaptionBar` объект. Как правило, строка заголовка добавляется в класс окна фрейма.

1. Вызовите метод [CMFCCaptionBar:: Create](#create) , чтобы создать элемент управления "заголовок заголовка" и присоединить его к `CMFCCaptionBar` объекту.

1. Вызовите [CMFCCaptionBar:: сетбуттон](#setbutton), [CMFCCaptionBar:: SetText](#settext), [CMFCCaptionBar:: Сетикон](#seticon)и [CMFCCaptionBar:: сетбитмап](#setbitmap) , чтобы задать элементы строки заголовка.

При задании элемента Button необходимо назначить кнопке идентификатор команды. Когда пользователь нажимает кнопку, строка заголовка направляет WM_COMMAND сообщения с этим ИДЕНТИФИКАТОРом в родительское окно фрейма.

Панель заголовка может также работать в режиме панели сообщений, который эмулирует панель сообщений, отображаемую в Microsoft Office приложениях 2007. В режиме панели сообщений в строке заголовка отображается точечный рисунок, сообщение и кнопка (обычно открывается диалоговое окно). К точечному рисунку можно назначить подсказку.

Чтобы включить режим панели сообщений, вызовите метод [CMFCCaptionBar:: Create](#create) и установите для четвертого параметра (бисмессажебармоде) значение true.

## <a name="example"></a>Пример

В приведенном ниже примере демонстрируется использование различных методов класса `CMFCCaptionBar` . В этом примере показано, как создать элемент управления "заголовок заголовка", задать трехмерную границу строки заголовка, задать расстояние в пикселях между границей элементов строки заголовка и краем элемента управления "заголовок заголовка", установить кнопку для строки заголовка, задать всплывающую подсказку для кнопки, задать текстовую метку для строки заголовка, установить точечный рисунок и задайте подсказку для изображения в строке заголовка. Этот фрагмент кода является частью [демонстрационного примера MS Office 2007](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_MSOffice2007Demo#1](../../mfc/reference/codesnippet/cpp/cmfccaptionbar-class_1.h)]
[!code-cpp[NVC_MFC_MSOffice2007Demo#2](../../mfc/reference/codesnippet/cpp/cmfccaptionbar-class_2.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CBasePane](../../mfc/reference/cbasepane-class.md)

[CPane](../../mfc/reference/cpane-class.md)

[CMFCCaptionBar](../../mfc/reference/cmfccaptionbar-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкскаптионбар. h

## <a name="cmfccaptionbarcreate"></a><a name="create"></a> CMFCCaptionBar:: Create

Создает элемент управления "заголовок заголовка" и прикрепляет его к `CMFCCaptionBar` объекту.

```
BOOL Create(
    DWORD dwStyle,
    CWnd* pParentWnd,
    UINT uID,
    int nHeight=-1,
    BOOL bIsMessageBarMode=FALSE);
```

### <a name="parameters"></a>Параметры

*двстиле*<br/>
Логическое или сочетание стилей заголовков.

*ппарентвнд*<br/>
Родительское окно элемента управления "заголовок" заголовка.

*Такой*<br/>
Идентификатор элемента управления "заголовок" заголовка.

*нхеигхт*<br/>
Высота элемента управления "заголовок" в пикселях. Если значение равно-1, то высота вычисляется в соответствии с высотой значка, текстом и кнопкой, отображаемой в элементе управления "заголовок" заголовка.

*бисмессажебармоде*<br/>
Значение TRUE, если строка заголовка находится в режиме панели сообщений; В противном случае — значение FALSE.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если элемент управления "заголовок заголовка" успешно создан; В противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

`CMFCCaptionBar`Объект создается в два этапа. Сначала вызывается конструктор, а затем вызывается `Create` метод, который создает элемент управления Windows и прикрепляет его к `CMFCCaptionBar` объекту.

## <a name="cmfccaptionbardoesallowdyninsertbefore"></a><a name="doesallowdyninsertbefore"></a> CMFCCaptionBar::D Оесалловдининсертбефоре

Указывает, можно ли динамически вставлять другую панель между заголовком и ее родительским фреймом.

```
virtual BOOL DoesAllowDynInsertBefore() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение FALSE, если не переопределено.

### <a name="remarks"></a>Комментарии

## <a name="cmfccaptionbarenablebutton"></a><a name="enablebutton"></a> CMFCCaptionBar:: Енаблебуттон

Включает или отключает кнопку в строке заголовка.

```cpp
void EnableButton(BOOL bEnable=TRUE);
```

### <a name="parameters"></a>Параметры

*bEnable*<br/>
окне Значение TRUE, чтобы включить кнопку; значение FALSE, чтобы отключить кнопку.

## <a name="cmfccaptionbargetalignment"></a><a name="getalignment"></a> CMFCCaptionBar:: Alignment

Возвращает выравнивание указанного элемента.

```
BarElementAlignment GetAlignment(BarElement elem);
```

### <a name="parameters"></a>Параметры

*Elem*<br/>
окне Элемент заголовка заголовка, для которого необходимо получить выравнивание.

### <a name="return-value"></a>Возвращаемое значение

Выравнивание элемента, например кнопки, точечного рисунка, текста или значка.

### <a name="remarks"></a>Комментарии

Выравнивание элемента может иметь одно из следующих значений:

- ALIGN_INVALID

- ALIGN_LEFT

- ALIGN_RIGHT

- ALIGN_CENTER

## <a name="cmfccaptionbargetbordersize"></a><a name="getbordersize"></a> CMFCCaptionBar:: Жетбордерсизе

Возвращает размер границы заголовка.

```
int GetBorderSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Размер границы в пикселях.

## <a name="cmfccaptionbargetbuttonrect"></a><a name="getbuttonrect"></a> CMFCCaptionBar:: Жетбуттонрект

Извлекает ограничивающий прямоугольник кнопки в строке заголовка.

```
CRect GetButtonRect() const;
```

### <a name="return-value"></a>Возвращаемое значение

`CRect`Объект, содержащий координаты ограничивающего прямоугольника кнопки в строке заголовка.

## <a name="cmfccaptionbargetmargin"></a><a name="getmargin"></a> CMFCCaptionBar:: Margin

Возвращает расстояние между границей элементов строки заголовка и границей элемента управления "заголовок".

```
int GetMargin() const;
```

### <a name="return-value"></a>Возвращаемое значение

Расстояние (в пикселях) между границей элементов строки заголовка и границей элемента управления "заголовок".

## <a name="cmfccaptionbarismessagebarmode"></a><a name="ismessagebarmode"></a> CMFCCaptionBar:: Исмессажебармоде

Указывает, находится ли строка заголовка в режиме панели сообщений.

```
BOOL IsMessageBarMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если строка заголовка находится в режиме панели сообщений; В противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

В режиме панели сообщений в строке заголовка отображается изображение с подсказкой, текстом сообщения и кнопкой.

## <a name="cmfccaptionbarm_clrbarbackground"></a><a name="m_clrbarbackground"></a> CMFCCaptionBar:: m_clrBarBackground

Цвет фона строки заголовка.

```
COLORREF m_clrBarBackground
```

## <a name="cmfccaptionbarm_clrbarborder"></a><a name="m_clrbarborder"></a> CMFCCaptionBar:: m_clrBarBorder

Цвет границы заголовка.

```
COLORREF m_clrBarBorder
```

## <a name="cmfccaptionbarm_clrbartext"></a><a name="m_clrbartext"></a> CMFCCaptionBar:: m_clrBarText

Цвет текста заголовка.

```
COLORREF m_clrBarText
```

## <a name="cmfccaptionbarondrawbackground"></a><a name="ondrawbackground"></a> CMFCCaptionBar:: Ондравбаккграунд

Вызывается платформой для заполнения фона строки заголовка.

```
virtual void OnDrawBackground(
    CDC* pDC,
    CRect rect);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства в строке заголовка.

*rect*<br/>
окне Ограничивающий прямоугольник для заполнения.

### <a name="remarks"></a>Комментарии

`OnDrawBackground`Метод вызывается при заполнении фона строки заголовка. Реализация по умолчанию заполняет фон с помощью цвета [CMFCCaptionBar:: m_clrBarBackground](#m_clrbarbackground) .

Переопределите этот метод в `CMFCCaptionBar` производном классе, чтобы настроить внешний вид строки заголовка.

## <a name="cmfccaptionbarondrawborder"></a><a name="ondrawborder"></a> CMFCCaptionBar:: Ондравбордер

Вызывается платформой для отрисовки границы заголовка.

```
virtual void OnDrawBorder(
    CDC* pDC,
    CRect rect);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Контекст устройства, используемый для отображения границ.

*rect*<br/>
окне Ограничивающий прямоугольник.

### <a name="remarks"></a>Комментарии

По умолчанию границы имеют плоский стиль.

Переопределите этот метод в `CMFCCaptionBar` производном классе, чтобы настроить внешний вид границ в строке заголовка.

## <a name="cmfccaptionbarondrawbutton"></a><a name="ondrawbutton"></a> CMFCCaptionBar:: Ондравбуттон

Вызывается структурой для рисования кнопки строки заголовка.

```
virtual void OnDrawButton(
    CDC* pDC,
    CRect rect,
    const CString& strButton,
    BOOL bEnabled);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства, используемый для вывода кнопки.

*rect*<br/>
окне Ограничивающий прямоугольник кнопки.

*стрбуттон*<br/>
окне Текстовая метка кнопки.

*бенаблед*<br/>
окне Значение TRUE, если кнопка включена; В противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Переопределите этот метод в `CMFCCaptionBar` производном классе, чтобы настроить внешний вид кнопки в строке заголовка.

## <a name="cmfccaptionbarondrawimage"></a><a name="ondrawimage"></a> CMFCCaptionBar:: Ондравимаже

Вызывается структурой для отрисовки изображения в строке заголовка.

```
virtual void OnDrawImage(
    CDC* pDC,
    CRect rect);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства, используемый для вывода изображения.

*rect*<br/>
окне Задает ограничивающий прямоугольник изображения.

### <a name="remarks"></a>Комментарии

Переопределите этот метод в `CMFCCaptionBar` производном классе, чтобы настроить внешний вид изображения.

## <a name="cmfccaptionbarondrawtext"></a><a name="ondrawtext"></a> CMFCCaptionBar:: Ондравтекст

Вызывается платформой для рисования текста строки заголовка.

```
virtual void OnDrawText(
    CDC* pDC,
    CRect rect,
    const CString& strText);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства, используемый для вывода кнопки.

*rect*<br/>
окне Ограничивающий прямоугольник текста.

*стртекст*<br/>
окне Отображаемая текстовая строка.

### <a name="remarks"></a>Комментарии

Реализация по умолчанию отображает текст с помощью `CDC::DrawText` и [CMFCCaptionBar:: m_clrBarText](#m_clrbartext) Color.

Переопределите этот метод в `CMFCCaptionBar` производном классе, чтобы настроить внешний вид текста в строке заголовка.

## <a name="cmfccaptionbarremovebitmap"></a><a name="removebitmap"></a> CMFCCaptionBar:: Ремовебитмап

Удаляет растровое изображение из строки заголовка.

```cpp
void RemoveBitmap();
```

## <a name="cmfccaptionbarremovebutton"></a><a name="removebutton"></a> CMFCCaptionBar:: Ремовебуттон

Удаляет кнопку из строки заголовка.

```cpp
void RemoveButton();
```

### <a name="remarks"></a>Комментарии

Макет элементов строки заголовка корректируется автоматически.

## <a name="cmfccaptionbarremoveicon"></a><a name="removeicon"></a> CMFCCaptionBar:: Ремовеикон

Удаляет значок из строки заголовка.

```cpp
void RemoveIcon();
```

## <a name="cmfccaptionbarremovetext"></a><a name="removetext"></a> CMFCCaptionBar:: Ремоветекст

Удаляет текстовую метку из строки заголовка.

```cpp
void RemoveText();
```

## <a name="cmfccaptionbarsetbitmap"></a><a name="setbitmap"></a> CMFCCaptionBar:: Сетбитмап

Задает точечный рисунок для заголовка.

```cpp
void SetBitmap(
    HBITMAP hBitmap,
    COLORREF clrTransparent,
    BOOL bStretch=FALSE,
    BarElementAlignment bmpAlignment=ALIGN_RIGHT);

void SetBitmap(
    UINT uiBmpResID,
    COLORREF clrTransparent,
    BOOL bStretch=FALSE,
    BarElementAlignment bmpAlignment=ALIGN_RIGHT);
```

### <a name="parameters"></a>Параметры

*хбитмап*<br/>
окне Заданный для изображения маркер.

*клртранспарент*<br/>
окне Значение RGB, указывающее прозрачный цвет точечного рисунка.

*бстретч*<br/>
окне Если значение — TRUE, точечный рисунок растягивается, если он не умещается в прямоугольнике, ограничивающем изображение. В противном случае точечный рисунок не растягивается.

*бмпалигнмент*<br/>
окне Выравнивание растрового изображения.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы задать точечный рисунок в строке заголовка.

Предыдущее растровое изображение уничтожается автоматически. Если в строке заголовка отображается значок, так как вы вызвали метод [CMFCCaptionBar:: сетикон](#seticon) , битовая карта не будет отображаться, если не удалить значок путем вызова [CMFCCaptionBar:: ремовеикон](#removeicon).

Битовая карта выстраивается, как указано параметром *бмпалигнмент* .  Этот параметр может принимать одно из следующих значений `BarElementAlignment`:

- ALIGN_INVALID

- ALIGN_LEFT

- ALIGN_RIGHT

- ALIGN_CENTER

## <a name="cmfccaptionbarsetbordersize"></a><a name="setbordersize"></a> CMFCCaptionBar:: Сетбордерсизе

Задает размер границы заголовка.

```cpp
void SetBorderSize(int nSize);
```

### <a name="parameters"></a>Параметры

*нсизе*<br/>
окне Новый размер границы заголовка в пикселях.

## <a name="cmfccaptionbarsetbutton"></a><a name="setbutton"></a> CMFCCaptionBar:: Сетбуттон

Задает кнопку для строки заголовка.

```cpp
void SetButton(
    LPCTSTR lpszLabel,
    UINT uiCmdUI,
    BarElementAlignment btnAlignmnet=ALIGN_LEFT,
    BOOL bHasDropDownArrow=TRUE);
```

### <a name="parameters"></a>Параметры

*лпсзлабел*<br/>
Метка команды кнопки.

*уикмдуи*<br/>
Идентификатор команды кнопки.

*бтналигнмнет*<br/>
Выравнивание кнопки.

*бхасдропдовнарров*<br/>
Значение TRUE, если кнопка отображает стрелку раскрывающегося списка; в противном случае — значение FALSE.

## <a name="cmfccaptionbarsetbuttonpressed"></a><a name="setbuttonpressed"></a> CMFCCaptionBar:: Сетбуттонпрессед

Указывает, оставалась ли нажата кнопка.

```cpp
void SetButtonPressed(BOOL bPresed=TRUE);
```

### <a name="parameters"></a>Параметры

*бпресед*<br/>
Значение TRUE, если кнопка сохраняет нажатое состояние, и FALSE в противном случае.

## <a name="cmfccaptionbarsetbuttontooltip"></a><a name="setbuttontooltip"></a> CMFCCaptionBar:: Сетбуттонтултип

Задает подсказку для кнопки.

```cpp
void SetButtonToolTip(
    LPCTSTR lpszToolTip,
    LPCTSTR lpszDescription=NULL);
```

### <a name="parameters"></a>Параметры

*lpszToolTip*<br/>
окне Заголовок подсказки.

*лпсздескриптион*<br/>
окне Описание подсказки.

## <a name="cmfccaptionbarsetflatborder"></a><a name="setflatborder"></a> CMFCCaptionBar:: Сетфлатбордер

Задает стиль границы заголовка.

```cpp
void SetFlatBorder(BOOL bFlat=TRUE);
```

### <a name="parameters"></a>Параметры

*бфлат*<br/>
окне Значение TRUE, если граница строки заголовка плоская. Значение FALSE, если граница является трехмерной.

## <a name="cmfccaptionbarseticon"></a><a name="seticon"></a> CMFCCaptionBar:: Сетикон

Задает значок для строки заголовка.

```cpp
void SetIcon(
    HICON hIcon,
    BarElementAlignment iconAlignment=ALIGN_RIGHT);
```

### <a name="parameters"></a>Параметры

*hIcon*<br/>
окне Описатель для задания значка.

*иконалигнмент*<br/>
окне Выравнивание значка.

### <a name="remarks"></a>Комментарии

В панелях заголовка могут отображаться значки или растровые изображения. Сведения о том, как отобразить точечный рисунок, см. в разделе [CMFCCaptionBar:: сетбитмап](#setbitmap) . Если заданы как значок, так и точечный рисунок, значок всегда отображается. Вызовите [CMFCCaptionBar:: ремовеикон](#removeicon) , чтобы удалить значок из строки заголовка.

Значок выстраивается в соответствии с параметром *иконалигнмент* . Может принимать одно из следующих `BarElementAlignment` значений:

- ALIGN_INVALID

- ALIGN_LEFT

- ALIGN_RIGHT

- ALIGN_CENTER

## <a name="cmfccaptionbarsetimagetooltip"></a><a name="setimagetooltip"></a> CMFCCaptionBar:: Сетимажетултип

Задает подсказку для изображения в строке заголовка.

```cpp
void SetImageToolTip(
    LPCTSTR lpszToolTip,
    LPCTSTR lpszDescription=NULL);
```

### <a name="parameters"></a>Параметры

*lpszToolTip*<br/>
окне Текст подсказки.

*лпсздескриптион*<br/>
окне Описание подсказки.

## <a name="cmfccaptionbarsetmargin"></a><a name="setmargin"></a> CMFCCaptionBar:: Сетмаргин

Задает расстояние между границей элемента заголовка и границей элемента управления "заголовок".

```cpp
void SetMargin(int nMargin);
```

### <a name="parameters"></a>Параметры

*нмаргин*<br/>
окне Расстояние (в пикселях) между границей элементов строки заголовка и границей элемента управления "заголовок".

## <a name="cmfccaptionbarsettext"></a><a name="settext"></a> CMFCCaptionBar:: SetText

Задает текстовую метку для строки заголовка.

```cpp
void SetText(
    const CString& strText,
    BarElementAlignment textAlignment=ALIGN_RIGHT);
```

### <a name="parameters"></a>Параметры

*стртекст*<br/>
окне Текстовая строка, которую необходимо задать.

*textAlignment*<br/>
окне Выравнивание текста.

### <a name="remarks"></a>Комментарии

Текстовая метка выстраивается по указанному параметру *TextAlignment* . Может принимать одно из следующих `BarElementAlignment` значений:

- ALIGN_INVALID

- ALIGN_LEFT

- ALIGN_RIGHT

- ALIGN_CENTER

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)
