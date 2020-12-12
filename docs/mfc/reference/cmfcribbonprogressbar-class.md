---
description: 'Дополнительные сведения о: Кмфкриббонпрогрессбар Class'
title: Класс Кмфкриббонпрогрессбар
ms.date: 11/04/2016
f1_keywords:
- CMFCRibbonProgressBar
- AFXRIBBONPROGRESSBAR/CMFCRibbonProgressBar
- AFXRIBBONPROGRESSBAR/CMFCRibbonProgressBar::CMFCRibbonProgressBar
- AFXRIBBONPROGRESSBAR/CMFCRibbonProgressBar::GetPos
- AFXRIBBONPROGRESSBAR/CMFCRibbonProgressBar::GetRangeMax
- AFXRIBBONPROGRESSBAR/CMFCRibbonProgressBar::GetRangeMin
- AFXRIBBONPROGRESSBAR/CMFCRibbonProgressBar::GetRegularSize
- AFXRIBBONPROGRESSBAR/CMFCRibbonProgressBar::IsInfiniteMode
- AFXRIBBONPROGRESSBAR/CMFCRibbonProgressBar::OnDraw
- AFXRIBBONPROGRESSBAR/CMFCRibbonProgressBar::SetInfiniteMode
- AFXRIBBONPROGRESSBAR/CMFCRibbonProgressBar::SetPos
- AFXRIBBONPROGRESSBAR/CMFCRibbonProgressBar::SetRange
helpviewer_keywords:
- CMFCRibbonProgressBar [MFC], CMFCRibbonProgressBar
- CMFCRibbonProgressBar [MFC], GetPos
- CMFCRibbonProgressBar [MFC], GetRangeMax
- CMFCRibbonProgressBar [MFC], GetRangeMin
- CMFCRibbonProgressBar [MFC], GetRegularSize
- CMFCRibbonProgressBar [MFC], IsInfiniteMode
- CMFCRibbonProgressBar [MFC], OnDraw
- CMFCRibbonProgressBar [MFC], SetInfiniteMode
- CMFCRibbonProgressBar [MFC], SetPos
- CMFCRibbonProgressBar [MFC], SetRange
ms.assetid: de3d9f2e-ed59-480e-aa7d-08a33ab36c67
ms.openlocfilehash: b4e91a604386a57aa7cac59294c569635583304c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321765"
---
# <a name="cmfcribbonprogressbar-class"></a>Класс Кмфкриббонпрогрессбар

Реализует элемент управления, который визуально показывает ход выполнения длительных операций.

## <a name="syntax"></a>Синтаксис

```
class CMFCRibbonProgressBar : public CMFCRibbonBaseElement
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонпрогрессбар:: Кмфкриббонпрогрессбар](#cmfcribbonprogressbar)|Создает и инициализирует объект `CMFCRibbonProgressBar`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкриббонпрогрессбар:: Жетпос](#getpos)|Возвращает текущий ход выполнения.|
|[Кмфкриббонпрогрессбар:: Жетранжемакс](#getrangemax)|Возвращает максимальное значение текущего диапазона.|
|[Кмфкриббонпрогрессбар:: Жетранжемин](#getrangemin)|Возвращает минимальное значение текущего диапазона.|
|[Кмфкриббонпрогрессбар:: Жетрегуларсизе](#getregularsize)|Возвращает стандартный размер элемента ленты. (Переопределяет [метод CMFCRibbonBaseElement:: жетрегуларсизе](../../mfc/reference/cmfcribbonbaseelement-class.md#getregularsize).)|
|[Кмфкриббонпрогрессбар:: Исинфинитемоде](#isinfinitemode)|Указывает, работает ли индикатор выполнения в бесконечном режиме.|
|[Кмфкриббонпрогрессбар:: OnDraw](#ondraw)|Вызывается платформой для отрисовки элемента ленты. (Переопределяет [метод CMFCRibbonBaseElement:: OnDraw](../../mfc/reference/cmfcribbonbaseelement-class.md#ondraw).)|
|[Кмфкриббонпрогрессбар:: Сетинфинитемоде](#setinfinitemode)|Задает индикатор выполнения для работы в бесконечном режиме.|
|[Кмфкриббонпрогрессбар:: Сетпос](#setpos)|Задает текущий ход выполнения.|
|[Кмфкриббонпрогрессбар:: SetRange](#setrange)|Задает минимальное и максимальное значения.|

## <a name="remarks"></a>Комментарии

`CMFCRibbonProgressBar`Может использоваться в двух режимах: Regular и Infinite. В обычном режиме индикатор выполнения заполняется слева направо и останавливается при достижении максимального значения. В бесконечном режиме индикатор выполнения многократно заполняется от минимального значения до максимального значения. Вы можете использовать бесконечный режим, чтобы указать, что операция выполняется, но время завершения неизвестно.

## <a name="example"></a>Пример

В приведенном ниже примере демонстрируется использование различных методов класса `CMFCRibbonProgressBar` . В примере показано, как настроить индикатор выполнения для работы в бесконечном режиме (где время завершения операции неизвестно), задать минимальное и максимальное значения индикатора выполнения и установить текущую позицию индикатора выполнения. Этот фрагмент кода является частью [демонстрационного примера MS Office 2007](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_MSOffice2007Demo#11](../../mfc/reference/codesnippet/cpp/cmfcribbonprogressbar-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)

[CMFCRibbonProgressBar](../../mfc/reference/cmfcribbonprogressbar-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксриббонпрогрессбар. h

## <a name="cmfcribbonprogressbarcmfcribbonprogressbar"></a><a name="cmfcribbonprogressbar"></a> Кмфкриббонпрогрессбар:: Кмфкриббонпрогрессбар

Создает и инициализирует объект [кмфкриббонпрогрессбар](../../mfc/reference/cmfcribbonprogressbar-class.md) .

```
CMFCRibbonProgressBar();

CMFCRibbonProgressBar(
    UINT nID,
    int nWidth = 90,
    int nHeight = 22);
```

### <a name="parameters"></a>Параметры

*nID*<br/>
окне Указывает идентификатор команды для индикатора выполнения ленты.

*нвидс*<br/>
окне Задает ширину (в пикселях) индикатора выполнения ленты.

*нхеигхт*<br/>
окне Задает высоту (в пикселях) индикатора выполнения ленты.

## <a name="cmfcribbonprogressbargetpos"></a><a name="getpos"></a> Кмфкриббонпрогрессбар:: Жетпос

Возвращает текущую точку индикатора выполнения.

```
int GetPos () const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение, представляющее текущую точку индикатора выполнения.

### <a name="remarks"></a>Комментарии

Заданный диапазон должен находиться в диапазоне, указанном методом [кмфкриббонпрогрессбар:: SetRange](#setrange) .

## <a name="cmfcribbonprogressbargetrangemax"></a><a name="getrangemax"></a> Кмфкриббонпрогрессбар:: Жетранжемакс

Возвращает текущее максимальное значение индикатора выполнения.

```
int GetRangeMax() const;
```

### <a name="return-value"></a>Возвращаемое значение

Максимальное значение текущего диапазона.

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonprogressbargetrangemin"></a><a name="getrangemin"></a> Кмфкриббонпрогрессбар:: Жетранжемин

Возвращает текущее минимальное значение диапазона индикатора выполнения.

```
int GetRangeMin() const;
```

### <a name="return-value"></a>Возвращаемое значение

Минимальное значение текущего диапазона.

## <a name="cmfcribbonprogressbargetregularsize"></a><a name="getregularsize"></a> Кмфкриббонпрогрессбар:: Жетрегуларсизе

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
virtual CSize GetRegularSize(CDC* pDC);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonprogressbarisinfinitemode"></a><a name="isinfinitemode"></a> Кмфкриббонпрогрессбар:: Исинфинитемоде

Указывает, работает ли индикатор выполнения в бесконечном режиме.

```
BOOL IsInfiniteMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если индикатор выполнения находится в бесконечном режиме; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

В бесконечном режиме индикатор выполнения заполняется несколько раз из минимального значения в максимальное значение. Вы можете использовать бесконечный режим, чтобы указать, что операция выполняется, но время завершения неизвестно.

## <a name="cmfcribbonprogressbarondraw"></a><a name="ondraw"></a> Кмфкриббонпрогрессбар:: OnDraw

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
virtual void OnDraw(CDC* pDC);
```

### <a name="parameters"></a>Параметры

окне *основной контроллер домена*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcribbonprogressbarsetinfinitemode"></a><a name="setinfinitemode"></a> Кмфкриббонпрогрессбар:: Сетинфинитемоде

Задает индикатор выполнения для работы в бесконечном режиме.

```cpp
void SetInfiniteMode(BOOL bSet = TRUE);
```

### <a name="parameters"></a>Параметры

*Управляемое bSet*<br/>
окне Значение TRUE, чтобы указать, что индикатор выполнения находится в бесконечном режиме; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Обычно, если индикатор выполнения находится в бесконечном режиме, он сообщает пользователю о том, что операция выполняется, но время завершения неизвестно. Таким же значением индикатор выполнения заполняется несколько раз из минимального значения в максимальное.

## <a name="cmfcribbonprogressbarsetpos"></a><a name="setpos"></a> Кмфкриббонпрогрессбар:: Сетпос

Задает текущую точку индикатора выполнения.

```cpp
void SetPos(
    int nPos,
    BOOL bRedraw = TRUE);
```

### <a name="parameters"></a>Параметры

*nPos*<br/>
окне Задает расположение, в которое задается индикатор выполнения.

*bRedraw*<br/>
окне Указывает, следует ли перерисовать индикатор выполнения.

### <a name="remarks"></a>Комментарии

Заданный диапазон должен находиться в диапазоне, указанном методом [кмфкриббонпрогрессбар:: SetRange](#setrange) .

## <a name="cmfcribbonprogressbarsetrange"></a><a name="setrange"></a> Кмфкриббонпрогрессбар:: SetRange

Задает минимальное и максимальное значения индикатора выполнения.

```cpp
void SetRange(
    int nMin,
    int nMax);
```

### <a name="parameters"></a>Параметры

*Nмин.*<br/>
окне Задает минимальное значение диапазона.

*Nмакс.*<br/>
окне Задает максимальное значение диапазона.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы определить диапазон индикатора выполнения, задав минимальное и максимальное значения.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс метод CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md)<br/>
[Класс CMFCRibbonBar](../../mfc/reference/cmfcribbonbar-class.md)
