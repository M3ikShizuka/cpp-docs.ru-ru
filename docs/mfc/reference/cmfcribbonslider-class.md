---
description: 'Дополнительные сведения о: Кмфкриббонслидер Class'
title: Класс Кмфкриббонслидер
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonSlider
- AFXRIBBONSLIDER/CMFCRibbonSlider
- AFXRIBBONSLIDER/CMFCRibbonSlider::CMFCRibbonSlider
- AFXRIBBONSLIDER/CMFCRibbonSlider::GetPos
- AFXRIBBONSLIDER/CMFCRibbonSlider::GetRangeMax
- AFXRIBBONSLIDER/CMFCRibbonSlider::GetRangeMin
- AFXRIBBONSLIDER/CMFCRibbonSlider::GetRegularSize
- AFXRIBBONSLIDER/CMFCRibbonSlider::GetZoomIncrement
- AFXRIBBONSLIDER/CMFCRibbonSlider::HasZoomButtons
- AFXRIBBONSLIDER/CMFCRibbonSlider::OnDraw
- AFXRIBBONSLIDER/CMFCRibbonSlider::SetPos
- AFXRIBBONSLIDER/CMFCRibbonSlider::SetRange
- AFXRIBBONSLIDER/CMFCRibbonSlider::SetZoomButtons
- AFXRIBBONSLIDER/CMFCRibbonSlider::SetZoomIncrement
helpviewer_keywords:
- CMFCRibbonSlider [MFC], CMFCRibbonSlider
- CMFCRibbonSlider [MFC], GetPos
- CMFCRibbonSlider [MFC], GetRangeMax
- CMFCRibbonSlider [MFC], GetRangeMin
- CMFCRibbonSlider [MFC], GetRegularSize
- CMFCRibbonSlider [MFC], GetZoomIncrement
- CMFCRibbonSlider [MFC], HasZoomButtons
- CMFCRibbonSlider [MFC], OnDraw
- CMFCRibbonSlider [MFC], SetPos
- CMFCRibbonSlider [MFC], SetRange
- CMFCRibbonSlider [MFC], SetZoomButtons
- CMFCRibbonSlider [MFC], SetZoomIncrement
ms.assetid: 9351ac34-f234-4e42-91e2-763f1989c8ff
ms.openlocfilehash: d125afdf961d97c0501742acdc75d7802c7e104d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321738"
---
# <a name="cmfcribbonslider-class"></a>Класс Кмфкриббонслидер

`CMFCRibbonSlider`Класс реализует элемент управления "ползунок", который можно добавить на панель ленты или в строку состояния ленты. Элемент управления "ползунок" ленты напоминает ползунки масштаба, отображаемые в приложениях Office 2007.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonSlider : public CMFCRibbonBaseElement
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонслидер:: Кмфкриббонслидер](#cmfcribbonslider)|Создает и инициализирует элемент управления "ползунок" ленты.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонслидер:: Жетпос](#getpos)|Возвращает текущую положение элемента управления "ползунок".|
|[Кмфкриббонслидер:: Жетранжемакс](#getrangemax)|Возвращает максимальное значение ползунка.|
|[Кмфкриббонслидер:: Жетранжемин](#getrangemin)|Возвращает минимальное значение ползунка.|
|[Кмфкриббонслидер:: Жетрегуларсизе](#getregularsize)|Возвращает стандартный размер элемента ленты. (Переопределяет [метод CMFCRibbonBaseElement:: жетрегуларсизе](../../mfc/reference/cmfcribbonbaseelement-class.md#getregularsize).)|
|[Кмфкриббонслидер:: Жетзуминкремент](#getzoomincrement)|Возвращает размер увеличения масштаба для элемента управления "ползунок".|
|[Кмфкриббонслидер:: Хасзумбуттонс](#haszoombuttons)|Указывает, имеет ли ползунок кнопки масштабирования.|
|[Кмфкриббонслидер:: OnDraw](#ondraw)|Вызывается платформой для отрисовки элемента ленты. (Переопределяет [метод CMFCRibbonBaseElement:: OnDraw](../../mfc/reference/cmfcribbonbaseelement-class.md#ondraw).)|
|[Кмфкриббонслидер:: Сетпос](#setpos)|Задает текущую положение элемента управления "ползунок".|
|[Кмфкриббонслидер:: SetRange](#setrange)|Задает диапазон элемента управления ползунка, устанавливая минимальное и максимальное значения.|
|[Кмфкриббонслидер:: Сетзумбуттонс](#setzoombuttons)|Показывает или скрывает кнопки масштабирования.|
|[Кмфкриббонслидер:: Сетзуминкремент](#setzoomincrement)|Задает размер увеличения масштаба для элемента управления "ползунок".|

## <a name="remarks"></a>Комментарии

С помощью метода можно `SetRange` настроить диапазон увеличения масштаба для ползунка. Текущее положение ползунка можно задать с помощью `SetPos` метода.

Кнопки с циклическим масштабом можно отобразить в левой и правой части ползунка с помощью `SetZoomButtons` метода. По умолчанию ползунок является горизонтальным, кнопка масштаба слева отображает знак «минус», а для кнопки «Масштаб вправо» отображается знак «плюс».

`SetZoomIncrement`Метод определяет шаг приращения, который добавляется к текущему положению или вычитается из него, когда пользователь нажимает кнопку ZOOM.

## <a name="example"></a>Пример

В следующем примере показано, как использовать различные методы в `CMFCRibbonSlider` классе для задания свойств ползунка. В примере показано, как создать `CMFCRibbonSlider` объект, отобразить кнопки масштабирования, задать текущую положение элемента управления Slider и задать диапазон значений для элемента управления "ползунок".

[!code-cpp[NVC_MFC_RibbonApp#12](../../mfc/reference/codesnippet/cpp/cmfcribbonslider-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)

[CMFCRibbonSlider](../../mfc/reference/cmfcribbonslider-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонслидер. h

## <a name="cmfcribbonslidercmfcribbonslider"></a><a name="cmfcribbonslider"></a> Кмфкриббонслидер:: Кмфкриббонслидер

Создайте ползунок ленты.

```
CMFCRibbonSlider(
    UINT nID,
    int nWidth=100);
```

### <a name="parameters"></a>Параметры

*nID*<br/>
окне Идентификатор ползунка.

[in]. *нвидс* Ширина ползунка в пикселях.

### <a name="remarks"></a>Комментарии

Конструирует ползунок ленты, который в категории панели, где добавлен ползунок, имеет ширину *нвидс* пикселей. По умолчанию ползунок является горизонтальным.

## <a name="cmfcribbonslidergetpos"></a><a name="getpos"></a> Кмфкриббонслидер:: Жетпос

Возвращает текущую положение элемента управления "ползунок".

```
int GetPos() const;
```

### <a name="return-value"></a>Возвращаемое значение

Текущее положение элемента управления "ползунок", который является позицией относительно начала ползунка.

## <a name="cmfcribbonslidergetrangemax"></a><a name="getrangemax"></a> Кмфкриббонслидер:: Жетранжемакс

Получает максимальный шаг ползунка, который может перемещаться ползунком на элемент управления "ползунок".

```
int GetRangeMax() const;
```

### <a name="return-value"></a>Возвращаемое значение

Максимальный шаг ползунка, который может перемещаться с помощью ползунка, на элемент управления Slider.

## <a name="cmfcribbonslidergetrangemin"></a><a name="getrangemin"></a> Кмфкриббонслидер:: Жетранжемин

Возвращает минимальное приращение, которое ползунок может перемещать на элемент управления Slider.

```
int GetRangeMin() const;
```

### <a name="return-value"></a>Возвращаемое значение

Минимальное приращение, которое может перемещаться с помощью ползунка на элемент управления Slider.

## <a name="cmfcribbonslidergetregularsize"></a><a name="getregularsize"></a> Кмфкриббонслидер:: Жетрегуларсизе

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
virtual CSize GetRegularSize(CDC* pDC);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonslidergetzoomincrement"></a><a name="getzoomincrement"></a> Кмфкриббонслидер:: Жетзуминкремент

Получите шаг увеличения масштаба для элемента управления "ползунок".

```
int GetZoomIncrement() const;
```

### <a name="return-value"></a>Возвращаемое значение

Увеличение масштаба для элемента управления "ползунок".

## <a name="cmfcribbonsliderhaszoombuttons"></a><a name="haszoombuttons"></a> Кмфкриббонслидер:: Хасзумбуттонс

Указывает, имеет ли ползунок кнопки масштабирования.

```
BOOL HasZoomButtons() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если ползунок имеет кнопки масштабирования; В противном случае — значение FALSE.

## <a name="cmfcribbonsliderondraw"></a><a name="ondraw"></a> Кмфкриббонслидер:: OnDraw

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
virtual void OnDraw(CDC* pDC);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonslidersetpos"></a><a name="setpos"></a> Кмфкриббонслидер:: Сетпос

Задает текущую положение элемента управления "ползунок".

```cpp
void SetPos(
    int nPos,
    BOOL bRedraw=TRUE);
```

### <a name="parameters"></a>Параметры

*nPos*<br/>
окне Задает положение, устанавливаемое для ползунка. Позиция относительно начала ползунка.

*bRedraw*<br/>
окне Если значение равно TRUE, ползунок будет перерисован.

## <a name="cmfcribbonslidersetrange"></a><a name="setrange"></a> Кмфкриббонслидер:: SetRange

Задайте диапазон значений для элемента управления "ползунок".

```cpp
void SetRange(
    int nMin,
    int nMax);
```

### <a name="parameters"></a>Параметры

*Nмин.*<br/>
окне Задает минимальное значение элемента управления "ползунок".

*Nмакс.*<br/>
окне Задает максимальное значение элемента управления "ползунок".

### <a name="remarks"></a>Комментарии

Задает диапазон значений для элемента управления "ползунок", устанавливая минимальное и максимальное значения.

## <a name="cmfcribbonslidersetzoombuttons"></a><a name="setzoombuttons"></a> Кмфкриббонслидер:: Сетзумбуттонс

Отображение или скрытие кнопок масштабирования.

```cpp
void SetZoomButtons(BOOL bSet=TRUE);
```

### <a name="parameters"></a>Параметры

[in]. *управляемое bSet* Значение TRUE для вывода кнопок масштабирования; Значение FALSE, чтобы скрыть их.

## <a name="cmfcribbonslidersetzoomincrement"></a><a name="setzoomincrement"></a> Кмфкриббонслидер:: Сетзуминкремент

Задайте шаг увеличения масштаба для элемента управления "ползунок".

```cpp
void SetZoomIncrement(int nZoomIncrement);
```

### <a name="parameters"></a>Параметры

*нзуминкремент*<br/>
окне Задает шаг масштабирования элемента управления ползунка.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс метод CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)
