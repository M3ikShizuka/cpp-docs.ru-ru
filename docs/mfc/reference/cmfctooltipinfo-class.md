---
description: 'Дополнительные сведения о: Кмфктултипинфо Class'
title: Класс Кмфктултипинфо
ms.date: 11/04/2016
f1_keywords:
- CMFCToolTipInfo
- AFXTOOLTIPCTRL/CMFCToolTipInfo
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_bBalloonTooltip
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_bBoldLabel
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_bDrawDescription
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_bDrawIcon
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_bDrawSeparator
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_bRoundedCorners
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_bVislManagerTheme
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_clrBorder
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_clrFill
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_clrFillGradient
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_clrText
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_nGradientAngle
- AFXTOOLTIPCTRL/CMFCToolTipInfo::m_nMaxDescrWidth
helpviewer_keywords:
- CMFCToolTipInfo [MFC], m_bBalloonTooltip
- CMFCToolTipInfo [MFC], m_bBoldLabel
- CMFCToolTipInfo [MFC], m_bDrawDescription
- CMFCToolTipInfo [MFC], m_bDrawIcon
- CMFCToolTipInfo [MFC], m_bDrawSeparator
- CMFCToolTipInfo [MFC], m_bRoundedCorners
- CMFCToolTipInfo [MFC], m_bVislManagerTheme
- CMFCToolTipInfo [MFC], m_clrBorder
- CMFCToolTipInfo [MFC], m_clrFill
- CMFCToolTipInfo [MFC], m_clrFillGradient
- CMFCToolTipInfo [MFC], m_clrText
- CMFCToolTipInfo [MFC], m_nGradientAngle
- CMFCToolTipInfo [MFC], m_nMaxDescrWidth
ms.assetid: f9d3d7f8-1f08-4342-a7b2-683860e5d2a5
ms.openlocfilehash: 06ceca500ad92d5f3a27e2740a298d9c1bbfe1cc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97143433"
---
# <a name="cmfctooltipinfo-class"></a>Класс Кмфктултипинфо

Хранит сведения о внешнем виде подсказок.

## <a name="syntax"></a>Синтаксис

```
class CMFCToolTipInfo
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCToolTipInfo::operator=](#operator_eq)||

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|[Кмфктултипинфо:: m_bBalloonTooltip](#m_bballoontooltip)|Логическая переменная, указывающая, имеет ли всплывающая подсказка вид выноски.|
|[CMFCToolTipInfo::m_bBoldLabel](#m_bboldlabel)|Логическая переменная, указывающая, выделяются ли заголовки всплывающих подсказок жирным шрифтом.|
|[CMFCToolTipInfo::m_bDrawDescription](#m_bdrawdescription)|Логическая переменная, указывающая, содержит ли всплывающая подсказка описание.|
|[CMFCToolTipInfo::m_bDrawIcon](#m_bdrawicon)|Логическая переменная, указывающая, содержит ли всплывающая подсказка значок.|
|[CMFCToolTipInfo::m_bDrawSeparator](#m_bdrawseparator)|Логическая переменная, указывающая, имеется ли разделитель между заголовком всплывающей подсказки и описанием.|
|[CMFCToolTipInfo::m_bRoundedCorners](#m_broundedcorners)|Логическая переменная, указывающая, закруглены ли углы всплывающей подсказки.|
|[CMFCToolTipInfo::m_bVislManagerTheme](#m_bvislmanagertheme)|Логическая переменная, указывающая, должен ли внешний вид подсказки контролироваться визуальным диспетчером (см. раздел [Класс CMFCVisualManager](../../mfc/reference/cmfcvisualmanager-class.md)).|
|[CMFCToolTipInfo::m_clrBorder](#m_clrborder)|Цвет границы всплывающей подсказки.|
|[CMFCToolTipInfo::m_clrFill](#m_clrfill)|Цвет фона всплывающей подсказки.|
|[CMFCToolTipInfo::m_clrFillGradient](#m_clrfillgradient)|Цвет градиентной заливки всплывающей подсказки.|
|[CMFCToolTipInfo::m_clrText](#m_clrtext)|Цвет текста всплывающей подсказки.|
|[CMFCToolTipInfo::m_nGradientAngle](#m_ngradientangle)|Угол градиентной заливки всплывающей подсказки.|
|[CMFCToolTipInfo::m_nMaxDescrWidth](#m_nmaxdescrwidth)|Максимальная возможная ширина описания во всплывающей подсказке (в пикселях).|

## <a name="remarks"></a>Комментарии

Используйте класс [кмфктултипктрл](../../mfc/reference/cmfctooltipctrl-class.md), `CMFCToolTipInfo` и [класс ктултипманажер](../../mfc/reference/ctooltipmanager-class.md) для реализации пользовательских подсказок в приложении. Пример использования этих классов подсказок см. в разделе [класс кмфктултипктрл](../../mfc/reference/cmfctooltipctrl-class.md) .

## <a name="example"></a>Пример

В следующем примере демонстрируется задание значений разных переменных-членов класса `CMFCToolTipInfo`.

[!code-cpp[NVC_MFC_RibbonApp#42](../../mfc/reference/codesnippet/cpp/cmfctooltipinfo-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CMFCToolTipInfo](../../mfc/reference/cmfctooltipinfo-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкстултипктрл. h

## <a name="cmfctooltipinfom_bballoontooltip"></a><a name="m_bballoontooltip"></a> Кмфктултипинфо:: m_bBalloonTooltip

Задает отображаемый стиль всех подсказок.

```
BOOL m_bBalloonTooltip;
```

### <a name="remarks"></a>Комментарии

Значение TRUE указывает, что всплывающие подсказки используют стиль подсказок, значение FALSE указывает, что в подсказках используется прямоугольный стиль.

## <a name="cmfctooltipinfom_bboldlabel"></a><a name="m_bboldlabel"></a> Кмфктултипинфо:: m_bBoldLabel

Указывает, является ли шрифт текста подсказки полужирным.

```
BOOL m_bBoldLabel;
```

### <a name="remarks"></a>Комментарии

Задайте для этого элемента значение TRUE, чтобы текст подсказки отображался полужирным шрифтом, или FALSE, чтобы отображать метки всплывающих подсказок со шрифтами, отличными от полужирного.

## <a name="cmfctooltipinfom_bdrawdescription"></a><a name="m_bdrawdescription"></a> Кмфктултипинфо:: m_bDrawDescription

Указывает, отображается ли текст описания в каждой подсказке.

```
BOOL m_bDrawDescription;
```

### <a name="remarks"></a>Комментарии

Присвойте этому элементу значение TRUE, чтобы отобразить описание, или FALSE, чтобы скрыть описание. Вы можете указать описание всплывающей подсказки, вызвав [кмфктултипктрл:: SetDescription.](../../mfc/reference/cmfctooltipctrl-class.md#setdescription)

## <a name="cmfctooltipinfom_bdrawicon"></a><a name="m_bdrawicon"></a> Кмфктултипинфо:: m_bDrawIcon

Указывает, отображаются ли значки во всех подсказках.

```
BOOL m_bDrawIcon;
```

### <a name="remarks"></a>Комментарии

Присвойте этому элементу значение TRUE, чтобы отображать значок в каждой подсказке, или FALSE для вывода всплывающих подсказок без значков.

## <a name="cmfctooltipinfom_bdrawseparator"></a><a name="m_bdrawseparator"></a> Кмфктултипинфо:: m_bDrawSeparator

Указывает, содержит ли каждая подсказка разделитель между меткой и ее описанием.

```
BOOL m_bDrawSeparator;
```

### <a name="remarks"></a>Комментарии

Присвойте этому элементу значение TRUE, чтобы отображать разделитель между меткой и описанием подсказки, или FALSE для вывода всплывающих подсказок без разделителя.

## <a name="cmfctooltipinfom_broundedcorners"></a><a name="m_broundedcorners"></a> Кмфктултипинфо:: m_bRoundedCorners

Указывает, имеют ли все подсказки скругленные углы.

```
BOOL m_bRoundedCorners;
```

### <a name="remarks"></a>Комментарии

Присвойте этому элементу значение TRUE, чтобы отображать скругленные углы во всплывающих подсказках, или FALSE для вывода прямоугольных углов на всплывающих подсказках.

## <a name="cmfctooltipinfom_clrborder"></a><a name="m_clrborder"></a> Кмфктултипинфо:: m_clrBorder

Задает цвет границ для всех подсказок.

```
COLORREF m_clrBorder;
```

## <a name="cmfctooltipinfom_clrfill"></a><a name="m_clrfill"></a> Кмфктултипинфо:: m_clrFill

Задает цвет фона всплывающей подсказки.

```
COLORREF m_clrFill;
```

### <a name="remarks"></a>Комментарии

Если [кмфктултипинфо:: m_clrFillGradient](#m_clrfillgradient) равно-1, цвет фона подсказки — `m_clrFill` . В противном случае `m_clrFill` задает цвет начала градиента и `m_clrFillGradient` задает цвет конца градиента. [Кмфктултипинфо:: m_nGradientAngle](#m_ngradientangle) определяет направление градиента.

## <a name="cmfctooltipinfom_clrfillgradient"></a><a name="m_clrfillgradient"></a> Кмфктултипинфо:: m_clrFillGradient

Задает конечный цвет для фона градиента для подсказок.

```
COLORREF m_clrFillGradient;
```

### <a name="remarks"></a>Комментарии

Если `m_clrFillGradient` равно-1, градиент отсутствует. В противном случае начальный цвет градиента задается [кмфктултипинфо:: m_clrFill](#m_clrfill) , а цвет завершения градиента задается параметром `m_clrFillGradient` . [Кмфктултипинфо:: m_nGradientAngle](#m_ngradientangle) определяет направление градиента.

## <a name="cmfctooltipinfom_clrtext"></a><a name="m_clrtext"></a> Кмфктултипинфо:: m_clrText

Задает цвет текста всех подсказок.

```
COLORREF m_clrText;
```

## <a name="cmfctooltipinfom_ngradientangle"></a><a name="m_ngradientangle"></a> Кмфктултипинфо:: m_nGradientAngle

Указывает угол, на котором градиент рисуется на фоне всплывающих подсказок.

```
int m_nGradientAngle;
```

### <a name="remarks"></a>Комментарии

`m_nGradientAngle` Задает угол (в градусах) смещения градиента на фоне подсказок по горизонтали. Если `m_nGradientAngle` значение равно 0, градиент рисуется слева направо. Если `m_nGradientAngle` имеет значение от 1 до 360, градиент вращается по часовой стрелке на это число градусов. Если `m_nGradientAngle` равно-1, то есть значение по умолчанию, градиент строится сверху вниз. Это то же самое, что и значение `m_nGradientAngle` 90.

[Кмфктултипинфо:: m_clrFill](#m_clrfill) `clrFill` Задает цвет начала градиента и [кмфктултипинфо:: m_clrFillGradient](#m_clrfillgradient) `clrFillGradient` задает цвет конца градиента. Если `m_clrFillGradient` равно-1, градиент отсутствует.

## <a name="cmfctooltipinfom_nmaxdescrwidth"></a><a name="m_nmaxdescrwidth"></a> Кмфктултипинфо:: m_nMaxDescrWidth

Задает максимальную ширину описания, отображаемого в каждой подсказке. Если ширина описания превышает указанное значение, текст упаковывается.

```
int m_nMaxDescrWidth;
```

## <a name="cmfctooltipinfom_bvislmanagertheme"></a><a name="m_bvislmanagertheme"></a> Кмфктултипинфо:: m_bVislManagerTheme

Указывает, управляет ли визуальный диспетчер приложения внешним видом всех всплывающих подсказок.

```
BOOL m_bVislManagerTheme;
```

### <a name="remarks"></a>Комментарии

Если `m_bVislManagerTheme` имеет значение true, каждая подсказка запрашивает новый [кмфктултипинфо](../../mfc/reference/cmfctooltipinfo-class.md) из визуального диспетчера приложения, прежде чем они появятся на экране, и использует значения в этом объекте для определения их внешнего вида. Другие члены [кмфктултипинфо](../../mfc/reference/cmfctooltipinfo-class.md) игнорируются.

## <a name="cmfctooltipinfooperator"></a><a name="operator_eq"></a> Кмфктултипинфо:: operator =

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
CMFCToolTipInfo& operator=(CMFCToolTipInfo& src);
```

### <a name="parameters"></a>Параметры

окне *src*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Ктултипманажер](../../mfc/reference/ctooltipmanager-class.md)<br/>
[Класс Кмфктултипктрл](../../mfc/reference/cmfctooltipctrl-class.md)
