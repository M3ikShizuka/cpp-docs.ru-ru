---
description: 'Дополнительные сведения о: Кмфчеадерктрл Class'
title: CMFCHeaderCtrl Class
ms.date: 11/04/2016
f1_keywords:
- CMFCHeaderCtrl
- AFXHEADERCTRL/CMFCHeaderCtrl
- AFXHEADERCTRL/CMFCHeaderCtrl::CMFCHeaderCtrl
- AFXHEADERCTRL/CMFCHeaderCtrl::EnableMultipleSort
- AFXHEADERCTRL/CMFCHeaderCtrl::GetColumnState
- AFXHEADERCTRL/CMFCHeaderCtrl::GetSortColumn
- AFXHEADERCTRL/CMFCHeaderCtrl::IsAscending
- AFXHEADERCTRL/CMFCHeaderCtrl::IsDialogControl
- AFXHEADERCTRL/CMFCHeaderCtrl::IsMultipleSort
- AFXHEADERCTRL/CMFCHeaderCtrl::RemoveSortColumn
- AFXHEADERCTRL/CMFCHeaderCtrl::SetSortColumn
- AFXHEADERCTRL/CMFCHeaderCtrl::OnDrawItem
- AFXHEADERCTRL/CMFCHeaderCtrl::OnDrawSortArrow
- AFXHEADERCTRL/CMFCHeaderCtrl::OnFillBackground
helpviewer_keywords:
- CMFCHeaderCtrl [MFC], CMFCHeaderCtrl
- CMFCHeaderCtrl [MFC], EnableMultipleSort
- CMFCHeaderCtrl [MFC], GetColumnState
- CMFCHeaderCtrl [MFC], GetSortColumn
- CMFCHeaderCtrl [MFC], IsAscending
- CMFCHeaderCtrl [MFC], IsDialogControl
- CMFCHeaderCtrl [MFC], IsMultipleSort
- CMFCHeaderCtrl [MFC], RemoveSortColumn
- CMFCHeaderCtrl [MFC], SetSortColumn
- CMFCHeaderCtrl [MFC], OnDrawItem
- CMFCHeaderCtrl [MFC], OnDrawSortArrow
- CMFCHeaderCtrl [MFC], OnFillBackground
ms.assetid: 2f5fbf7b-5c75-42db-9216-640b1628f777
ms.openlocfilehash: a6be476e095dc4a013705657e259a90d7cafe0d4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97265380"
---
# <a name="cmfcheaderctrl-class"></a>CMFCHeaderCtrl Class

`CMFCHeaderCtrl`Класс поддерживает сортировку нескольких столбцов в элементе управления "заголовок".

## <a name="syntax"></a>Синтаксис

```
class CMFCHeaderCtrl : public CHeaderCtrl
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфчеадерктрл:: Кмфчеадерктрл](#cmfcheaderctrl)|Формирует объект `CMFCHeaderCtrl`.|
|`CMFCHeaderCtrl::~CMFCHeaderCtrl`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфчеадерктрл:: Енаблемултиплесорт](#enablemultiplesort)|Включает или отключает режим *сортировки нескольких столбцов* для текущего элемента управления "заголовок".|
|[Кмфчеадерктрл:: Жетколумнстате](#getcolumnstate)|Указывает, что столбец не отсортирован или сортируется в порядке возрастания или убывания.|
|[Кмфчеадерктрл:: Жетсортколумн](#getsortcolumn)|Возвращает отсчитываемый от нуля индекс первого отсортированного столбца в элементе управления "заголовок".|
|`CMFCHeaderCtrl::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|
|[Кмфчеадерктрл:: по возрастанию](#isascending)|Указывает, сортируется ли любой столбец в элементе управления "заголовок" в возрастающем порядке.|
|[Кмфчеадерктрл:: Исдиалогконтрол](#isdialogcontrol)|Указывает, является ли родительское окно текущего элемента управления "заголовок" диалоговым окном.|
|[Кмфчеадерктрл:: Исмултиплесорт](#ismultiplesort)|Указывает, находится ли текущий элемент управления "заголовок" в режиме *сортировки нескольких столбцов* .|
|[Кмфчеадерктрл:: Ремовесортколумн](#removesortcolumn)|Удаляет указанный столбец из списка столбцов сортировки.|
|[Кмфчеадерктрл:: Сетсортколумн](#setsortcolumn)|Задает порядок сортировки указанного столбца в элементе управления "заголовок".|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Кмфчеадерктрл:: Ондравитем](#ondrawitem)|Вызывается платформой для рисования столбца элемента управления заголовка.|
|[Кмфчеадерктрл:: Ондравсортарров](#ondrawsortarrow)|Вызывается структурой для рисования стрелки сортировки.|
|[Кмфчеадерктрл:: Онфиллбаккграунд](#onfillbackground)|Вызывается платформой для заполнения фона столбца элемента управления заголовка.|

## <a name="example"></a>Пример

В следующем примере показано, как создать объект `CMFCHeaderCtrl` класса и как включить режим *сортировки с несколькими столбцами* для элемента управления "текущий заголовок".

[!code-cpp[NVC_MFC_RibbonApp#24](../../mfc/reference/codesnippet/cpp/cmfcheaderctrl-class_1.cpp)]

## <a name="remarks"></a>Комментарии

`CMFCHeaderCtrl`Класс рисует стрелку сортировки в столбце элемента управления заголовков, чтобы указать, что столбец сортируется. Используйте режим *сортировки с несколькими столбцами* , если набор столбцов в элементе управления "родительский список" ( [класс кмфклистктрл](../../mfc/reference/cmfclistctrl-class.md)) можно сортировать одновременно.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CHeaderCtrl](../../mfc/reference/cheaderctrl-class.md)

[CMFCHeaderCtrl](../../mfc/reference/cmfcheaderctrl-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксхеадерктрл. h

## <a name="cmfcheaderctrlcmfcheaderctrl"></a><a name="cmfcheaderctrl"></a> Кмфчеадерктрл:: Кмфчеадерктрл

Формирует объект `CMFCHeaderCtrl`.

```
CMFCHeaderCtrl::CMFCHeaderCtrl()
```

### <a name="remarks"></a>Комментарии

Этот конструктор инициализирует следующие переменные члена для указанных значений:

|Переменная-член|Значение|
|---------------------|-----------|
|`m_bIsMousePressed`|FALSE|
|`m_bMultipleSort`|FALSE|
|`m_bAscending`|true|
|`m_nHighlightedItem`|-1|
|`m_bTracked`|FALSE|
|`m_bIsDlgControl`|FALSE|
|`m_hFont`|NULL|

## <a name="cmfcheaderctrlenablemultiplesort"></a><a name="enablemultiplesort"></a> Кмфчеадерктрл:: Енаблемултиплесорт

Включает или отключает режим *сортировки нескольких столбцов* для текущего элемента управления "заголовок".

```cpp
void EnableMultipleSort(BOOL bEnable=TRUE);
```

### <a name="parameters"></a>Параметры

*bEnable*<br/>
окне Значение TRUE, чтобы включить режим сортировки нескольких столбцов; Значение FALSE, чтобы отключить режим сортировки нескольких столбцов и удалить все столбцы из списка отсортированных столбцов. Значение по умолчанию — TRUE.

### <a name="remarks"></a>Комментарии

Этот метод используется для включения или отключения режима сортировки нескольких столбцов. Два или более столбца могут участвовать в сортировке, если элемент управления "заголовок" находится в режиме сортировки с несколькими столбцами.

## <a name="cmfcheaderctrlgetcolumnstate"></a><a name="getcolumnstate"></a> Кмфчеадерктрл:: Жетколумнстате

Указывает, является ли столбец несортированным или сортируется в порядке возрастания или убывания.

```
int GetColumnState(int iColumn) const;
```

### <a name="parameters"></a>Параметры

*иколумн*<br/>
окне Отсчитываемый от нуля индекс столбца.

### <a name="return-value"></a>Возвращаемое значение

Значение, указывающее состояние сортировки указанного столбца. В следующем списке указаны возможные значения.

|Значение|Описание|
|-----------|-----------------|
|-1|Отсортировано в порядке убывания.|
|0|Не отсортировано.|
|1|Отсортировано в порядке возрастания.|

### <a name="remarks"></a>Комментарии

## <a name="cmfcheaderctrlgetsortcolumn"></a><a name="getsortcolumn"></a> Кмфчеадерктрл:: Жетсортколумн

Возвращает отсчитываемый от нуля индекс первого отсортированного столбца в элементе управления "заголовок".

```
int GetSortColumn() const;
```

### <a name="return-value"></a>Возвращаемое значение

Индекс отсортированного столбца или значение-1, если столбец не найден.

### <a name="remarks"></a>Комментарии

Если элемент управления "заголовок" находится в режиме *сортировки нескольких столбцов* и приложение было скомпилировано в режиме отладки, этот метод утверждает и рекомендует использовать вместо этого метод [Кмфчеадерктрл:: жетколумнстате](#getcolumnstate) . Если элемент управления "заголовок" находится в режиме сортировки нескольких столбцов и приложение было скомпилировано в розничном режиме, этот метод возвращает значение-1.

## <a name="cmfcheaderctrlisascending"></a><a name="isascending"></a> Кмфчеадерктрл:: по возрастанию

Указывает, сортируется ли любой столбец в элементе управления "заголовок" в возрастающем порядке.

```
BOOL IsAscending() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если любой столбец в элементе управления "заголовок" сортируется в возрастающем порядке; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Значение, возвращаемое этим методом, используется для вывода стрелки сортировки соответствующей позиции элемента управления заголовка. Чтобы задать порядок сортировки, используйте метод [кмфчеадерктрл:: сетсортколумн](#setsortcolumn) .

## <a name="cmfcheaderctrlisdialogcontrol"></a><a name="isdialogcontrol"></a> Кмфчеадерктрл:: Исдиалогконтрол

Указывает, является ли родительское окно текущего элемента управления "заголовок" диалоговым окном.

```
BOOL IsDialogControl() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если родительское окно текущего элемента управления "заголовок" является диалоговым. в противном случае — значение FALSE.

## <a name="cmfcheaderctrlismultiplesort"></a><a name="ismultiplesort"></a> Кмфчеадерктрл:: Исмултиплесорт

Указывает, находится ли текущий элемент управления "заголовок" в режиме *сортировки нескольких столбцов* .

```
BOOL IsMultipleSort() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если включен режим сортировки нескольких столбцов; в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Используйте метод [кмфчеадерктрл:: енаблемултиплесорт](#enablemultiplesort) , чтобы включить или отключить режим сортировки нескольких столбцов. Два или более столбца могут участвовать в сортировке, если элемент управления "заголовок" находится в режиме сортировки с несколькими столбцами.

## <a name="cmfcheaderctrlondrawitem"></a><a name="ondrawitem"></a> Кмфчеадерктрл:: Ондравитем

Вызывается платформой для рисования столбца элемента управления заголовка.

```
virtual void OnDrawItem(
    CDC* pDC,
    int iItem,
    CRect rect,
    BOOL bIsPressed,
    BOOL bIsHighlighted);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*iItem*<br/>
окне Отсчитываемый от нуля индекс рисуемого элемента.

*rect*<br/>
окне Ограничивающий прямоугольник рисуемого элемента.

*биспрессед*<br/>
окне Значение TRUE, чтобы нарисовать элемент в состоянии нажатия; в противном случае — значение FALSE.

*бишигхлигхтед*<br/>
окне Значение TRUE, чтобы нарисовать элемент в выделенном состоянии; в противном случае — значение FALSE.

## <a name="cmfcheaderctrlondrawsortarrow"></a><a name="ondrawsortarrow"></a> Кмфчеадерктрл:: Ондравсортарров

Вызывается структурой для рисования стрелки сортировки.

```
virtual void OnDrawSortArrow(
    CDC* pDC,
    CRect rectArrow);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

*ректарров*<br/>
окне Ограничивающий прямоугольник со стрелкой сортировки.

## <a name="cmfcheaderctrlonfillbackground"></a><a name="onfillbackground"></a> Кмфчеадерктрл:: Онфиллбаккграунд

Вызывается платформой для заполнения фона столбца элемента управления заголовка.

```
virtual void OnFillBackground(CDC* pDC);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
окне Указатель на контекст устройства.

### <a name="remarks"></a>Комментарии

## <a name="cmfcheaderctrlremovesortcolumn"></a><a name="removesortcolumn"></a> Кмфчеадерктрл:: Ремовесортколумн

Удаляет указанный столбец из списка столбцов сортировки.

```cpp
void RemoveSortColumn(int iColumn);
```

### <a name="parameters"></a>Параметры

*иколумн*<br/>
окне Отсчитываемый от нуля индекс удаляемого столбца.

## <a name="cmfcheaderctrlsetsortcolumn"></a><a name="setsortcolumn"></a> Кмфчеадерктрл:: Сетсортколумн

Задает порядок сортировки указанного столбца в элементе управления "заголовок".

```cpp
void SetSortColumn(
    int iColumn,
    BOOL bAscending=TRUE,
    BOOL bAdd=FALSE);
```

### <a name="parameters"></a>Параметры

*иколумн*<br/>
окне Отсчитываемый от нуля индекс столбца элемента управления "заголовок". Если этот параметр меньше нуля, этот метод удаляет все столбцы из списка столбцов сортировки.

*басцендинг*<br/>
окне Задает порядок сортировки столбца, который указывает параметр *иколумн* . Значение TRUE, чтобы задать порядок по возрастанию; Значение FALSE, чтобы задать порядок по убыванию. Значение по умолчанию — TRUE.

*бадд*<br/>
окне Значение TRUE, чтобы задать порядок сортировки столбца, заданного параметром *иколумн* .

Если текущий элемент управления "заголовок" находится в режиме *сортировки с несколькими столбцами* , этот метод добавляет указанный столбец в список столбцов сортировки. Используйте [кмфчеадерктрл:: енаблемултиплесорт](#enablemultiplesort) для задания режима сортировки нескольких столбцов.

Если режим сортировки нескольких столбцов не задан и этот метод компилируется в режиме отладки, этот метод утверждает. Если режим сортировки нескольких столбцов не установлен и этот метод компилируется в розничном режиме, этот метод сначала удаляет все столбцы из списка столбцов сортировки, а затем добавляет указанный столбец в список.

Значение FALSE, чтобы сначала удалить все столбцы из списка столбцов сортировки, а затем добавить указанный столбец в список. Значение по умолчанию — FALSE.

### <a name="remarks"></a>Комментарии

Этот метод используется для задания порядка сортировки столбца. При необходимости этот метод добавляет столбец в список столбцов сортировки. Элемент управления "заголовок" использует порядок сортировки для рисования стрелки сортировки, которая указывает вверх или вниз.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфклистктрл](../../mfc/reference/cmfclistctrl-class.md)
