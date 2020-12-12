---
description: 'Дополнительные сведения о: Кмфкколорпиккерктрл Class'
title: Класс Кмфкколорпиккерктрл
ms.date: 11/19/2018
f1_keywords:
- CMFCColorPickerCtrl
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::CMFCColorPickerCtrl
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::GetColor
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::GetHLS
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::GetHue
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::GetLuminance
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::GetSaturation
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::SelectCellHexagon
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::SetColor
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::SetHLS
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::SetHue
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::SetLuminance
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::SetLuminanceBarWidth
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::SetOriginalColor
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::SetPalette
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::SetSaturation
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::SetType
- AFXCOLORPICKERCTRL/CMFCColorPickerCtrl::DrawCursor
helpviewer_keywords:
- CMFCColorPickerCtrl [MFC], CMFCColorPickerCtrl
- CMFCColorPickerCtrl [MFC], GetColor
- CMFCColorPickerCtrl [MFC], GetHLS
- CMFCColorPickerCtrl [MFC], GetHue
- CMFCColorPickerCtrl [MFC], GetLuminance
- CMFCColorPickerCtrl [MFC], GetSaturation
- CMFCColorPickerCtrl [MFC], SelectCellHexagon
- CMFCColorPickerCtrl [MFC], SetColor
- CMFCColorPickerCtrl [MFC], SetHLS
- CMFCColorPickerCtrl [MFC], SetHue
- CMFCColorPickerCtrl [MFC], SetLuminance
- CMFCColorPickerCtrl [MFC], SetLuminanceBarWidth
- CMFCColorPickerCtrl [MFC], SetOriginalColor
- CMFCColorPickerCtrl [MFC], SetPalette
- CMFCColorPickerCtrl [MFC], SetSaturation
- CMFCColorPickerCtrl [MFC], SetType
- CMFCColorPickerCtrl [MFC], DrawCursor
ms.assetid: b9bbd03c-beb0-4b55-9765-9985fd05e5dc
ms.openlocfilehash: e4363c08af86dee96df1492e9a029414d9902435
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97313077"
---
# <a name="cmfccolorpickerctrl-class"></a>Класс Кмфкколорпиккерктрл

`CMFCColorPickerCtrl`Класс предоставляет функциональные возможности для элемента управления, используемого для выбора цветов.

## <a name="syntax"></a>Синтаксис

```
class CMFCColorPickerCtrl : public CButton
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкколорпиккерктрл:: Кмфкколорпиккерктрл](#cmfccolorpickerctrl)|Формирует объект `CMFCColorPickerCtrl`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкколорпиккерктрл:: "Color"](#getcolor)|Извлекает цвет, выбираемый пользователем.|
|[Кмфкколорпиккерктрл:: Жеслс](#gethls)|Извлекает значения оттенка, яркости и насыщенности цвета, выбираемого пользователем.|
|[Кмфкколорпиккерктрл:: Жесуе](#gethue)|Извлекает компонент оттенка цвета, который выбирает пользователь.|
|[Кмфкколорпиккерктрл:: "светимость"](#getluminance)|Извлекает компонент освещенности цвета, выбираемого пользователем.|
|[Кмфкколорпиккерктрл:: обесцветить](#getsaturation)|Извлекает компонент насыщенности цвета, выбираемого пользователем.|
|[Кмфкколорпиккерктрл:: Селектцеллхексагон](#selectcellhexagon)|Устанавливает текущий цвет в цвет, определяемый заданными компонентами цвета RGB или заданной ячейкой шестиугольника.|
|[Кмфкколорпиккерктрл:: Сетколор](#setcolor)|Устанавливает текущий цвет в указанное значение цвета RGB.|
|[Кмфкколорпиккерктрл:: Сеслс](#sethls)|Устанавливает текущий цвет в указанное значение цвета HLS.|
|[Кмфкколорпиккерктрл:: Сесуе](#sethue)|Изменяет компонент оттенка текущего выбранного цвета.|
|[Кмфкколорпиккерктрл:: Сетлуминанце](#setluminance)|Изменяет компонент светимости текущего выбранного цвета.|
|[Кмфкколорпиккерктрл:: Сетлуминанцебарвидс](#setluminancebarwidth)|Задает ширину панели освещенности в элементе управления "Выбор цвета".|
|[Кмфкколорпиккерктрл:: Сеторигиналколор](#setoriginalcolor)|Задает первоначальный выбранный цвет.|
|[Кмфкколорпиккерктрл:: Сетпалетте](#setpalette)|Задает текущую цветовую палитру.|
|[Кмфкколорпиккерктрл:: Сетсатуратион](#setsaturation)|Изменяет компонент насыщенности выбранного в данный момент цвета.|
|[Кмфкколорпиккерктрл:: Сеттипе](#settype)|Задает тип элемента управления "Выбор цвета" для вывода.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Кмфкколорпиккерктрл::D Равкурсор](#drawcursor)|Вызвано структурой перед отображением курсора, указывающего на выбранный цвет.|

## <a name="remarks"></a>Комментарии

Стандартные цвета выбираются из цветовой палитры шестиугольника, а пользовательские цвета выбираются из панели освещенности, в которой цвета задаются с помощью красной/зеленой/синей нотации или нотации оттенка, сатуаратиона и светимости.

На следующем рисунке показаны несколько `CMFCColorPickerCtrl` объектов.

![Диалоговое окно для CMFCColorPickerCtrl](../../mfc/reference/media/colorpicker.png "Диалоговое окно для CMFCColorPickerCtrl")

`CMFCColorPickerCtrl`Поддерживает две пары стилей. Стили HEX и HEX_GREYSCALE подходят для выбора стандартного цвета. Стили выбора и СВЕТИМОСТи подходят для выбора пользовательского цвета.

Чтобы включить `CMFCColorPickerCtrl` элемент управления в диалоговое окно, выполните следующие действия.

1. При использовании **ClassWizard** Вставьте новый элемент управления "Кнопка" в шаблон диалогового окна (поскольку `CMFCColorPickerCtrl` класс наследуется от `CButton` класса).

1. Вставьте переменную-член, связанную с новым элементом управления "Кнопка", в класс диалогового окна. Затем измените тип переменной с `CButton` на `CMFCColorPickerCtrl` .

1. Вставьте `WM_INITDIALOG` обработчик сообщений для класса диалогового окна. В обработчике задайте тип, палитру и исходный выбранный цвет `CMFCColorPickerCtrl` элемента управления.

## <a name="example"></a>Пример

В следующем примере показано, как настроить `CMFCColorPickerCtrl` объект с помощью различных методов в `CMFCColorPickerCtrl` классе. В примере показано, как задать тип элемента управления выборки и задать его цвет, оттенок, светимость и насыщенность. Пример является частью [примера новых элементов управления](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_NewControls#4](../../mfc/reference/codesnippet/cpp/cmfccolorpickerctrl-class_1.h)]
[!code-cpp[NVC_MFC_NewControls#5](../../mfc/reference/codesnippet/cpp/cmfccolorpickerctrl-class_2.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CButton](../../mfc/reference/cbutton-class.md)

[CMFCColorPickerCtrl](../../mfc/reference/cmfccolorpickerctrl-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксколорпиккерктрл. h

## <a name="cmfccolorpickerctrlcmfccolorpickerctrl"></a><a name="cmfccolorpickerctrl"></a> Кмфкколорпиккерктрл:: Кмфкколорпиккерктрл

Формирует объект `CMFCColorPickerCtrl`.

```
CMFCColorPickerCtrl();
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfccolorpickerctrldrawcursor"></a><a name="drawcursor"></a> Кмфкколорпиккерктрл::D Равкурсор

Вызвано структурой перед отображением курсора, указывающего на выбранный цвет.

```
virtual void DrawCursor(
    CDC* pDC,
    const CRect& rect);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*rect*<br/>
окне Задает прямоугольную область вокруг выбранного цвета.

### <a name="remarks"></a>Комментарии

Переопределите этот метод, если необходимо изменить форму курсора, указывающую на выбранный цвет.

## <a name="cmfccolorpickerctrlgetcolor"></a><a name="getcolor"></a> Кмфкколорпиккерктрл:: "Color"

Извлекает цвет, выбираемый пользователем.

```
COLORREF GetColor() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение RGB выбранного цвета.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolorpickerctrlgethls"></a><a name="gethls"></a> Кмфкколорпиккерктрл:: Жеслс

Извлекает значения оттенка, яркости и насыщенности цвета, выбираемого пользователем.

```cpp
void GetHLS(
    double* hue,
    double* luminance,
    double* saturation);
```

### <a name="parameters"></a>Параметры

*цвет*<br/>
заполняет Указатель на переменную типа Double, получающую сведения о оттенках.

*яркостью*<br/>
заполняет Указатель на переменную типа Double, получающую сведения о освещенности.

*насыщенность*<br/>
заполняет Указатель на переменную типа Double, которая получает сведения о насыщенности.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolorpickerctrlgethue"></a><a name="gethue"></a> Кмфкколорпиккерктрл:: Жесуе

Извлекает компонент оттенка цвета, который выбирает пользователь.

```
double GetHue() const;
```

### <a name="return-value"></a>Возвращаемое значение

Компонент оттенка выбранного цвета.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolorpickerctrlgetluminance"></a><a name="getluminance"></a> Кмфкколорпиккерктрл:: "светимость"

Извлекает компонент освещенности цвета, выбираемого пользователем.

```
double GetLuminance() const;
```

### <a name="return-value"></a>Возвращаемое значение

Компонент светимости выбранного цвета.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolorpickerctrlgetsaturation"></a><a name="getsaturation"></a> Кмфкколорпиккерктрл:: обесцветить

Извлекает значение насыщенности цвета, выбираемого пользователем.

```
double GetSaturation() const;
```

### <a name="return-value"></a>Возвращаемое значение

Компонент насыщенности выбранного цвета.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolorpickerctrlselectcellhexagon"></a><a name="selectcellhexagon"></a> Кмфкколорпиккерктрл:: Селектцеллхексагон

Устанавливает текущий цвет в цвет, определяемый заданными компонентами цвета RGB или заданной ячейкой шестиугольника.

```cpp
void SelectCellHexagon(
    BYTE R,
    BYTE G,
    BYTE B);

BOOL SelectCellHexagon(
    int x,
    int y);
```

### <a name="parameters"></a>Параметры

*R*<br/>
окне Компонент красного цвета.

*Модуле*<br/>
окне Компонент зеленого цвета.

*B*<br/>
окне Компонент синего цвета.

*x*<br/>
окне Координата x курсора, указывающая на ячейку шестиугольника.

*y*<br/>
окне Координата y курсора, указывающая на ячейку шестиугольника.

### <a name="return-value"></a>Возвращаемое значение

Вторая перегрузка этого метода всегда возвращает значение FALSE.

### <a name="remarks"></a>Комментарии

Первая перегрузка этого метода устанавливает текущий цвет в цвет, соответствующий заданным цветным компонентам элемента управления "Выбор цвета" красного, зеленого и синего цветов.

Вторая перегрузка этого метода устанавливает текущий цвет в цвет ячейки шестиугольника, на которую указывает указанное положение курсора.

## <a name="cmfccolorpickerctrlsetcolor"></a><a name="setcolor"></a> Кмфкколорпиккерктрл:: Сетколор

Устанавливает текущий цвет в указанное значение цвета RGB.

```cpp
void SetColor(COLORREF Color);
```

### <a name="parameters"></a>Параметры

*Цвет*<br/>
окне Значение цвета RGB.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolorpickerctrlsethls"></a><a name="sethls"></a> Кмфкколорпиккерктрл:: Сеслс

Устанавливает текущий цвет в указанное значение цвета HLS.

```cpp
void SetHLS(
    double hue,
    double luminance,
    double saturation,
    BOOL bInvalidate=TRUE);
```

### <a name="parameters"></a>Параметры

*цвет*<br/>
окне Значение оттенка.

*яркостью*<br/>
окне Значение светимости.

*насыщенность*<br/>
окне Значение насыщенности.

*бинвалидате*<br/>
окне Значение TRUE, чтобы принудительно обновить окно до нового цвета; в противном случае — значение FALSE. Значение по умолчанию — TRUE.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolorpickerctrlsethue"></a><a name="sethue"></a> Кмфкколорпиккерктрл:: Сесуе

Изменяет цветовой тон выбранного в данный момент цвета.

```cpp
void SetHue(double Hue);
```

### <a name="parameters"></a>Параметры

*Hue*<br/>
окне Значение оттенка.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolorpickerctrlsetluminance"></a><a name="setluminance"></a> Кмфкколорпиккерктрл:: Сетлуминанце

Изменяет светимость выбранного в данный момент цвета.

```cpp
void SetLuminance(double Luminance);
```

### <a name="parameters"></a>Параметры

*Освещенность*<br/>
окне Значение светимости.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolorpickerctrlsetluminancebarwidth"></a><a name="setluminancebarwidth"></a> Кмфкколорпиккерктрл:: Сетлуминанцебарвидс

Задает ширину панели освещенности в элементе управления "Выбор цвета".

```cpp
void SetLuminanceBarWidth(int w);
```

### <a name="parameters"></a>Параметры

*w*<br/>
окне Ширина индикатора освещенности в пикселях.

### <a name="remarks"></a>Комментарии

Этот метод используется для изменения размера панели освещенности, которая находится на вкладке **Пользовательская** вкладка элемента управления выбор цвета. Параметр *w* задает новую ширину панели освещенности. Значение Width игнорируется, если оно превышает три четверти значения ширины клиентской области.

## <a name="cmfccolorpickerctrlsetoriginalcolor"></a><a name="setoriginalcolor"></a> Кмфкколорпиккерктрл:: Сеторигиналколор

Задает первоначальный выбранный цвет.

```cpp
void SetOriginalColor(COLORREF ref);
```

### <a name="parameters"></a>Параметры

*ref*<br/>
окне Значение цвета RGB.

### <a name="remarks"></a>Комментарии

Вызывайте этот метод при инициализации элемента управления "Выбор цвета".

## <a name="cmfccolorpickerctrlsetpalette"></a><a name="setpalette"></a> Кмфкколорпиккерктрл:: Сетпалетте

Задает текущую цветовую палитру.

```cpp
void SetPalette(CPalette* pPalette);
```

### <a name="parameters"></a>Параметры

*ппалетте*<br/>
окне Указатель на цветовую палитру.

### <a name="remarks"></a>Комментарии

Цветовая палитра определяет массив цветов, представленных в элементе управления "Выбор цвета".

## <a name="cmfccolorpickerctrlsetsaturation"></a><a name="setsaturation"></a> Кмфкколорпиккерктрл:: Сетсатуратион

Изменяет насыщенность выбранного в данный момент цвета.

```cpp
void SetSaturation(double Saturation);
```

### <a name="parameters"></a>Параметры

*Насыщенность*<br/>
окне Значение насыщенности.

### <a name="remarks"></a>Комментарии

## <a name="cmfccolorpickerctrlsettype"></a><a name="settype"></a> Кмфкколорпиккерктрл:: Сеттипе

Задает тип элемента управления "Выбор цвета" для вывода.

```cpp
void SetType(COLORTYPE colorType);
```

### <a name="parameters"></a>Параметры

*колортипе*<br/>
окне Тип элемента управления "Выбор цвета".

Типы определяются `CMFCColorPickerCtrl::COLORTYPE` перечислением. Возможные типы: СВЕТИМОСТь, средство выбора, HEX и HEX_GREYSCALE. Тип по умолчанию — "средство выбора".

### <a name="remarks"></a>Комментарии

Чтобы задать тип элемента управления "Выбор цвета", вызовите этот метод перед созданием элемента управления Windows.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкколордиалог](../../mfc/reference/cmfccolordialog-class.md)
