---
description: 'Дополнительные сведения о: Кмфктултипктрл Class'
title: Класс Кмфктултипктрл
ms.date: 11/04/2016
f1_keywords:
- CMFCToolTipCtrl
- AFXTOOLTIPCTRL/CMFCToolTipCtrl
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::GetIconSize
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::GetParams
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::OnDrawBorder
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::OnDrawDescription
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::OnDrawIcon
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::OnDrawLabel
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::OnDrawSeparator
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::OnFillBackground
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::SetDescription
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::SetFixedWidth
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::SetHotRibbonButton
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::SetLocation
- AFXTOOLTIPCTRL/CMFCToolTipCtrl::SetParams
helpviewer_keywords:
- CMFCToolTipCtrl [MFC], GetIconSize
- CMFCToolTipCtrl [MFC], GetParams
- CMFCToolTipCtrl [MFC], OnDrawBorder
- CMFCToolTipCtrl [MFC], OnDrawDescription
- CMFCToolTipCtrl [MFC], OnDrawIcon
- CMFCToolTipCtrl [MFC], OnDrawLabel
- CMFCToolTipCtrl [MFC], OnDrawSeparator
- CMFCToolTipCtrl [MFC], OnFillBackground
- CMFCToolTipCtrl [MFC], SetDescription
- CMFCToolTipCtrl [MFC], SetFixedWidth
- CMFCToolTipCtrl [MFC], SetHotRibbonButton
- CMFCToolTipCtrl [MFC], SetLocation
- CMFCToolTipCtrl [MFC], SetParams
ms.assetid: 9fbfcfb1-a8ab-417f-ae29-9a9ca85ee58f
ms.openlocfilehash: 918a702a94f2847298d86868d35b2bad65b65b33
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331698"
---
# <a name="cmfctooltipctrl-class"></a>Класс Кмфктултипктрл

Расширенная реализация всплывающей подсказки на основе класса [CToolTipCtrl Class](../../mfc/reference/ctooltipctrl-class.md). Подсказка на основе класса `CMFCToolTipCtrl` может отображать значок, метку и описание. Можно настроить его внешний вид с помощью градиентной заливки, пользовательских цветов текста и границы, полужирного шрифта, скругленных углов или стиля всплывающего предупреждения.

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```cpp
class CMFCToolTipCtrl : public CToolTipCtrl
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CMFCToolTipCtrl::CMFCToolTipCtrl`|Конструктор по умолчанию.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCToolTipCtrl::GetIconSize](#geticonsize)|Возвращает размер значка во всплывающей подсказке.|
|[CMFCToolTipCtrl::GetParams](#getparams)|Возвращает параметры отображения всплывающей подсказки.|
|[CMFCToolTipCtrl::OnDrawBorder](#ondrawborder)|Рисует границу всплывающей подсказки.|
|[CMFCToolTipCtrl::OnDrawDescription](#ondrawdescription)||
|[CMFCToolTipCtrl::OnDrawIcon](#ondrawicon)|Отображает значок во всплывающей подсказке.|
|[CMFCToolTipCtrl::OnDrawLabel](#ondrawlabel)|Рисует заголовок всплывающей подсказки или вычисляет размер метки.|
|[CMFCToolTipCtrl::OnDrawSeparator](#ondrawseparator)|Рисует разделитель между меткой и описанием во всплывающей подсказке.|
|[CMFCToolTipCtrl::OnFillBackground](#onfillbackground)|Заливает фон всплывающей подсказки.|
|[CMFCToolTipCtrl::SetDescription](#setdescription)|Задает описание, которое отображается во всплывающей подсказке.|
|[CMFCToolTipCtrl::SetFixedWidth](#setfixedwidth)||
|[CMFCToolTipCtrl::SetHotRibbonButton](#sethotribbonbutton)||
|[CMFCToolTipCtrl::SetLocation](#setlocation)||
|[CMFCToolTipCtrl::SetParams](#setparams)|Задает внешний вид всплывающей подсказки с помощью объекта `CMFCToolTipInfo`.|

## <a name="remarks"></a>Комментарии

Используйте `CMFCToolTipCtrl` `CMFCToolTipInfo` объекты [классов](../../mfc/reference/ctooltipmanager-class.md) , и ктултипманажер для реализации настраиваемых подсказок в приложении.

Например, чтобы реализовать всплывающие подсказки в виде выносок, сделайте следующее:

1. Используйте метод [класса CWinAppEx](../../mfc/reference/cwinappex-class.md) для инициализации диспетчера подсказок в приложении.

2. Создайте структуру `CMFCToolTipInfo`, чтобы задать необходимый стиль оформления:

    ```cpp
    CMFCToolTipInfo params;
    params.m_bBoldLabel = FALSE;
    params.m_bDrawDescription = FALSE;
    params.m_bDrawIcon = FALSE;
    params.m_bRoundedCorners = TRUE;
    params.m_bDrawSeparator = FALSE;
    if (m_bCustomColors)
    {
        params.m_clrFill = RGB (255, 255, 255);
        params.m_clrFillGradient = RGB (228, 228, 240);
        params.m_clrText = RGB (61, 83, 80);
        params.m_clrBorder = RGB (144, 149, 168);

    }
    ```

3. Используйте метод [ктултипманажер:: сеттултиппарамс](../../mfc/reference/ctooltipmanager-class.md#settooltipparams) , чтобы задать визуальный стиль для всех всплывающих подсказок в приложении с помощью стилей, определенных в `CMFCToolTipInfo` объекте.

    ```cpp
    theApp.GetTooltipManager ()->SetTooltipParams (AFX_TOOLTIP_TYPE_ALL,
        RUNTIME_CLASS (CMFCToolTipCtrl), &params);
    ```

Для управления поведением всплывающей подсказки и ее отрисовкой вы также можете получить новый производный класс из класса `CMFCToolTipCtrl`. Чтобы задать новый класс элемента управления "Всплывающая подсказка", используйте метод `CTooltipManager::SetTooltipParams`:

```cpp
myApp.GetTooltipManager ()->SetTooltipParams (AFX_TOOLTIP_TYPE_ALL,
    RUNTIME_CLASS (CMyToolTipCtrl))
```

Чтобы восстановить класс элемента управления "Всплывающая подсказка" по умолчанию и сбросить оформление подсказки на стандартное, укажите значение NULL в классе среды выполнения и параметрах всплывающей подсказки в методе `SetTooltipParams`:

```cpp
theApp.GetTooltipManager ()->SetTooltipParams (AFX_TOOLTIP_TYPE_ALL,
    NULL,
    NULL);
```

## <a name="example"></a>Пример

В следующем примере демонстрируется создание объекта `CMFCToolTipCtrl`, задание описания, отображаемого во всплывающей подсказке, а также задание ширины элемента управления "Всплывающая подсказка".

[!code-cpp[NVC_MFC_RibbonApp#41](../../mfc/reference/codesnippet/cpp/cmfctooltipctrl-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CToolTipCtrl](../../mfc/reference/ctooltipctrl-class.md)

[CMFCToolTipCtrl](../../mfc/reference/cmfctooltipctrl-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкстултипктрл. h

## <a name="cmfctooltipctrlcmfctooltipctrl"></a><a name="cmfctooltipctrl"></a> Кмфктултипктрл:: Кмфктултипктрл

```cpp
CMFCToolTipCtrl(CMFCToolTipInfo* pParams = NULL);
```

### <a name="parameters"></a>Параметры

окне *ппарамс*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfctooltipctrlgeticonsize"></a><a name="geticonsize"></a> Кмфктултипктрл:: Жетиконсизе

Возвращает размер значка во всплывающей подсказке.

```cpp
virtual CSize GetIconSize();
```

### <a name="return-value"></a>Возвращаемое значение

Размер значка в пикселях.

## <a name="cmfctooltipctrlgetparams"></a><a name="getparams"></a> Кмфктултипктрл:: params

Возвращает параметры отображения всплывающей подсказки.

```cpp
const CMFCToolTipInfo& GetParams() const;
```

### <a name="return-value"></a>Возвращаемое значение

Текущие параметры экрана всплывающей подсказки, которые хранятся в объекте [класса кмфктултипинфо](../../mfc/reference/cmfctooltipinfo-class.md) .

## <a name="cmfctooltipctrlondrawborder"></a><a name="ondrawborder"></a> Кмфктултипктрл:: Ондравбордер

Рисует границу всплывающей подсказки.

```cpp
virtual void OnDrawBorder(
    CDC* pDC,
    CRect rect,
    COLORREF clrLine);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*rect*<br/>
окне Ограничивающий прямоугольник подсказки.

*клрлине*<br/>
окне Цвет границы.

### <a name="remarks"></a>Комментарии

Переопределите этот метод в производном классе, чтобы настроить внешний вид границы подсказки.

## <a name="cmfctooltipctrlondrawdescription"></a><a name="ondrawdescription"></a> Кмфктултипктрл:: Ондравдескриптион

```cpp
virtual CSize OnDrawDescription(
    CDC* pDC,
    CRect rect,
    BOOL bCalcOnly);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>
[in] *rect*<br/>
окне *бкалконли*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfctooltipctrlondrawicon"></a><a name="ondrawicon"></a> Кмфктултипктрл:: Ондравикон

Отображает значок во всплывающей подсказке.

```cpp
virtual BOOL OnDrawIcon(
    CDC* pDC,
    CRect rectImage);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*ректимаже*<br/>
окне Координаты значка.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если значок был нарисован. В противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Переопределите этот метод в производном классе, чтобы отобразить пользовательский значок. Необходимо также переопределить [кмфктултипктрл:: жетиконсизе](#geticonsize) , чтобы позволить подсказке правильно вычислить макет текста и описания.

## <a name="cmfctooltipctrlondrawlabel"></a><a name="ondrawlabel"></a> Кмфктултипктрл:: Ондравлабел

Рисует заголовок всплывающей подсказки или вычисляет размер метки.

```cpp
virtual CSize OnDrawLabel(
    CDC* pDC,
    CRect rect,
    BOOL bCalcOnly);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*rect*<br/>
окне Ограничивающий прямоугольник области метки.

*бкалконли*<br/>
окне Если значение равно TRUE, метка не будет отображаться.

### <a name="return-value"></a>Возвращаемое значение

Размер метки в пикселях.

### <a name="remarks"></a>Комментарии

Переопределите этот метод в производном классе, если необходимо настроить внешний вид метки подсказки.

## <a name="cmfctooltipctrlondrawseparator"></a><a name="ondrawseparator"></a> Кмфктултипктрл:: Ондравсепаратор

Рисует разделитель между меткой и описанием во всплывающей подсказке.

```cpp
virtual void OnDrawSeparator(
    CDC* pDC,
    int x1,
    int x2,
    int y);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*x1*<br/>
окне Горизонтальная координата левого конца разделителя.

*штук*<br/>
окне Горизонтальная координата правого конца разделителя.

*да*<br/>
окне Вертикальная координата разделителя.

### <a name="remarks"></a>Комментарии

Реализация по умолчанию рисует строку от точки (x1, y) до точки (x2, y).

Переопределите этот метод в производном классе, чтобы настроить внешний вид разделителя.

## <a name="cmfctooltipctrlonfillbackground"></a><a name="onfillbackground"></a> Кмфктултипктрл:: Онфиллбаккграунд

Заливает фон всплывающей подсказки.

```cpp
virtual void OnFillBackground(
    CDC* pDC,
    CRect rect,
    COLORREF& clrText,
    COLORREF& clrLine);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*rect*<br/>
окне Задает ограничивающий прямоугольник области для заполнения.

*clrText*<br/>
окне Цвет переднего плана подсказки.

*клрлине*<br/>
окне Цвет границ и разделитель между меткой и описанием.

### <a name="remarks"></a>Комментарии

Реализация по умолчанию заполняет прямоугольник, заданный параметром *Rect* , цветом или шаблоном, указанным последним вызовом метода [Кмфктултипктрл:: SetParams](#setparams).

Переопределите этот метод в производном классе, если необходимо настроить внешний вид подсказки.

## <a name="cmfctooltipctrlsetdescription"></a><a name="setdescription"></a> Кмфктултипктрл:: SetDescription

Задает описание, которое отображается во всплывающей подсказке.

```cpp
virtual void SetDescription(const CString strDesrciption);
```

### <a name="parameters"></a>Параметры

*стрдесрЦиптион*<br/>
окне Текст описания.

### <a name="remarks"></a>Комментарии

Текст описания отображается в подсказке под разделителем.

## <a name="cmfctooltipctrlsetfixedwidth"></a><a name="setfixedwidth"></a> Кмфктултипктрл:: Сетфикседвидс

```cpp
void SetFixedWidth(
    int nWidthRegular,
    int nWidthLargeImage);
```

### <a name="parameters"></a>Параметры

окне *нвидсрегулар*<br/>
окне *нвидсларжеимаже*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfctooltipctrlsethotribbonbutton"></a><a name="sethotribbonbutton"></a> Кмфктултипктрл:: Сесотриббонбуттон

```cpp
void SetHotRibbonButton(CMFCRibbonButton* pRibbonButton);
```

### <a name="parameters"></a>Параметры

окне *приббонбуттон*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfctooltipctrlsetlocation"></a><a name="setlocation"></a> Кмфктултипктрл:: SetLocation

```cpp
void SetLocation(CPoint pt);
```

### <a name="parameters"></a>Параметры

окне *пт*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfctooltipctrlsetparams"></a><a name="setparams"></a> Кмфктултипктрл:: SetParams

Задает внешний вид всплывающей подсказки с помощью объекта [класса кмфктултипинфо](../../mfc/reference/cmfctooltipinfo-class.md) .

```cpp
void SetParams(CMFCToolTipInfo* pParams);
```

### <a name="parameters"></a>Параметры

*ппарамс*<br/>
окне Указатель на объект [класса кмфктултипинфо](../../mfc/reference/cmfctooltipinfo-class.md) , который содержит параметры вывода.

### <a name="remarks"></a>Комментарии

При отображении подсказки она рисуется с помощью цветов и визуальных стилей, которые *ппарамс* указывает. Значение *ппарамс* хранится в защищенном члене `m_Params` , доступ к которому может осуществляться производным классом, который переопределяет [кмфктултипктрл:: ондравбордер](#ondrawborder), [кмфктултипктрл:: ондравикон](#ondrawicon), [Кмфктултипктрл:: ондравлабел](#ondrawlabel), [CMFCToolTipCtrl:: OnDrawSeparator](#ondrawseparator)или [CMFCToolTipCtrl:: OnFillBackground](#onfillbackground) для поддержки указанного внешнего вида.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CToolTipCtrl](../../mfc/reference/ctooltipctrl-class.md)<br/>
[Класс Ктултипманажер](../../mfc/reference/ctooltipmanager-class.md)<br/>
[Класс Кмфктултипинфо](../../mfc/reference/cmfctooltipinfo-class.md)<br/>
[Класс CWinAppEx](../../mfc/reference/cwinappex-class.md)
