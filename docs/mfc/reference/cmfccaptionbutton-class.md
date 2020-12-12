---
description: 'Дополнительные сведения о: Кмфккаптионбуттон Class'
title: Класс Кмфккаптионбуттон
ms.date: 11/04/2016
f1_keywords:
- CMFCCaptionButton
- AFXCAPTIONBUTTON/CMFCCaptionButton
- AFXCAPTIONBUTTON/CMFCCaptionButton::CMFCCaptionButton
- AFXCAPTIONBUTTON/CMFCCaptionButton::GetHit
- AFXCAPTIONBUTTON/CMFCCaptionButton::GetIconID
- AFXCAPTIONBUTTON/CMFCCaptionButton::GetRect
- AFXCAPTIONBUTTON/CMFCCaptionButton::GetSize
- AFXCAPTIONBUTTON/CMFCCaptionButton::IsMiniFrameButton
- AFXCAPTIONBUTTON/CMFCCaptionButton::Move
- AFXCAPTIONBUTTON/CMFCCaptionButton::OnDraw
- AFXCAPTIONBUTTON/CMFCCaptionButton::SetMiniFrameButton
helpviewer_keywords:
- CMFCCaptionButton [MFC], CMFCCaptionButton
- CMFCCaptionButton [MFC], GetHit
- CMFCCaptionButton [MFC], GetIconID
- CMFCCaptionButton [MFC], GetRect
- CMFCCaptionButton [MFC], GetSize
- CMFCCaptionButton [MFC], IsMiniFrameButton
- CMFCCaptionButton [MFC], Move
- CMFCCaptionButton [MFC], OnDraw
- CMFCCaptionButton [MFC], SetMiniFrameButton
ms.assetid: c5774b38-c0dd-414a-9ede-3b2f78f233ec
ms.openlocfilehash: 6c3c1cbeea4a548f2951276b3ad43cb598cf22a8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327747"
---
# <a name="cmfccaptionbutton-class"></a>Класс Кмфккаптионбуттон

`CMFCCaptionButton`Класс реализует кнопку, которая отображается в строке заголовка для закрепляемой панели или окна с рамкой. Как правило, платформа создает кнопки заголовка автоматически.

## <a name="syntax"></a>Синтаксис

```
class CMFCCaptionButton : public CObject
```

## <a name="members"></a>Члены

### <a name="constructors"></a>Конструкторы

|Имя|Описание|
|----------|-----------------|
|[Кмфккаптионбуттон:: Кмфккаптионбуттон](#cmfccaptionbutton)|Конструирует объект Кмфккаптионбуттон.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфккаптионбуттон:: Жесит](#gethit)|Возвращает команду, представленную кнопкой.|
|[Кмфккаптионбуттон:: Жетиконид](#geticonid)|Возвращает идентификатор изображения, связанный с кнопкой.|
|[Кмфккаптионбуттон:: коrect](#getrect)|Возвращает прямоугольник, занятый кнопкой.|
|[Кмфккаптионбуттон:: DataSize](#getsize)|Возвращает ширину и высоту кнопки.|
|[Кмфккаптионбуттон:: Исминифрамебуттон](#isminiframebutton)|Указывает, задана ли высота строки заголовка на мини-размер.|
|[Кмфккаптионбуттон:: Move](#move)|Задает положение и состояние окна для кнопки рисования.|
|[Кмфккаптионбуттон:: OnDraw](#ondraw)|Рисует кнопку заголовка.|
|[Кмфккаптионбуттон:: Сетминифрамебуттон](#setminiframebutton)|Задает мини-размер заголовка окна.|

## <a name="remarks"></a>Комментарии

Можно создать производный класс от [класса кпанефрамевнд](../../mfc/reference/cpaneframewnd-class.md) и использовать защищенный метод, `AddButton` , чтобы добавить кнопки заголовка в свернутое окно фрейма.

Кпанефрамевнд. h определяет идентификаторы команд для двух типов кнопок заголовка:

- AFX_CAPTION_BTN_PIN, отображающая кнопку с закреплением, когда область закрепления поддерживает режим автоматического скрытия.

- AFX_CAPTION_BTN_CLOSE, которая отображает кнопку **Закрыть** , когда область может быть закрыта или скрыта.

## <a name="example"></a>Пример

В следующем примере показано, как создать `CMFCCaptionButton` объект и задать свернутый размер заголовка окна.

[!code-cpp[NVC_MFC_RibbonApp#43](../../mfc/reference/codesnippet/cpp/cmfccaptionbutton-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCCaptionButton](../../mfc/reference/cmfccaptionbutton-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкскаптионбуттон. h

## <a name="cmfccaptionbuttoncmfccaptionbutton"></a><a name="cmfccaptionbutton"></a> Кмфккаптионбуттон:: Кмфккаптионбуттон

Формирует объект `CMFCCaptionButton`.

```
CMFCCaptionButton();

CMFCCaptionButton(
    UINT nHit,
    BOOL bLeftAlign = FALSE);
```

### <a name="parameters"></a>Параметры

*нхит*<br/>
окне Команда, связанная с кнопкой.

*блефталигн*<br/>
окне Указывает, выдается ли кнопка по левому краю.

В следующей таблице перечислены возможные значения для параметра *нхит* .

|Значение|Команда|
|-----------|-------------|
|AFX_HTCLOSE|Кнопка "Закрыть".|
|хтминбуттон|Кнопка сворачивания.|
|хтмаксбуттон|Кнопка "развернуть".|
|AFX_HTLEFTBUTTON|Кнопка со стрелкой влево.|
|AFX_HTRIGHTBUTTON|Кнопка со стрелкой вправо.|
|AFX_HTMENU|Кнопка меню со стрелкой вниз.|
|хтновхере|Значение по умолчанию; не представляет команду.|

### <a name="remarks"></a>Комментарии

По умолчанию кнопки заголовков не связаны с командой.

Кнопки заголовка вычисляются либо справа, либо слева.

## <a name="cmfccaptionbuttongethit"></a><a name="gethit"></a> Кмфккаптионбуттон:: Жесит

Возвращает команду, представленную кнопкой.

```
UINT GetHit() const;
```

### <a name="return-value"></a>Возвращаемое значение

Команда, представленная кнопкой.

В следующей таблице перечислены возможные возвращаемые значения.

|Значение|Команда|
|-----------|-------------|
|AFX_HTCLOSE|Кнопка "Закрыть".|
|хтминбуттон|Кнопка сворачивания.|
|хтмаксбуттон|Кнопка "развернуть".|
|AFX_HTLEFTBUTTON|Кнопка со стрелкой влево.|
|AFX_HTRIGHTBUTTON|Кнопка со стрелкой вправо.|
|AFX_HTMENU|Кнопка меню со стрелкой вниз.|
|хтновхере|Значение по умолчанию; не представляет команду.|

## <a name="cmfccaptionbuttongeticonid"></a><a name="geticonid"></a> Кмфккаптионбуттон:: Жетиконид

Возвращает идентификатор изображения, связанный с кнопкой.

```
virtual CMenuImages::IMAGES_IDS GetIconID(
    BOOL bHorz,
    BOOL bMaximized = FALSE) const;
```

### <a name="parameters"></a>Параметры

*бхорз*<br/>
окне Значение TRUE для кодов изображений стрелок Left или right; FALSE для кодов изображений со стрелками вверх или вниз.

*бмаксимизед*<br/>
окне Значение TRUE для максимального идентификатора изображения; Значение FALSE для сворачивания идентификатора образа.

### <a name="return-value"></a>Возвращаемое значение

Идентификатор образа.

### <a name="remarks"></a>Комментарии

Параметры указывают идентификаторы изображений для кнопок "Minimize" или "развернуть заголовок".

## <a name="cmfccaptionbuttongetrect"></a><a name="getrect"></a> Кмфккаптионбуттон:: коrect

Возвращает прямоугольник, занятый кнопкой.

```
virtual CRect GetRect() const;
```

### <a name="return-value"></a>Возвращаемое значение

Прямоугольник, представляющий расположение кнопки.

### <a name="remarks"></a>Комментарии

Если кнопка не отображается, возвращается размер 0.

## <a name="cmfccaptionbuttongetsize"></a><a name="getsize"></a> Кмфккаптионбуттон:: DataSize

Возвращает ширину и высоту кнопки.

```
static CSize GetSize();
```

### <a name="return-value"></a>Возвращаемое значение

Внешние размеры кнопки.

### <a name="remarks"></a>Комментарии

Возвращаемый размер включает поля и границы кнопки.

## <a name="cmfccaptionbuttonisminiframebutton"></a><a name="isminiframebutton"></a> Кмфккаптионбуттон:: Исминифрамебуттон

Указывает, задана ли высота строки заголовка на мини-размер.

```
BOOL IsMiniFrameButton() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если для заголовка задан мини-размер; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

## <a name="cmfccaptionbuttonmove"></a><a name="move"></a> Кмфккаптионбуттон:: Move

Задает положение и состояние окна для кнопки рисования.

```cpp
void Move(
    const CPoint& ptTo,
    BOOL bHide = FALSE);
```

### <a name="parameters"></a>Параметры

*птто*<br/>
окне Новое расположение.

*bHide*<br/>
окне Указывает, следует ли отображать кнопку.

## <a name="cmfccaptionbuttonondraw"></a><a name="ondraw"></a> Кмфккаптионбуттон:: OnDraw

Рисует кнопку заголовка.

```
virtual void OnDraw(
    CDC* pDC,
    BOOL bActive,
    BOOL bHorz = TRUE,
    BOOL bMaximized = TRUE,
    BOOL bDisabled = FALSE);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства для кнопки.

*бактиве*<br/>
окне Следует ли нарисовать изображение активной кнопки.

*бхорз*<br/>
окне Зарезервировано для использования в производном классе.

*бмаксимизед*<br/>
окне Следует ли нарисовать развернутое изображение кнопки.

*бдисаблед*<br/>
окне Следует ли нарисовать изображение кнопки Enabled.

### <a name="remarks"></a>Комментарии

Параметр *бмаксимизед* используется, когда кнопка является кнопкой развертывания или сворачивания.

## <a name="cmfccaptionbuttonsetminiframebutton"></a><a name="setminiframebutton"></a> Кмфккаптионбуттон:: Сетминифрамебуттон

Задает мини-размер заголовка окна.

```cpp
void SetMiniFramebutton(BOOL bSet = TRUE);
```

### <a name="parameters"></a>Параметры

*Управляемое bSet*<br/>
окне TRUE для высоты заголовков свернутого заголовка; Значение FALSE для высоты строки заголовка по умолчанию.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кпанефрамевнд](../../mfc/reference/cpaneframewnd-class.md)<br/>
[Класс CDockablePane](../../mfc/reference/cdockablepane-class.md)
