---
description: 'Дополнительные сведения о: CMFCAutoHideButton Class'
title: Класс CMFCAutoHideButton
ms.date: 10/18/2018
f1_keywords:
- CMFCAutoHideButton
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::BringToTop
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::Create
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::GetAlignment
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::GetAutoHideWindow
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::GetParentToolBar
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::GetRect
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::GetSize
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::GetTextSize
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::HighlightButton
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::IsActive
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::IsHighlighted
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::IsHorizontal
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::IsTop
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::IsVisible
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::Move
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::OnDraw
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::OnDrawBorder
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::OnFillBackground
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::ReplacePane
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::ShowAttachedWindow
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::ShowButton
- AFXAUTOHIDEBUTTON/CMFCAutoHideButton::UnSetAutoHideMode
helpviewer_keywords:
- CMFCAutoHideButton [MFC], BringToTop
- CMFCAutoHideButton [MFC], Create
- CMFCAutoHideButton [MFC], GetAlignment
- CMFCAutoHideButton [MFC], GetAutoHideWindow
- CMFCAutoHideButton [MFC], GetParentToolBar
- CMFCAutoHideButton [MFC], GetRect
- CMFCAutoHideButton [MFC], GetSize
- CMFCAutoHideButton [MFC], GetTextSize
- CMFCAutoHideButton [MFC], HighlightButton
- CMFCAutoHideButton [MFC], IsActive
- CMFCAutoHideButton [MFC], IsHighlighted
- CMFCAutoHideButton [MFC], IsHorizontal
- CMFCAutoHideButton [MFC], IsTop
- CMFCAutoHideButton [MFC], IsVisible
- CMFCAutoHideButton [MFC], Move
- CMFCAutoHideButton [MFC], OnDraw
- CMFCAutoHideButton [MFC], OnDrawBorder
- CMFCAutoHideButton [MFC], OnFillBackground
- CMFCAutoHideButton [MFC], ReplacePane
- CMFCAutoHideButton [MFC], ShowAttachedWindow
- CMFCAutoHideButton [MFC], ShowButton
- CMFCAutoHideButton [MFC], UnSetAutoHideMode
ms.assetid: c80e6b8b-25ca-4d12-9d27-457731028ab0
ms.openlocfilehash: 9d100417193ea8a757b02b9cc8fad0cdedf668f9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336579"
---
# <a name="cmfcautohidebutton-class"></a>Класс CMFCAutoHideButton

Кнопка, отображающая или скрывающая [CDockablePane Class](../../mfc/reference/cdockablepane-class.md) , настроенный на скрытие.

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```
class CMFCAutoHideButton : public CObject
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCAutoHideButton::BringToTop](#bringtotop)||
|[CMFCAutoHideButton::Create](#create)|Создает и инициализирует кнопку автоматического скрытия.|
|[CMFCAutoHideButton::GetAlignment](#getalignment)|Извлекает выравнивание кнопки автоматического скрытия.|
|[CMFCAutoHideButton::GetAutoHideWindow](#getautohidewindow)|Возвращает объект [CDockablePane](../../mfc/reference/cdockablepane-class.md) , связанный с кнопкой автоматического скрытия.|
|[CMFCAutoHideButton::GetParentToolBar](#getparenttoolbar)||
|[CMFCAutoHideButton::GetRect](#getrect)||
|[CMFCAutoHideButton::GetSize](#getsize)|Определяет размер кнопки автоматического скрытия.|
|[CMFCAutoHideButton::GetTextSize](#gettextsize)|Возвращает размер текстовой метки для кнопки автоматического скрытия.|
|[CMFCAutoHideButton::HighlightButton](#highlightbutton)|Выделяет кнопку автоматического скрытия.|
|[CMFCAutoHideButton::IsActive](#isactive)|Указывает, активна ли кнопка автоматического скрытия.|
|[CMFCAutoHideButton::IsHighlighted](#ishighlighted)|Возвращает выделенное состояние кнопки автоматического скрытия.|
|[CMFCAutoHideButton::IsHorizontal](#ishorizontal)|Определяет, является кнопка автоматического скрытия горизонтальной или вертикальной.|
|[CMFCAutoHideButton::IsTop](#istop)||
|[CMFCAutoHideButton::IsVisible](#isvisible)|Указывает, является ли кнопка видимой.|
|[CMFCAutoHideButton::Move](#move)||
|[CMFCAutoHideButton::OnDraw](#ondraw)|Этот метод вызывается платформой при рисовании кнопки автоматического скрытия.|
|[CMFCAutoHideButton::OnDrawBorder](#ondrawborder)|Этот метод вызывается платформой при рисовании границ кнопки автоматического скрытия.|
|[CMFCAutoHideButton::OnFillBackground](#onfillbackground)|Этот метод вызывается платформой при заливке фона кнопки автоматического скрытия.|
|[CMFCAutoHideButton::ReplacePane](#replacepane)||
|[CMFCAutoHideButton::ShowAttachedWindow](#showattachedwindow)|Показывает или скрывает связанный [класс CDockablePane](../../mfc/reference/cdockablepane-class.md).|
|[CMFCAutoHideButton::ShowButton](#showbutton)|Показывает или скрывает кнопку автоматического скрытия.|
|[CMFCAutoHideButton::UnSetAutoHideMode](#unsetautohidemode)||

## <a name="remarks"></a>Комментарии

При создании `CMFCAutoHideButton` объект прикрепляется к [классу CDockablePane](../../mfc/reference/cdockablepane-class.md). В результате взаимодействия пользователя с объектом `CMFCAutoHideButton` показывается или скрывается объект `CDockablePane`.

По умолчанию при включении автоматического скрытия платформа автоматически создает объект класса `CMFCAutoHideButton`. Вместо объекта класса `CMFCAutoHideButton` платформа может создавать элемент настраиваемого класса пользовательского интерфейса. Чтобы указать, какой настраиваемый класс пользовательского интерфейса должна использовать платформа, задайте для статической переменной-члена `CMFCAutoHideBar::m_pAutoHideButtonRTS` значение, равное необходимому настраиваемому классу. По умолчанию для переменной задано значение `CMFCAutoHideButton`.

## <a name="example"></a>Пример

В этом примере демонстрируется создание объекта `CMFCAutoHideButton` и использование различных методов класса `CMFCAutoHideButton`. В этом примере демонстрируется инициализация объекта `CMFCAutoHideButton` с помощью метода `Create`, а также отображение связанного класса `CDockablePane` и кнопки автоматического скрытия.

[!code-cpp[NVC_MFC_RibbonApp#32](../../mfc/reference/codesnippet/cpp/cmfcautohidebutton-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CMFCAutoHideButton`

## <a name="requirements"></a>Требования

**Заголовок:** afxautohidebutton.h

## <a name="cmfcautohidebuttonbringtotop"></a><a name="bringtotop"></a> CMFCAutoHideButton:: Брингтотоп

```cpp
void BringToTop();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebuttoncreate"></a><a name="create"></a> CMFCAutoHideButton:: Create

Создает и инициализирует кнопку автоматического скрытия.

```
virtual BOOL Create(
    CMFCAutoHideBar* pParentBar,
    CDockablePane* pAutoHideWnd,
    DWORD dwAlignment);
```

### <a name="parameters"></a>Параметры

*ппарентбар*<br/>
окне Указатель на родительскую панель инструментов.

*паутохидевнд*<br/>
окне Указатель на объект [CDockablePane](../../mfc/reference/cdockablepane-class.md) . Эта кнопка автоматического скрытия скрывает и показывает, что `CDockablePane` .

*двалигнмент*<br/>
окне Значение, указывающее выравнивание кнопки с основным окном фрейма.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

При создании `CMFCAutoHideButton` объекта необходимо связать кнопку автоматического скрытия с конкретным `CDockablePane` . Пользователь может использовать кнопку автоматического скрытия для скрытия и отображения связанного `CDockablePane` .

Параметр *двалигнмент* указывает, где находится кнопка автоматического скрытия в приложении. Параметру может быть присвоено одно из следующих значений:

- CBRS_ALIGN_LEFT

- CBRS_ALIGN_RIGHT

- CBRS_ALIGN_TOP

- CBRS_ALIGN_BOTTOM

## <a name="cmfcautohidebuttongetalignment"></a><a name="getalignment"></a> CMFCAutoHideButton:: Alignment

Извлекает выравнивание кнопки автоматического скрытия.

```
DWORD GetAlignment() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение типа DWORD, содержащее текущее выравнивание кнопки автоматического скрытия.

### <a name="remarks"></a>Комментарии

Выравнивание кнопки автоматического скрытия указывает, где находится кнопка в приложении. Это может быть одно из следующих значений:

- CBRS_ALIGN_LEFT

- CBRS_ALIGN_RIGHT

- CRBS_ALIGN_TOP

- CBRS_ALIGN_BOTTOM

## <a name="cmfcautohidebuttongetautohidewindow"></a><a name="getautohidewindow"></a> CMFCAutoHideButton:: Жетаутохидевиндов

Возвращает объект [CDockablePane](../../mfc/reference/cdockablepane-class.md) , связанный с кнопкой автоматического скрытия.

```
CDockablePane* GetAutoHideWindow() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на связанный `CDockablePane` объект.

### <a name="remarks"></a>Комментарии

Чтобы связать кнопку автоматического скрытия с `CDockablePane` , передайте в `CDockablePane` метод [CMFCAutoHideButton:: Create](#create) параметр в качестве параметра.

## <a name="cmfcautohidebuttongetparenttoolbar"></a><a name="getparenttoolbar"></a> CMFCAutoHideButton:: Жетпаренттулбар

```
CMFCAutoHideBar* GetParentToolBar();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebuttongetrect"></a><a name="getrect"></a> CMFCAutoHideButton:: коrect

```
CRect GetRect() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebuttongetsize"></a><a name="getsize"></a> CMFCAutoHideButton:: DataSize

Определяет размер кнопки автоматического скрытия.

```
CSize GetSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

`CSize`Объект, содержащий размер кнопки.

### <a name="remarks"></a>Комментарии

Вычисляемый размер включает размер границы кнопки автоматического скрытия.

## <a name="cmfcautohidebuttongettextsize"></a><a name="gettextsize"></a> CMFCAutoHideButton:: Жеттекстсизе

Возвращает размер текстовой метки для кнопки автоматического скрытия.

```
virtual CSize GetTextSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Объект [ксизе](../../atl-mfc-shared/reference/csize-class.md) , который содержит размер текста для кнопки автоматического скрытия.

## <a name="cmfcautohidebuttonisactive"></a><a name="isactive"></a> CMFCAutoHideButton:: @ Active

Указывает, активна ли кнопка автоматического скрытия.

```
BOOL IsActive() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если кнопка автоматического скрытия активна; В противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Кнопка автоматического скрытия активна, когда отображается связанное окно [класса CDockablePane](../../mfc/reference/cdockablepane-class.md) .

## <a name="cmfcautohidebuttonishorizontal"></a><a name="ishorizontal"></a> CMFCAutoHideButton:: по горизонтали

Определяет, является кнопка автоматического скрытия горизонтальной или вертикальной.

```
BOOL IsHorizontal() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если кнопка является горизонтальной; 0 в противном случае.

### <a name="remarks"></a>Комментарии

Платформа задает ориентацию объекта [CMFCAutoHideButton](../../mfc/reference/cmfcautohidebutton-class.md) при его создании.  Можно управлять ориентацией с помощью параметра *двалигнмент* в методе [CMFCAutoHideButton:: Create](#create) .

## <a name="cmfcautohidebuttonistop"></a><a name="istop"></a> CMFCAutoHideButton:: Истоп

```
BOOL IsTop() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebuttonisvisible"></a><a name="isvisible"></a> CMFCAutoHideButton:: Visible

Указывает, является ли кнопка автоматического скрытия видимой.

```
virtual BOOL IsVisible() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если кнопка видима; В противном случае — значение FALSE.

## <a name="cmfcautohidebuttonondraw"></a><a name="ondraw"></a> CMFCAutoHideButton:: OnDraw

Этот метод вызывается платформой при рисовании кнопки автоматического скрытия.

```
virtual void OnDraw(CDC* pDC);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

### <a name="remarks"></a>Комментарии

Если вы хотите настроить внешний вид кнопок автоматического скрытия в приложении, создайте новый класс, производный от `CMFCAutoHideButton` . В производном классе Переопределите этот метод.

## <a name="cmfcautohidebuttonondrawborder"></a><a name="ondrawborder"></a> CMFCAutoHideButton:: Ондравбордер

Этот метод вызывается платформой при рисовании границ кнопки автоматического скрытия.

```
virtual void OnDrawBorder(
    CDC* pDC,
    CRect rectBounds,
    CRect rectBorderSize);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*ректбаундс*<br/>
окне Ограничивающий прямоугольник кнопки автоматического скрытия.

*ректбордерсизе*<br/>
окне Толщина границы для каждой стороны кнопки автоматического скрытия.

### <a name="remarks"></a>Комментарии

Если необходимо настроить границы каждой кнопки автоматического скрытия в приложении, создайте новый класс, производный от `CMFCAutoHideButton` . В производном классе Переопределите этот метод.

## <a name="cmfcautohidebuttononfillbackground"></a><a name="onfillbackground"></a> CMFCAutoHideButton:: Онфиллбаккграунд

Этот метод вызывается платформой при заливке фона кнопки автоматического скрытия.

```
virtual void OnFillBackground(
    CDC* pDC,
    CRect rect);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*rect*<br/>
окне Ограничивающий прямоугольник кнопки автоматического скрытия.

### <a name="remarks"></a>Комментарии

Если вы хотите настроить фон для кнопок автоматического скрытия в приложении, создайте новый класс, производный от `CMFCAutoHideButton` . В производном классе Переопределите этот метод.

## <a name="cmfcautohidebuttonshowattachedwindow"></a><a name="showattachedwindow"></a> CMFCAutoHideButton:: Шоваттачедвиндов

Показывает или скрывает связанный [класс CDockablePane](../../mfc/reference/cdockablepane-class.md).

```cpp
void ShowAttachedWindow(BOOL bShow);
```

### <a name="parameters"></a>Параметры

*bShow*<br/>
окне Логическое значение, указывающее, показывает ли этот метод присоединенный объект `CDockablePane` .

## <a name="cmfcautohidebuttonshowbutton"></a><a name="showbutton"></a> CMFCAutoHideButton:: ShowButton

Показывает или скрывает кнопку автоматического скрытия.

```
virtual void ShowButton(BOOL bShow);
```

### <a name="parameters"></a>Параметры

*bShow*<br/>
окне Логическое значение, указывающее, следует ли отображать кнопку автоматического скрытия.

## <a name="cmfcautohidebuttonmove"></a><a name="move"></a> CMFCAutoHideButton:: Move

```cpp
void Move(int nOffset);
```

### <a name="parameters"></a>Параметры

окне *ноффсет*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebuttonreplacepane"></a><a name="replacepane"></a> CMFCAutoHideButton:: Реплацепане

```cpp
void ReplacePane(CDockablePane* pNewBar);
```

### <a name="parameters"></a>Параметры

окне *пневбар*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebuttonunsetautohidemode"></a><a name="unsetautohidemode"></a> CMFCAutoHideButton:: Унсетаутохидемоде

Отключение режима автоматического скрытия.

```
virtual void UnSetAutoHideMode(CDockablePane* pFirstBarInGroup);
```

### <a name="parameters"></a>Параметры

*пфирстбаринграуп*<br/>
окне Указатель на первую строку в группе.

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebuttonhighlightbutton"></a><a name="highlightbutton"></a> CMFCAutoHideButton:: Хигхлигхтбуттон

Выделяется кнопка автоматического скрытия.

```
virtual void HighlightButton(BOOL bHighlight);
```

### <a name="parameters"></a>Параметры

*бхигхлигхт*<br/>
Указывает новое состояние кнопки автоматического скрытия. Значение TRUE показывает, что кнопка выделена, значение FALSE указывает, что кнопка не выделяется.

### <a name="remarks"></a>Комментарии

## <a name="cmfcautohidebuttonishighlighted"></a><a name="ishighlighted"></a> CMFCAutoHideButton:: выделять

Возвращает состояние выделения для кнопки автоматического скрытия.

```
virtual BOOL IsHighlighted() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если кнопка автоматического скрытия выделена; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCAutoHideBar](../../mfc/reference/cmfcautohidebar-class.md)<br/>
[Класс CAutoHideDockSite](../../mfc/reference/cautohidedocksite-class.md)
