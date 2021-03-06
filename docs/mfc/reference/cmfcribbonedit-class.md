---
description: 'Дополнительные сведения о: Кмфкриббонедит Class'
title: Класс Кмфкриббонедит
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonEdit
- AFXRIBBONEDIT/CMFCRibbonEdit
- AFXRIBBONEDIT/CMFCRibbonEdit::CMFCRibbonEdit
- AFXRIBBONEDIT/CMFCRibbonEdit::CanBeStretched
- AFXRIBBONEDIT/CMFCRibbonEdit::CopyFrom
- AFXRIBBONEDIT/CMFCRibbonEdit::CreateEdit
- AFXRIBBONEDIT/CMFCRibbonEdit::DestroyCtrl
- AFXRIBBONEDIT/CMFCRibbonEdit::DropDownList
- AFXRIBBONEDIT/CMFCRibbonEdit::EnableSpinButtons
- AFXRIBBONEDIT/CMFCRibbonEdit::GetCompactSize
- AFXRIBBONEDIT/CMFCRibbonEdit::GetEditText
- AFXRIBBONEDIT/CMFCRibbonEdit::GetIntermediateSize
- AFXRIBBONEDIT/CMFCRibbonEdit::GetTextAlign
- AFXRIBBONEDIT/CMFCRibbonEdit::GetWidth
- AFXRIBBONEDIT/CMFCRibbonEdit::HasCompactMode
- AFXRIBBONEDIT/CMFCRibbonEdit::HasFocus
- AFXRIBBONEDIT/CMFCRibbonEdit::HasLargeMode
- AFXRIBBONEDIT/CMFCRibbonEdit::HasSpinButtons
- AFXRIBBONEDIT/CMFCRibbonEdit::IsHighlighted
- AFXRIBBONEDIT/CMFCRibbonEdit::OnAfterChangeRect
- AFXRIBBONEDIT/CMFCRibbonEdit::OnDraw
- AFXRIBBONEDIT/CMFCRibbonEdit::OnDrawLabelAndImage
- AFXRIBBONEDIT/CMFCRibbonEdit::OnDrawOnList
- AFXRIBBONEDIT/CMFCRibbonEdit::OnEnable
- AFXRIBBONEDIT/CMFCRibbonEdit::OnHighlight
- AFXRIBBONEDIT/CMFCRibbonEdit::OnKey
- AFXRIBBONEDIT/CMFCRibbonEdit::OnLButtonDown
- AFXRIBBONEDIT/CMFCRibbonEdit::OnLButtonUp
- AFXRIBBONEDIT/CMFCRibbonEdit::OnRTLChanged
- AFXRIBBONEDIT/CMFCRibbonEdit::OnShow
- AFXRIBBONEDIT/CMFCRibbonEdit::Redraw
- AFXRIBBONEDIT/CMFCRibbonEdit::SetACCData
- AFXRIBBONEDIT/CMFCRibbonEdit::SetEditText
- AFXRIBBONEDIT/CMFCRibbonEdit::SetTextAlign
- AFXRIBBONEDIT/CMFCRibbonEdit::SetWidth
helpviewer_keywords:
- CMFCRibbonEdit [MFC], CMFCRibbonEdit
- CMFCRibbonEdit [MFC], CanBeStretched
- CMFCRibbonEdit [MFC], CMFCRibbonEdit
- CMFCRibbonEdit [MFC], CopyFrom
- CMFCRibbonEdit [MFC], CreateEdit
- CMFCRibbonEdit [MFC], DestroyCtrl
- CMFCRibbonEdit [MFC], DropDownList
- CMFCRibbonEdit [MFC], EnableSpinButtons
- CMFCRibbonEdit [MFC], GetCompactSize
- CMFCRibbonEdit [MFC], GetEditText
- CMFCRibbonEdit [MFC], GetIntermediateSize
- CMFCRibbonEdit [MFC], GetTextAlign
- CMFCRibbonEdit [MFC], GetWidth
- CMFCRibbonEdit [MFC], HasCompactMode
- CMFCRibbonEdit [MFC], HasFocus
- CMFCRibbonEdit [MFC], HasLargeMode
- CMFCRibbonEdit [MFC], HasSpinButtons
- CMFCRibbonEdit [MFC], IsHighlighted
- CMFCRibbonEdit [MFC], OnAfterChangeRect
- CMFCRibbonEdit [MFC], OnDraw
- CMFCRibbonEdit [MFC], OnDrawLabelAndImage
- CMFCRibbonEdit [MFC], OnDrawOnList
- CMFCRibbonEdit [MFC], OnEnable
- CMFCRibbonEdit [MFC], OnHighlight
- CMFCRibbonEdit [MFC], OnKey
- CMFCRibbonEdit [MFC], OnLButtonDown
- CMFCRibbonEdit [MFC], OnLButtonUp
- CMFCRibbonEdit [MFC], OnRTLChanged
- CMFCRibbonEdit [MFC], OnShow
- CMFCRibbonEdit [MFC], Redraw
- CMFCRibbonEdit [MFC], SetACCData
- CMFCRibbonEdit [MFC], SetEditText
- CMFCRibbonEdit [MFC], SetTextAlign
- CMFCRibbonEdit [MFC], SetWidth
ms.assetid: 9b85f1f2-446b-454e-9af9-104fdad8a897
ms.openlocfilehash: be88698de9f98c590efebd4e2e8780d810aa8b96
ms.sourcegitcommit: c0c9cdae79f19655e809a4979227c51bb19cff63
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "102236567"
---
# <a name="cmfcribbonedit-class"></a>Класс Кмфкриббонедит

Реализует элемент управления "Правка", расположенный на панели ленты.

## <a name="syntax"></a>Синтаксис

```cpp
class CMFCRibbonEdit : public CMFCRibbonButton
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание:|
|----------|-----------------|
|[Кмфкриббонедит:: Кмфкриббонедит](#cmfcribbonedit)|Формирует объект `CMFCRibbonEdit`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание:|
|----------|-----------------|
|[Кмфкриббонедит:: Канбестретчед](#canbestretched)|Указывает, может ли высота `CMFCRibbonEdit` элемента управления увеличиваться по вертикали до высоты строки ленты.|
|[Кмфкриббонедит:: Кмфкриббонедит](#cmfcribbonedit)|Формирует объект `CMFCRibbonEdit`.|
|[Кмфкриббонедит:: CopyFrom](#copyfrom)|Копирует состояние указанного `CMFCRibbonEdit` объекта в текущий `CMFCRibbonEdit` объект.|
|[Кмфкриббонедит:: Креатидит](#createedit)|Создает новое текстовое поле для `CMFCRibbonEdit` объекта.|
|[Кмфкриббонедит::D Естройктрл](#destroyctrl)|Уничтожает `CMFCRibbonEdit` объект.|
|[Кмфкриббонедит::D Ропдовнлист](#dropdownlist)|Удаляет список.|
|[Кмфкриббонедит:: Енаблеспинбуттонс](#enablespinbuttons)|Включает и задает диапазон кнопки "Счетчик" для текстового поля.|
|[Кмфкриббонедит:: Жеткомпактсизе](#getcompactsize)|Получает компактный размер `CFMCRibbonEdit` объекта.|
|[Кмфкриббонедит:: Жетедиттекст](#getedittext)|Извлекает текст из текстового поля.|
|[Кмфкриббонедит:: GetIntermediateSize](#getintermediatesize)|Возвращает промежуточный размер `CMFCRibbonEdit` объекта.|
|[Кмфкриббонедит:: Жеттексталигн](#gettextalign)|Извлекает выравнивание текста в текстовом поле.|
|[Кмфкриббонедит:: Полуширинный](#getwidth)|Получает ширину элемента управления в пикселях `CMFCRibbonEdit` .|
|[Кмфкриббонедит:: Хаскомпактмоде](#hascompactmode)|Указывает, может ли размер отображаемого `CMFCRibbonEdit` элемента управления сжиматься.|
|[Кмфкриббонедит:: Хасфокус](#hasfocus)|Указывает `CMFCRIbbonEdit` , имеет ли элемент управления фокус.|
|[Кмфкриббонедит:: Хасларжемоде](#haslargemode)|Указывает, может ли размер экрана для `CMFCRibbonEdit` элемента управления быть большим.|
|[Кмфкриббонедит:: Хасспинбуттонс](#hasspinbuttons)|Указывает, содержит ли текстовое поле кнопку с вращением.|
|[Кмфкриббонедит:: выделять](#ishighlighted)|Указывает, `CMFCRibbonEdit` выделен ли элемент управления.|
|[Кмфкриббонедит:: Онафтерчанжерект](#onafterchangerect)|Вызывается структурой при изменении размеров отображаемого прямоугольника для `CMFCRibbonEdit` элемента управления.|
|[Кмфкриббонедит:: OnDraw](#ondraw)|Вызывается платформой для рисования `CMFCRibbonEdit` элемента управления.|
|[Кмфкриббонедит:: Ондравлабеландимаже](#ondrawlabelandimage)|Вызывается платформой для рисования метки и изображения для `CMFCRibbonEdit` элемента управления.|
|[Кмфкриббонедит:: Ондравонлист](#ondrawonlist)|Вызывается структурой для отрисовки `CMFCRibbonEdit` элемента управления в списке команд.|
|[Кмфкриббонедит:: OnEnable](#onenable)|Вызывается платформой для включения или отключения `CMFCRibbonEdit` элемента управления.|
|[Кмфкриббонедит:: onhighlight](#onhighlight)|Вызывается структурой, когда указатель попадает или оставляет границы `CMFCRibbonEdit` элемента управления.|
|[Кмфкриббонедит:: Онкэй](#onkey)|Вызывается структурой, когда пользователь нажимает на KeyTip, а `CMFCRibbonEdit` элемент управления находится в фокусе.|
|[Кмфкриббонедит:: Онлбуттондовн](#onlbuttondown)|Вызывается платформой для обновления `CMFCRibbonEdit` элемента управления при нажатии пользователем левой кнопки мыши на элементе управления.|
|[Кмфкриббонедит:: Онлбуттонуп](#onlbuttonup)|Вызывается структурой, когда пользователь отпускает левую кнопку мыши.|
|[Кмфкриббонедит:: Онртлчанжед](#onrtlchanged)|Вызывается платформой для обновления `CMFCRibbonEdit` элемента управления при изменении направления в макете.|
|[Кмфкриббонедит:: onShow](#onshow)|Вызывается платформой для отображения или скрытия `CMFCRibbonEdit` элемента управления.|
|[Кмфкриббонедит:: перерисовка](#redraw)|Обновляет отображение `CMFCRibbonEdit` элемента управления.|
|[Кмфкриббонедит:: Сетаккдата](#setaccdata)|Задает данные специальных возможностей для `CMFCRibbonEdit` объекта.|
|[Кмфкриббонедит:: Сетедиттекст](#setedittext)|Задает текст в текстовом поле.|
|[Кмфкриббонедит:: Сеттексталигн](#settextalign)|Задает выравнивание текста для текстового поля.|
|[Кмфкриббонедит:: Сетвидс](#setwidth)|Задает ширину текстового поля для `CMFCRibbonEdit` элемента управления.|

## <a name="remarks"></a>Remarks

## <a name="example"></a>Пример

В следующем примере демонстрируется создание `CMFCRibbonEdit` объекта, отображение счетчиков рядом с элементом управления "поле ввода" и задание текста элемента управления "поле ввода". Этот фрагмент кода является частью [демонстрационного примера MS Office 2007](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_MSOffice2007Demo#7](../../mfc/reference/codesnippet/cpp/cmfcribbonedit-class_1.cpp)]

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонедит. h

## <a name="cmfcribboneditcanbestretched"></a><a name="canbestretched"></a> Кмфкриббонедит:: Канбестретчед

Указывает, может ли высота элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) увеличиваться вертикально до высоты строки ленты.

```cpp
virtual BOOL CanBeStretched();
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает значение FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditcmfcribbonedit"></a><a name="cmfcribbonedit"></a> Кмфкриббонедит:: Кмфкриббонедит

Конструирует объект [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
CMFCRibbonEdit(
    UINT nID,
    int nWidth,
    LPCTSTR lpszLabel = NULL,
    int nImage = -1);

CMFCRibbonEdit();
```

### <a name="parameters"></a>Параметры

*nID*<br/>
окне Идентификатор команды для `CMFCRibbonEdit` элемента управления.

*нвидс*<br/>
окне Ширина (в пикселях) текстового поля `CMFCRibbonEdit` элемента управления.

*лпсзлабел*<br/>
окне Метка для `CMFCRibbonEdit` элемента управления.

*нимаже*<br/>
окне Индекс мелкого изображения, используемого для `CMFCRibbonEdit` элемента управления. Коллекция небольших изображений поддерживается родительской категорией ленты.

### <a name="remarks"></a>Комментарии

`CMFCRibbonEdit`Элемент управления не использует большое изображение.

## <a name="cmfcribboneditcopyfrom"></a><a name="copyfrom"></a> Кмфкриббонедит:: CopyFrom

Копирует состояние указанного объекта [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) в текущий объект [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual void CopyFrom(const CMFCRibbonBaseElement& src);
```

### <a name="parameters"></a>Параметры

*src*<br/>
окне Исходный `CMFCRibbonEdit` объект.

### <a name="remarks"></a>Комментарии

Параметр *src* должен иметь тип `CMFCRibbonEdit` .

## <a name="cmfcribboneditcreateedit"></a><a name="createedit"></a> Кмфкриббонедит:: Креатидит

Создает новое текстовое поле для объекта [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual CMFCRibbonRichEditCtrl* CreateEdit(
    CWnd* pWndParent,
    DWORD dwEditStyle);
```

### <a name="parameters"></a>Параметры

*пвндпарент*<br/>
окне Указатель на родительское окно `CMFCRibbonEdit` объекта.

*дведитстиле*<br/>
окне Задает стиль текстового поля. Стили окон, перечисленные в разделе "Примечания", можно объединить в [стили элемента управления Edit](/windows/win32/Controls/edit-control-styles) , описанные в Windows SDK.

### <a name="return-value"></a>Возвращаемое значение

Указатель на новое текстовое поле, если метод был успешным; в противном случае значение NULL.

### <a name="remarks"></a>Комментарии

Переопределите этот метод в производном классе, чтобы создать настраиваемое текстовое поле.

К текстовому полю можно применить следующие [стили окна](../../mfc/reference/styles-used-by-mfc.md#window-styles) :

- **WS_CHILD**

- **WS_VISIBLE**

- **WS_DISABLED**

- **WS_GROUP**

- **WS_TABSTOP**

## <a name="cmfcribboneditdestroyctrl"></a><a name="destroyctrl"></a> Кмфкриббонедит::D Естройктрл

Уничтожает объект [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual void DestroyCtrl();
```

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditdropdownlist"></a><a name="dropdownlist"></a> Кмфкриббонедит::D Ропдовнлист

Удаляет список.

```cpp
virtual void DropDownList();
```

### <a name="remarks"></a>Комментарии

По умолчанию этот метод не выполняет никаких действий. Переопределите этот метод, чтобы раскрывающийся список.

## <a name="cmfcribboneditenablespinbuttons"></a><a name="enablespinbuttons"></a> Кмфкриббонедит:: Енаблеспинбуттонс

Включает и задает диапазон кнопки "Счетчик" для текстового поля.

```cpp
void EnableSpinButtons(
    int nMin,
    int nMax);
```

### <a name="parameters"></a>Параметры

*Nмин.*<br/>
окне Минимальное значение кнопки счетчика.

*Nмакс.*<br/>
окне Максимальное значение кнопки счетчика.

### <a name="remarks"></a>Комментарии

На кнопках счетчика отображается стрелка вверх и вниз, позволяющая пользователям перемещаться по фиксированному набору значений.

## <a name="cmfcribboneditgetcompactsize"></a><a name="getcompactsize"></a> Кмфкриббонедит:: Жеткомпактсизе

Получает компактный размер объекта [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual CSize GetCompactSize(CDC* pDC);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства для `CMFCRibbonEdit` объекта.

### <a name="return-value"></a>Возвращаемое значение

Размер в компактном `CMFCRibbonEdit` объекте.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditgetedittext"></a><a name="getedittext"></a> Кмфкриббонедит:: Жетедиттекст

Извлекает текст из текстового поля.

```cpp
CString GetEditText() const;
```

### <a name="return-value"></a>Возвращаемое значение

Текст в текстовом поле.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditgetintermediatesize"></a><a name="getintermediatesize"></a> Кмфкриббонедит:: GetIntermediateSize

Возвращает промежуточный размер объекта [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual CSize GetIntermediateSize(CDC* pDC);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства для `CMFCRibbonEdit` объекта.

### <a name="return-value"></a>Возвращаемое значение

Промежуточный размер `CMFCRibbonEdit` объекта.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditgettextalign"></a><a name="gettextalign"></a> Кмфкриббонедит:: Жеттексталигн

Извлекает выравнивание текста в текстовом поле.

```cpp
int GetTextAlign() const;
```

### <a name="return-value"></a>Возвращаемое значение

Перечислимое значение выравнивания текста. Возможные значения см. в разделе "Примечания".

### <a name="remarks"></a>Комментарии

Возвращаемое значение является одним из следующих стилей элемента управления Edit:

- **ES_LEFT** для выравнивания по левому краю

- **ES_CENTER** для выравнивания по центру

- **ES_RIGHT** для выравнивания по правому краю

Дополнительные сведения об этих стилях см. в разделе [Edit Control Styles](/windows/win32/Controls/edit-control-styles).

## <a name="cmfcribboneditgetwidth"></a><a name="getwidth"></a> Кмфкриббонедит:: Полуширинный

Получает ширину (в пикселях) элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
int GetWidth(BOOL bInFloatyMode = FALSE) const;
```

### <a name="parameters"></a>Параметры

*бинфлоатимоде*<br/>
окне Значение TRUE `CMFCRibbonEdit` , если элемент управления находится в режиме с плавающей запятой; в противном случае — значение false.

### <a name="return-value"></a>Возвращаемое значение

Ширина (в пикселях) `CMFCRibbonEdit` элемента управления.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonedithascompactmode"></a><a name="hascompactmode"></a> Кмфкриббонедит:: Хаскомпактмоде

Указывает, может ли размер отображаемого элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) быть компактным.

```cpp
virtual BOOL HasCompactMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает значение TRUE.

### <a name="remarks"></a>Комментарии

По умолчанию этот метод всегда возвращает значение TRUE. Переопределите этот метод, чтобы указать, может ли размер отображения быть компактным.

## <a name="cmfcribbonedithasfocus"></a><a name="hasfocus"></a> Кмфкриббонедит:: Хасфокус

Указывает, имеет ли элемент управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) фокус.

```cpp
virtual BOOL HasFocus() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если `CMFCRibbonEdit` элемент управления имеет фокус; в противном случае — значение false.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonedithaslargemode"></a><a name="haslargemode"></a> Кмфкриббонедит:: Хасларжемоде

Указывает, может ли размер отображаемого элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) быть большим.

```cpp
virtual BOOL HasLargeMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает значение FALSE.

### <a name="remarks"></a>Комментарии

По умолчанию этот метод всегда возвращает значение FALSE. Переопределите этот метод, чтобы указать, может ли размер отображения быть большим.

## <a name="cmfcribbonedithasspinbuttons"></a><a name="hasspinbuttons"></a> Кмфкриббонедит:: Хасспинбуттонс

Указывает, содержит ли текстовое поле кнопку с вращением.

```cpp
virtual BOOL HasSpinButtons() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если текстовое поле содержит кнопку счетчика; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditishighlighted"></a><a name="ishighlighted"></a> Кмфкриббонедит:: выделять

Указывает, выделен ли элемент управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual BOOL IsHighlighted() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если `CMFCRibbonEdit` элемент управления выделен; в противном случае — значение false.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditonafterchangerect"></a><a name="onafterchangerect"></a> Кмфкриббонедит:: Онафтерчанжерект

Вызывается структурой при изменении размеров отображаемого прямоугольника для элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual void OnAfterChangeRect(CDC* pDC);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства для `CMFCRibbonEdit` элемента управления.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditondraw"></a><a name="ondraw"></a> Кмфкриббонедит:: OnDraw

Вызывается платформой для рисования элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual void OnDraw(CDC* pDC);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства для `CMFCRibbonEdit` элемента управления.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditondrawlabelandimage"></a><a name="ondrawlabelandimage"></a> Кмфкриббонедит:: Ондравлабеландимаже

Вызывается платформой для рисования метки и изображения для элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual void OnDrawLabelAndImage(CDC* pDC);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства для `CMFCRibbonEdit` элемента управления.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditondrawonlist"></a><a name="ondrawonlist"></a> Кмфкриббонедит:: Ондравонлист

Вызывается платформой для рисования элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) в списке команд.

```cpp
virtual void OnDrawOnList(
    CDC* pDC,
    CString strText,
    int nTextOffset,
    CRect rect,
    BOOL bIsSelected,
    BOOL bHighlighted);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства для `CMFCRibbonEdit` элемента управления.

*стртекст*<br/>
[in] Отображаемый текст.

*нтекстоффсет*<br/>
окне Расстояние (в пикселях) от левого края окна списка до отображаемого текста.

*перетаскиваемые*<br/>
окне Отображаемый прямоугольник для `CMFCRibbonEdit` элемента управления.

*бисселектед*<br/>
окне Этот параметр не используется.

*бхигхлигхтед*<br/>
окне Этот параметр не используется.

### <a name="remarks"></a>Комментарии

В окне Список команд отображаются элементы управления ленты, позволяющие пользователям настраивать панель быстрого доступа.

## <a name="cmfcribboneditonenable"></a><a name="onenable"></a> Кмфкриббонедит:: OnEnable

Вызывается платформой для включения или отключения элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual void OnEnable(BOOL bEnable);
```

### <a name="parameters"></a>Параметры

*bEnable*<br/>
окне Значение TRUE, чтобы включить элемент управления; Значение FALSE, чтобы отключить элемент управления.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditonhighlight"></a><a name="onhighlight"></a> Кмфкриббонедит:: onhighlight

Вызывается структурой, когда указатель попадает или оставляет границы элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual void OnHighlight(BOOL bHighlight);
```

### <a name="parameters"></a>Параметры

*бхигхлигхт*<br/>
окне Значение TRUE, если указатель находится в границах `CMFCRibbonEdit` элемента управления; в противном случае — значение false.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditonkey"></a><a name="onkey"></a> Кмфкриббонедит:: Онкэй

Вызывается структурой, когда пользователь нажимает на KeyTip, а элемент управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) — фокус.

```cpp
virtual BOOL OnKey(BOOL bIsMenuKey);
```

### <a name="parameters"></a>Параметры

*бисменукэй*<br/>
окне Значение TRUE, если KeyTip отображает всплывающее меню; в противном случае — значение FALSE.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если событие было обработано; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditonlbuttondown"></a><a name="onlbuttondown"></a> Кмфкриббонедит:: Онлбуттондовн

Вызывается платформой для обновления элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) , когда пользователь нажимает на элементе управления левую кнопку мыши.

```cpp
virtual void OnLButtonDown(CPoint point);
```

### <a name="parameters"></a>Параметры

*точки*<br/>
окне Этот параметр не используется.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditonlbuttonup"></a><a name="onlbuttonup"></a> Кмфкриббонедит:: Онлбуттонуп

Вызывается структурой, когда пользователь отпускает левую кнопку мыши.

```cpp
virtual void OnLButtonUp(CPoint point);
```

### <a name="parameters"></a>Параметры

*точки*<br/>
окне Этот параметр не используется.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditonrtlchanged"></a><a name="onrtlchanged"></a> Кмфкриббонедит:: Онртлчанжед

Вызывается платформой для обновления элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) при изменении направления в макете.

```cpp
virtual void OnRTLChanged(BOOL bIsRTL);
```

### <a name="parameters"></a>Параметры

*бисртл*<br/>
окне Значение TRUE, если макет размещается справа налево; Значение FALSE, если макет расположен слева направо.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditonshow"></a><a name="onshow"></a> Кмфкриббонедит:: onShow

Вызывается платформой для отображения или скрытия элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual void OnShow(BOOL bShow);
```

### <a name="parameters"></a>Параметры

*bShow*<br/>
окне Значение TRUE для отображения элемента управления; Значение FALSE, чтобы скрыть элемент управления.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditredraw"></a><a name="redraw"></a> Кмфкриббонедит:: перерисовка

Обновляет отображение элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual void Redraw();
```

### <a name="remarks"></a>Комментарии

Этот метод перерисовывает прямоугольник отображения для `CMFCRibbonEdit` объекта путем косвенного вызова [CWnd:: редраввиндов](/windows/win32/api/winuser/nf-winuser-redrawwindow) с набором флагов RDW_INVALIDATE, RDW_ERASE и RDW_UPDATENOW.

## <a name="cmfcribboneditsetaccdata"></a><a name="setaccdata"></a> Кмфкриббонедит:: Сетаккдата

Задает данные специальных возможностей для объекта [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
virtual BOOL SetACCData(
    CWnd* pParent,
    CAccessibilityData& data);
```

### <a name="parameters"></a>Параметры

*ппарент*<br/>
Указатель на родительское окно для `CMFCRibbonEdit` объекта.

*data*<br/>
Данные о специальных возможностях для `CMFCRibbonEdit` объекта.

### <a name="return-value"></a>Возвращаемое значение

Всегда возвращает значение TRUE.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribboneditsetedittext"></a><a name="setedittext"></a> Кмфкриббонедит:: Сетедиттекст

Задает текст в текстовом поле.

```cpp
void SetEditText(CString strText);
```

### <a name="parameters"></a>Параметры

*стртекст*<br/>
окне Текст для текстового поля.

## <a name="cmfcribboneditsettextalign"></a><a name="settextalign"></a> Кмфкриббонедит:: Сеттексталигн

Задает выравнивание текста для текстового поля.

```cpp
void SetTextAlign(int nAlign);
```

### <a name="parameters"></a>Параметры

*налигн*<br/>
окне Перечислимое значение выравнивания текста. Возможные значения см. в разделе "Примечания".

### <a name="remarks"></a>Комментарии

Параметр *налигн* является одним из следующих стилей элемента управления Edit:

- ES_LEFT для выравнивания по левому краю

- ES_CENTER для выравнивания по центру

- ES_RIGHT для выравнивания по правому краю

Дополнительные сведения об этих стилях см. в разделе [Edit Control Styles](/windows/win32/Controls/edit-control-styles).

## <a name="cmfcribboneditsetwidth"></a><a name="setwidth"></a> Кмфкриббонедит:: Сетвидс

Задает ширину текстового поля для элемента управления [кмфкриббонедит](../../mfc/reference/cmfcribbonedit-class.md) .

```cpp
void SetWidth(
    int nWidth,
    BOOL bInFloatyMode = FALSE);
```

### <a name="parameters"></a>Параметры

*нвидс*<br/>
окне Ширина (в пикселях) текстового поля.

*бинфлоатимоде*<br/>
Значение TRUE, чтобы задать ширину для плавающего режима. Значение FALSE, чтобы задать ширину для обычного режима.

### <a name="remarks"></a>Комментарии

`CMFCRibbonEdit`Элемент управления имеет две ширины в зависимости от режима его просмотра: плавающий режим и обычный режим.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)<br/>
[Класс CMFCRibbonBar](../../mfc/reference/cmfcribbonbar-class.md)
