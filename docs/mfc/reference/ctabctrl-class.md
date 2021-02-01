---
title: Класс CTabCtrl
description: 'Дополнительные сведения о: CTabCtrl Class'
ms.date: 1/29/2021
f1_keywords:
- CTabCtrl
- AFXCMN/CTabCtrl
- AFXCMN/CTabCtrl::CTabCtrl
- AFXCMN/CTabCtrl::AdjustRect
- AFXCMN/CTabCtrl::Create
- AFXCMN/CTabCtrl::CreateEx
- AFXCMN/CTabCtrl::DeleteAllItems
- AFXCMN/CTabCtrl::DeleteItem
- AFXCMN/CTabCtrl::DeselectAll
- AFXCMN/CTabCtrl::DrawItem
- AFXCMN/CTabCtrl::GetCurFocus
- AFXCMN/CTabCtrl::GetCurSel
- AFXCMN/CTabCtrl::GetExtendedStyle
- AFXCMN/CTabCtrl::GetImageList
- AFXCMN/CTabCtrl::GetItem
- AFXCMN/CTabCtrl::GetItemCount
- AFXCMN/CTabCtrl::GetItemRect
- AFXCMN/CTabCtrl::GetItemState
- AFXCMN/CTabCtrl::GetRowCount
- AFXCMN/CTabCtrl::GetToolTips
- AFXCMN/CTabCtrl::HighlightItem
- AFXCMN/CTabCtrl::HitTest
- AFXCMN/CTabCtrl::InsertItem
- AFXCMN/CTabCtrl::RemoveImage
- AFXCMN/CTabCtrl::SetCurFocus
- AFXCMN/CTabCtrl::SetCurSel
- AFXCMN/CTabCtrl::SetExtendedStyle
- AFXCMN/CTabCtrl::SetImageList
- AFXCMN/CTabCtrl::SetItem
- AFXCMN/CTabCtrl::SetItemExtra
- AFXCMN/CTabCtrl::SetItemSize
- AFXCMN/CTabCtrl::SetItemState
- AFXCMN/CTabCtrl::SetMinTabWidth
- AFXCMN/CTabCtrl::SetPadding
- AFXCMN/CTabCtrl::SetToolTips
helpviewer_keywords:
- CTabCtrl [MFC], CTabCtrl
- CTabCtrl [MFC], AdjustRect
- CTabCtrl [MFC], Create
- CTabCtrl [MFC], CreateEx
- CTabCtrl [MFC], DeleteAllItems
- CTabCtrl [MFC], DeleteItem
- CTabCtrl [MFC], DeselectAll
- CTabCtrl [MFC], DrawItem
- CTabCtrl [MFC], GetCurFocus
- CTabCtrl [MFC], GetCurSel
- CTabCtrl [MFC], GetExtendedStyle
- CTabCtrl [MFC], GetImageList
- CTabCtrl [MFC], GetItem
- CTabCtrl [MFC], GetItemCount
- CTabCtrl [MFC], GetItemRect
- CTabCtrl [MFC], GetItemState
- CTabCtrl [MFC], GetRowCount
- CTabCtrl [MFC], GetToolTips
- CTabCtrl [MFC], HighlightItem
- CTabCtrl [MFC], HitTest
- CTabCtrl [MFC], InsertItem
- CTabCtrl [MFC], RemoveImage
- CTabCtrl [MFC], SetCurFocus
- CTabCtrl [MFC], SetCurSel
- CTabCtrl [MFC], SetExtendedStyle
- CTabCtrl [MFC], SetImageList
- CTabCtrl [MFC], SetItem
- CTabCtrl [MFC], SetItemExtra
- CTabCtrl [MFC], SetItemSize
- CTabCtrl [MFC], SetItemState
- CTabCtrl [MFC], SetMinTabWidth
- CTabCtrl [MFC], SetPadding
- CTabCtrl [MFC], SetToolTips
ms.openlocfilehash: 31056e452973432f9f9a6d453de8c413c9b60463
ms.sourcegitcommit: beac3ddf1a20de5e836569ae07407d5f3703f536
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2021
ms.locfileid: "99224490"
---
# <a name="ctabctrl-class"></a>Класс `CTabCtrl`

Предоставляет функциональные возможности стандартного элемента управления "вкладка" Windows.

## <a name="syntax"></a>Синтаксис

```cpp
class CTabCtrl : public CWnd
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|Имя|Описание|
|----------|-----------------|
|[`CTabCtrl::CTabCtrl`](#ctabctrl) | Формирует объект `CTabCtrl`.|


### <a name="public-methods"></a>Открытые методы

|name  |Описание  |
|---------|---------|
|[`CTabCtrl::AdjustRect`](#adjustrect) | Вычисляет область просмотра элемента управления вкладки по заданному прямоугольнику окна или вычисляет прямоугольник окна, который соответствует заданной области экрана. |
|[`CTabCtrl::Create`](#create) | Создает элемент управления "Вкладка" и присоединяет его к экземпляру `TabCtrl` объекта  |
|[`CTabCtrl::CreateEx`](#createex) | Создает элемент управления "Вкладка" с указанными расширенными стилями Windows и присоединяет его к экземпляру объекта CTabCtrl.|
|[`CTabCtrl::DeleteAllItems`](#deleteallitems) | Удаляет все элементы из элемента управления "Вкладка".|
|[`CTabCtrl::DeleteItem`](#deleteitem) | Удаляет элемент из элемента управления "Вкладка".|
|[`CTabCtrl::DeselectAll`](#deselectall) | Сбрасывает элементы в элементе управления "Вкладка" и очищает все нажатые клавиши.|
|[`CTabCtrl::DrawItem`](#drawitem) | Рисует указанный элемент элемента управления "Вкладка".|
|[`CTabCtrl::GetCurFocus`](#getcurfocus) | Извлекает вкладку с текущим фокусом элемента управления "Вкладка".|
|[`CTabCtrl::GetCurSel`](#getcursel) | Определяет текущую выбранную вкладку в элементе управления "Вкладка".|
|[`CTabCtrl::GetExtendedStyle`](#getextendedstyle) | Извлекает расширенные стили, используемые в данный момент для элемента управления "Вкладка".|
|[`CTabCtrl::GetImageList`](#getimagelist) | Извлекает список изображений, связанных с элементом управления "Вкладка".|
|[`CTabCtrl::GetItem`](#getitem) | Извлекает сведения о вкладке в элементе управления "Вкладка".|
|[`CTabCtrl::GetItemCount`](#getitemcount) | Извлекает число вкладок в наборе вкладок.|
|[`CTabCtrl::GetItemRect`](#getitemrect) | Извлекает ограничивающий прямоугольник для вкладки в элементе управления "Вкладка".|
|[`CTabCtrl::GetItemState`](#getitemstate) | Получает состояние указанного элемента управления вкладки.|
|[`CTabCtrl::GetRowCount`](#getrowcount) | Извлекает текущее число строк вкладок в элементе управления "Вкладка".|
|[`CTabCtrl::GetToolTips`](#gettooltips) | Извлекает маркер элемента управления "Подсказка", связанный с элементом управления "Вкладка".|
|[`CTabCtrl::HighlightItem`](#highlightitem) | Задает состояние выделения элемента вкладки.|
|[`CTabCtrl::HitTest`](#hittest) | Определяет, какая вкладка, если она есть, находится на заданной позиции экрана.|
|[`CTabCtrl::InsertItem`](#insertitem) | Вставляет новую вкладку в элемент управления "Вкладка".|
|[`CTabCtrl::RemoveImage`](#removeimage) | Удаляет изображение из списка изображений элемента управления "Вкладка".|
|[`CTabCtrl::SetCurFocus`](#setcurfocus) | Устанавливает фокус на указанную вкладку в элементе управления "Вкладка".|
|[`CTabCtrl::SetCurSel`](#setcursel) | Выбирает вкладку в элементе управления "Вкладка".|
|[`CTabCtrl::SetExtendedStyle`](#setextendedstyle) | Задает расширенные стили для элемента управления "Вкладка".|
|[`CTabCtrl::SetImageList`](#setimagelist) | Присваивает список изображений элементу управления "Вкладка".|
|[`CTabCtrl::SetItem`](#setitem) | Задает некоторые или все атрибуты вкладки.|
|[`CTabCtrl::SetItemExtra`](#setitemextra) | Задает число байтов на вкладку, зарезервированную для определяемых приложением данных в элементе управления "Вкладка".|
|[`CTabCtrl::SetItemSize`](#setitemsize) | Задает ширину и высоту элемента.|
|[`CTabCtrl::SetItemState`](#setitemstate) | Задает состояние указанного элемента управления вкладки.|
|[`CTabCtrl::SetMinTabWidth`](#setmintabwidth) | Устанавливает минимальную ширину элементов в элементе управления "Вкладка".|
|[`CTabCtrl::SetPadding`](#setpadding) | Задает объем пространства (заполнение) вокруг значка вкладок и метки в элементе управления "Вкладка".|
|[`CTabCtrl::SetToolTips`](#settooltips) | Назначает элемент управления «Подсказка» для элемента управления Tab.|

## <a name="remarks"></a>Remarks

Элемент управления "Вкладка" аналогичен разделителям в записной книжке или меткам в CAB-файле. С помощью элемента управления "Вкладка" приложение может определить несколько страниц для одной области окна или диалогового окна. Каждая страница состоит из набора сведений или группы элементов управления, которые отображаются в приложении, когда пользователь выбирает соответствующую вкладку. Специальный тип элемента управления "Вкладка" отображает вкладки, которые выглядят как кнопки. Нажатие кнопки должна сразу же выполнить команду вместо отображения страницы.

Этот элемент управления (и, следовательно, `CTabCtrl` класс) доступен только для программ, работающих под управлением windows 95/98 и Windows NT версии 3,51 и более поздних версий.

Дополнительные сведения о см `CTabCtrl` . в разделе [элементы управления](../../mfc/controls-mfc.md) и [использование `CTabCtrl` ](../../mfc/using-ctabctrl.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[`CObject`](../../mfc/reference/cobject-class.md)\
[`CCmdTarget`](../../mfc/reference/ccmdtarget-class.md)\
[`CWnd`](../../mfc/reference/cwnd-class.md)

`CTabCtrl`

## <a name="requirements"></a>Требования

**Заголовок:**`afxcmn.h`

## <a name="adjustrect"></a>`CTabCtrl::AdjustRect`

Вычисляет область просмотра элемента управления вкладки по заданному прямоугольнику окна или вычисляет прямоугольник окна, который соответствует заданной области экрана.

```cpp
void AdjustRect(BOOL bLarger,   LPRECT lpRect);
```

### <a name="parameters"></a>Параметры

*`bLarger`*\
Указывает, какую операцию следует выполнить. Если этот параметр имеет значение `TRUE` , то *`lpRect`* задает отображаемый прямоугольник и получает соответствующий прямоугольник окна. Если этот параметр имеет значение `FALSE` , то *`lpRect`* задает прямоугольник окна и получает соответствующий отображаемый прямоугольник.

*`lpRect`*\
Указатель на [`RECT`](/windows/win32/api/windef/ns-windef-rect) структуру, которая задает заданный прямоугольник и получает вычисляемый прямоугольник.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFC_CTabCtrl#1](../../mfc/reference/codesnippet/cpp/ctabctrl-class_1.cpp)]

## <a name="ctabctrlcreate"></a><a name="create"></a> `CTabCtrl::Create`

Создает элемент управления "Вкладка" и присоединяет его к экземпляру `CTabCtrl` объекта.

```cpp
virtual BOOL Create(
    DWORD dwStyle,
    const RECT& rect,
    CWnd* pParentWnd,
    UINT nID);
```

### <a name="parameters"></a>Параметры

*`dwStyle`*\
Задает стиль элемента управления Tab. Примените любое сочетание [стилей элементов управления Tab](/windows/win32/Controls/tab-control-styles), описанное в Windows SDK. См. раздел **Примечания** для списка стилей окна, которые также можно применить к элементу управления.

*`rect`*\
Задает размер и позицию элемента управления "Вкладка". Это может быть либо [`CRect`](../../atl-mfc-shared/reference/crect-class.md) объект, либо [`RECT`](/windows/win32/api/windef/ns-windef-rect) структура.

*`pParentWnd`*\
Задает родительское окно элемента управления вкладки, обычно `CDialog` . Оно не должно иметь значение NULL.

*`nID`*\
Задает идентификатор элемента управления вкладки.

### <a name="return-value"></a>Возвращаемое значение

`TRUE` значение, если инициализация объекта выполнена успешно. в противном случае — значение `FALSE` .

### <a name="remarks"></a>Remarks

`CTabCtrl`Объект создается в два этапа. Сначала вызовите конструктор, а затем вызовите метод `Create` , который создает элемент управления "Вкладка" и присоединяет его к `CTabCtrl` объекту.

В дополнение к стилям элемента управления "Вкладка" к элементу управления "Вкладка" можно применить следующие стили окна:

- `WS_CHILD`: Создает дочернее окно, представляющее элемент управления "Вкладка". Не может использоваться с WS_POPUP стилем.
- `WS_VISIBLE`: Создает элемент управления "Вкладка", который изначально является видимым.
- `WS_DISABLED`: Создает окно, которое изначально отключено.
- `WS_GROUP`: Задает первый элемент управления группы элементов управления, в которой пользователь может перемещаться от одного элемента управления к другому с помощью клавиш со стрелками. Все элементы управления, определенные с помощью `WS_GROUP` стиля: после первого элемента управления принадлежат к одной группе. Следующий элемент управления с `WS_GROUP` стилем: завершает группу стилей и запускает следующую группу (то есть одна группа заканчивается, где начинается следующая).
- `WS_TABSTOP`: Указывает одно из нескольких элементов управления, через которое пользователь может перемещаться с помощью клавиши TAB. Клавиша TAB перемещает пользователя к следующему элементу управления, указанному `WS_TABSTOP` стилем:.

Чтобы создать элемент управления "Вкладка" с расширенными стилями окна, вызовите метод [`CTabCtrl::CreateEx`](#createex) вместо `Create` .

### <a name="example"></a>Пример

[!code-cpp[NVC_MFC_CTabCtrl#2](../../mfc/reference/codesnippet/cpp/ctabctrl-class_2.cpp)]

## <a name="ctabctrlcreateex"></a><a name="createex"></a> `CTabCtrl::CreateEx`

Создает элемент управления (дочернее окно) и связывает его с `CTabCtrl` объектом.

```cpp
virtual BOOL CreateEx(
    DWORD dwExStyle,
    DWORD dwStyle,
    const RECT& rect,
    CWnd* pParentWnd,
    UINT nID);
```

### <a name="parameters"></a>Параметры

*`dwExStyle`*\
Задает расширенный стиль создаваемого элемента управления. Список расширенных стилей Windows см *`dwExStyle`* . в параметре для [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexw) в Windows SDK.

*`dwStyle`*\
Задает стиль элемента управления Tab. Примените любое сочетание [стилей элементов управления Tab](/windows/win32/Controls/tab-control-styles), описанное в Windows SDK.  [`Create`](#create) Список стилей окон, которые также можно применить к элементу управления, см. в разделе Примечания в.

*`rect`*\
Ссылка на [`RECT`](/windows/win32/api/windef/ns-windef-rect) структуру, описывающую размер и расположение создаваемого окна в клиентских координатах *`pParentWnd`* .

*`pParentWnd`*\
Указатель на окно, которое является родительским элементом управления.

*`nID`*\
Идентификатор дочернего окна элемента управления.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если успешное выполнение равно 0.

### <a name="remarks"></a>Remarks

Используйте `CreateEx` вместо [`Create`](#create) для применения расширенных стилей Windows, заданных **WS_EX_** в расширенном стиле Windows.

`CreateEx` создает элемент управления с расширенными стилями Windows, заданными параметром *`dwExStyle`* . Установка расширенных стилей, относящихся к элементу управления с помощью [`SetExtendedStyle`](#setextendedstyle) . Например, используйте `CreateEx` для установки таких стилей, как WS_EX_CONTEXTHELP, но используйте `SetExtendedStyle` для установки таких стилей, как TCS_EX_FLATSEPARATORS. Дополнительные сведения см. в статье стили, описанные в разделе « [Управление расширенными стилями](/windows/win32/Controls/tab-control-extended-styles) » в Windows SDK.

## <a name="ctabctrlctabctrl"></a><a name="ctabctrl"></a> `CTabCtrl::CTabCtrl`

Формирует объект `CTabCtrl`.

```cpp
CTabCtrl();
```

## <a name="ctabctrldeleteallitems"></a><a name="deleteallitems"></a> `CTabCtrl::DeleteAllItems`

Удаляет все элементы из элемента управления "Вкладка".

```cpp
BOOL DeleteAllItems();
```

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

## <a name="ctabctrldeleteitem"></a><a name="deleteitem"></a> `CTabCtrl::DeleteItem`

Удаляет указанный элемент из элемента управления "Вкладка".

```cpp
BOOL DeleteItem(int nItem);
```

### <a name="parameters"></a>Параметры

*`nItem`*\
Отсчитываемое от нуля значение удаляемого элемента.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFC_CTabCtrl#3](../../mfc/reference/codesnippet/cpp/ctabctrl-class_3.cpp)]

## <a name="ctabctrldeselectall"></a><a name="deselectall"></a> `CTabCtrl::DeselectAll`

Сбрасывает элементы в элементе управления "Вкладка" и очищает все нажатые клавиши.

```cpp
void DeselectAll(BOOL fExcludeFocus);
```

### <a name="parameters"></a>Параметры

*`fExcludeFocus`*\
Флаг, указывающий область девыделения элемента. Если этот параметр имеет значение `FALSE` , все кнопки на вкладке будут сброшены. Если задано значение `TRUE` , все элементы вкладки, кроме выбранного в данный момент, будут сброшены.

### <a name="remarks"></a>Remarks

Эта функция члена реализует поведение сообщения Win32, [`TCM_DESELECTALL`](/windows/win32/Controls/tcm-deselectall) как описано в Windows SDK.

## <a name="ctabctrldrawitem"></a><a name="drawitem"></a> `CTabCtrl::DrawItem`

Вызывается структурой при изменении визуального аспекта элемента управления "Вкладка", рисуемого владельцем.

```cpp
virtual void DrawItem(LPDRAWITEMSTRUCT lpDrawItemStruct);
```

### <a name="parameters"></a>Параметры

*`lpDrawItemStruct`*\
Указатель на структуру, [`DRAWITEMSTRUCT`](/windows/win32/api/winuser/ns-winuser-drawitemstruct) описывающую закрашиваемый элемент.

### <a name="remarks"></a>Remarks

`itemAction`Элемент `DRAWITEMSTRUCT` структуры определяет действие рисования.

По умолчанию эта функция члена не выполняет никаких действий. Переопределите эту функцию-член, чтобы реализовать Рисование для объекта, рисуемого владельцем `CTabCtrl` .

Приложение должно восстановить все объекты интерфейса графических устройств (GDI), выбранные для контекста интерфейса, указанного в *`lpDrawItemStruct`* перед завершением этой функции-члена.

## <a name="ctabctrlgetcurfocus"></a><a name="getcurfocus"></a> `CTabCtrl::GetCurFocus`

Извлекает индекс вкладки с текущим фокусом.

```cpp
int GetCurFocus() const;
```

### <a name="return-value"></a>Возвращаемое значение

Отсчитываемый от нуля индекс вкладки с текущим фокусом.

## <a name="ctabctrlgetcursel"></a><a name="getcursel"></a> `CTabCtrl::GetCurSel`

Извлекает текущую выбранную вкладку в элементе управления "Вкладка".

```cpp
int GetCurSel() const;
```

### <a name="return-value"></a>Возвращаемое значение

Отсчитываемый от нуля индекс выбранной вкладки в случае успеха или-1, если вкладка не выбрана.

## <a name="ctabctrlgetextendedstyle"></a><a name="getextendedstyle"></a> `CTabCtrl::GetExtendedStyle`

Извлекает расширенные стили, используемые в данный момент для элемента управления "Вкладка".

```cpp
DWORD GetExtendedStyle();
```

### <a name="return-value"></a>Возвращаемое значение

Представляет расширенные стили, используемые в данный момент для элемента управления "Вкладка". Это значение представляет собой сочетание [расширенных стилей элемента управления Tab](/windows/win32/Controls/tab-control-extended-styles), как описано в Windows SDK.

### <a name="remarks"></a>Remarks

Эта функция члена реализует поведение сообщения Win32 [TCM_GETEXTENDEDSTYLE](/windows/win32/Controls/tcm-getextendedstyle), как описано в Windows SDK.

## <a name="ctabctrlgetimagelist"></a><a name="getimagelist"></a> `CTabCtrl::GetImageList`

Извлекает список изображений, связанных с элементом управления "Вкладка".

```cpp
CImageList* GetImageList() const;
```

### <a name="return-value"></a>Возвращаемое значение

В случае успеха указатель на список изображений элемента управления Tab; в противном случае значение NULL.

## <a name="ctabctrlgetitem"></a><a name="getitem"></a> `CTabCtrl::GetItem`

Извлекает сведения о вкладке в элементе управления "Вкладка".

```cpp
BOOL GetItem(int nItem,   TCITEM* pTabCtrlItem) const;
```

### <a name="parameters"></a>Параметры

*`nItem`*\
Отсчитываемый от нуля индекс вкладки.

*`pTabCtrlItem`*\
Указатель на [`TCITEM`](/windows/win32/api/commctrl/ns-commctrl-tcitemw) структуру, используемый для указания извлекаемой информации. Также используется для получения сведений о вкладке. Эта структура используется с функциями- `InsertItem` `GetItem` членами, и `SetItem` .

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение `TRUE` в случае успешного выполнения; в противном случае — значение `FALSE`.

### <a name="remarks"></a>Remarks

При отправке сообщения `mask` член указывает, какие атрибуты должны быть возвращены. Если `mask` элемент задает `TCIF_TEXT` значение, `pszText` элемент должен содержать адрес буфера, который получает текст элемента, а `cchTextMax` член должен задавать размер буфера.

- `mask`

   Значение, указывающее, какие `TCITEM` элементы структуры извлекаются или задаются. Этот элемент может быть нулевым или иметь сочетание следующих значений:

  - `TCIF_TEXT`: `pszText` Элемент является допустимым.
  - `TCIF_IMAGE`: `iImage` Элемент является допустимым.
  - `TCIF_PARAM`: `lParam` Элемент является допустимым.
  - `TCIF_RTLREADING`: Текст `pszText` отображается с использованием порядка чтения справа налево в системах на иврите или арабском языке.
  - `TCIF_STATE`: `dwState` Элемент является допустимым.

- `pszText`

   Указатель на строку с завершающим нулем, содержащую текст вкладки, если структура содержит сведения о вкладке. Если структура получает сведения, этот член задает адрес буфера, который получает текст вкладки.

- `cchTextMax`

   Размер буфера, на который указывает `pszText` . Этот элемент игнорируется, если структура не получает сведений.

- `iImage` Индекс в списке изображений элемента управления Tab или-1, если для вкладки нет изображения.

- `lParam`

   Определяемые приложением данные, связанные с вкладкой. Если на одну вкладку приходится более 4 байт данных, определяемых приложением, приложение должно определить структуру и использовать ее вместо `TCITEM` структуры. Первый член определяемой приложением структуры должен быть структурой [тЦитемхеадер](/windows/win32/api/commctrl/ns-commctrl-tcitemheaderw). `TCITEMHEADER`Структура идентична `TCITEM` структуре, но без `lParam` элемента. Разница между размером структуры и размером `TCITEMHEADER` структуры должна равняться количеству дополнительных байтов на вкладку.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFC_CTabCtrl#4](../../mfc/reference/codesnippet/cpp/ctabctrl-class_4.cpp)]

## <a name="ctabctrlgetitemcount"></a><a name="getitemcount"></a> `CTabCtrl::GetItemCount`

Извлекает число вкладок в наборе вкладок.

```cpp
int GetItemCount() const;
```

### <a name="return-value"></a>Возвращаемое значение

Число элементов в элементе управления "Вкладка".

### <a name="example"></a>Пример

  См. пример для [`CPropertySheet::GetTabControl`](../../mfc/reference/cpropertysheet-class.md#gettabcontrol) .

## <a name="ctabctrlgetitemrect"></a><a name="getitemrect"></a> `CTabCtrl::GetItemRect`

Извлекает ограничивающий прямоугольник для указанной вкладки в элементе управления "Вкладка".

```cpp
BOOL GetItemRect(int nItem,   LPRECT lpRect) const;
```

### <a name="parameters"></a>Параметры

*`nItem`*\
Отсчитываемый от нуля индекс элемента вкладки.

*`lpRect`*\
Указатель на [`RECT`](/windows/win32/api/windef/ns-windef-rect) структуру, которая получает ограничивающий прямоугольник вкладки. Эти координаты используют текущий режим сопоставления окна просмотра.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="example"></a>Пример

  См. пример для [`CPropertySheet::GetTabControl`](../../mfc/reference/cpropertysheet-class.md#gettabcontrol) .

## <a name="ctabctrlgetitemstate"></a><a name="getitemstate"></a> `CTabCtrl::GetItemState`

Получает состояние элемента управления "Вкладка", идентифицируемого *`nItem`* .

```cpp
DWORD GetItemState(
    int nItem,
    DWORD dwMask) const;
```

### <a name="parameters"></a>Параметры

*`nItem`*\
Отсчитываемый от нуля номер индекса элемента, для которого требуется получить сведения о состоянии.

*`dwMask`*\
Маска, указывающая, какие из флагов состояния элемента должны быть возвращены. Список значений см. в разделе элемент маски [`TCITEM`](/windows/win32/api/commctrl/ns-commctrl-tcitemw) структуры, как описано в Windows SDK.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на значение DWORD, получающее сведения о состоянии. Может иметь одно из следующих значений:

|Значение|Описание|
|-----------|-----------------|
|`TCIS_BUTTONPRESSED`|Элемент управления вкладки выбран.|
|`TCIS_HIGHLIGHTED`|Элемент управления вкладки выделяется, а вкладка и текст рисуются с использованием текущего цвета выделения. При использовании цвета выделения это будет истинной интерполяцией, а не с перекрашенным цветом.|

### <a name="remarks"></a>Remarks

Состояние элемента задается `dwState` членом `TCITEM` структуры.

## <a name="ctabctrlgetrowcount"></a><a name="getrowcount"></a> `CTabCtrl::GetRowCount`

Извлекает текущее количество строк в элементе управления "Вкладка".

```cpp
int GetRowCount() const;
```

### <a name="return-value"></a>Возвращаемое значение

Количество строк вкладок в элементе управления "Вкладка".

### <a name="remarks"></a>Remarks

Только элементы управления "Вкладка", имеющие стиль TCS_MULTILINE, могут содержать несколько строк вкладок.

## <a name="ctabctrlgettooltips"></a><a name="gettooltips"></a> `CTabCtrl::GetToolTips`

Извлекает маркер элемента управления "Подсказка", связанный с элементом управления "Вкладка".

```cpp
CToolTipCtrl* GetToolTips() const;
```

### <a name="return-value"></a>Возвращаемое значение

При успешном завершении элемента управления Подсказка в противном случае — NULL.

### <a name="remarks"></a>Remarks

Элемент управления "Вкладка" создает элемент управления "всплывающая подсказка", если он имеет стиль TCS_TOOLTIPS. Можно также назначить элемент управления "Подсказка" для элемента управления "Вкладка" с помощью `SetToolTips` функции-члена.

## <a name="ctabctrlhighlightitem"></a><a name="highlightitem"></a> `CTabCtrl::HighlightItem`

Задает состояние выделения элемента вкладки.

```cpp
BOOL HighlightItem(int idItem,  BOOL fHighlight = TRUE);
```

### <a name="parameters"></a>Параметры

*`idItem`*\
Отсчитываемый от нуля индекс элемента управления вкладки.

*`fHighlight`*\
Значение, указывающее заданное состояние выделения. Если это значение равно `TRUE` , вкладка выделяется; `FALSE` значение, если для вкладки задано состояние по умолчанию.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение в случае успеха, иначе — 0.

### <a name="remarks"></a>Remarks

Эта функция члена реализует сообщение Win32 [`TCM_HIGHLIGHTITEM`](/windows/win32/Controls/tcm-highlightitem) , как описано в Windows SDK.

## <a name="ctabctrlhittest"></a><a name="hittest"></a> `CTabCtrl::HitTest`

Определяет, какая вкладка, если она есть, находится на заданной позиции экрана.

```cpp
int HitTest(TCHITTESTINFO* pHitTestInfo) const;
```

### <a name="parameters"></a>Параметры

*фиттестинфо*\
Указатель на [`TCHITTESTINFO`](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) структуру, как описано в Windows SDK, которая указывает на проверяемую на экране точку экрана.

### <a name="return-value"></a>Возвращаемое значение

Возвращает отсчитываемый от нуля индекс вкладки или-1, если вкладка не находится в указанной позиции.

## <a name="ctabctrlinsertitem"></a><a name="insertitem"></a> `CTabCtrl::InsertItem`

Вставляет новую вкладку в существующий элемент управления "Вкладка".

```cpp
LONG InsertItem(
    int nItem,
    TCITEM* pTabCtrlItem);

LONG InsertItem(
    int nItem,
    LPCTSTR lpszItem);

LONG InsertItem(
    int nItem,
    LPCTSTR lpszItem,
    int nImage);

LONG InsertItem(
    UINT nMask,
    int nItem,
    LPCTSTR lpszItem,
    int nImage,
    LPARAM lParam);

LONG InsertItem(
    UINT nMask,
    int nItem,
    LPCTSTR lpszItem,
    int nImage,
    LPARAM lParam,
    DWORD dwState,
    DWORD dwStateMask);
```

### <a name="parameters"></a>Параметры

*`nItem`*\
Отсчитываемый от нуля индекс новой вкладки.

*`pTabCtrlItem`*\
Указатель на [`TCITEM`](/windows/win32/api/commctrl/ns-commctrl-tcitemw) структуру, указывающую атрибуты вкладки.

*`lpszItem`*\
Адрес строки, завершающейся нулем, которая содержит текст вкладки.

*`nImage`*\
Отсчитываемый от нуля индекс изображения, вставляемого из списка изображений.

*`nMask`*\
Указывает, какие `TCITEM` атрибуты структуры задаются. Может быть нулем или сочетанием следующих значений:

- `TCIF_TEXT`: `pszText` Элемент является допустимым.
- `TCIF_IMAGE`: `iImage` Элемент является допустимым.
- `TCIF_PARAM`: *`lParam`* Элемент является допустимым.
- `TCIF_RTLREADING`: Текст `pszText` отображается с использованием порядка чтения справа налево в системах на иврите или арабском языке.
- `TCIF_STATE`: *`dwState`* Элемент является допустимым.

*`lParam`*\
Определяемые приложением данные, связанные с вкладкой.

*`dwState`*\
Указывает значения для состояний элемента. Дополнительные сведения см [`TCITEM`](/windows/win32/api/commctrl/ns-commctrl-tcitemw) . в разделе Windows SDK.

*`dwStateMask`*\
Указывает, какие состояния должны быть установлены. Дополнительные сведения см [`TCITEM`](/windows/win32/api/commctrl/ns-commctrl-tcitemw) . в разделе Windows SDK.

### <a name="return-value"></a>Возвращаемое значение

Отсчитываемый от нуля индекс новой вкладки в случае успеха; в противном случае — 1.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFC_CTabCtrl#5](../../mfc/reference/codesnippet/cpp/ctabctrl-class_5.cpp)]

## <a name="ctabctrlremoveimage"></a><a name="removeimage"></a> `CTabCtrl::RemoveImage`

Удаляет указанный образ из списка изображений элемента управления "Вкладка".

```cpp
void RemoveImage(int nImage);
```

### <a name="parameters"></a>Параметры

*`nImage`*\
Отсчитываемый от нуля индекс удаляемого изображения.

### <a name="remarks"></a>Remarks

Элемент управления "Вкладка" обновляет индекс изображения каждой вкладки, чтобы каждая вкладка осталась связанной с одним и тем же изображением.

## <a name="ctabctrlsetcurfocus"></a><a name="setcurfocus"></a> `CTabCtrl::SetCurFocus`

Устанавливает фокус на указанную вкладку в элементе управления "Вкладка".

```cpp
void SetCurFocus(int nItem);
```

### <a name="parameters"></a>Параметры

*`nItem`*\
Указывает индекс вкладки, получающей фокус.

### <a name="remarks"></a>Remarks

Эта функция члена реализует поведение сообщения Win32 [TCM_SETCURFOCUS](/windows/win32/Controls/tcm-setcurfocus), как описано в Windows SDK.

## <a name="ctabctrlsetcursel"></a><a name="setcursel"></a> `CTabCtrl::SetCurSel`

Выбирает вкладку в элементе управления "Вкладка".

```cpp
int SetCurSel(int nItem);
```

### <a name="parameters"></a>Параметры

*`nItem`*\
Отсчитываемый от нуля индекс элемента, который необходимо выбрать.

### <a name="return-value"></a>Возвращаемое значение

Отсчитываемый от нуля индекс ранее выбранной вкладки в случае успеха, в противном случае — 1.

### <a name="remarks"></a>Remarks

Элемент управления "Вкладка" не отправляет сообщение уведомления TCN_SELCHANGING или TCN_SELCHANGE, если выбрана вкладка с помощью этой функции. Эти уведомления отправляются с помощью WM_NOTIFY, когда пользователь нажимает или использует клавиатуру для изменения вкладок.

## <a name="ctabctrlsetextendedstyle"></a><a name="setextendedstyle"></a> `CTabCtrl::SetExtendedStyle`

Задает расширенные стили для элемента управления "Вкладка".

```cpp
DWORD SetExtendedStyle(DWORD dwNewStyle, DWORD dwExMask = 0);
```

### <a name="parameters"></a>Параметры

*`dwNewStyle`*\
Значение, указывающее сочетание расширенных стилей элемента управления Tab.

*`dwExMask`*\
Значение типа DWORD, указывающее, какие стили в должны *`dwNewStyle`* быть затронуты. Будут изменены только расширенные стили в *`dwExMask`* . Все остальные стили будут поддерживаться как есть. Если этот параметр равен нулю, будут затронуты все стили в *`dwNewStyle`* .

### <a name="return-value"></a>Возвращаемое значение

Значение типа DWORD, содержащее предыдущий [элемент управления Tab, расширенные стили](/windows/win32/Controls/tab-control-extended-styles), как описано в Windows SDK.

### <a name="return-value"></a>Возвращаемое значение

Эта функция члена реализует поведение сообщения Win32 [`TCM_SETEXTENDEDSTYLE`](/windows/win32/Controls/tcm-setextendedstyle) , как описано в Windows SDK.

## <a name="ctabctrlsetimagelist"></a><a name="setimagelist"></a> `CTabCtrl::SetImageList`

Присваивает список изображений элементу управления "Вкладка".

```cpp
CImageList* SetImageList(CImageList* pImageList);
```

### <a name="parameters"></a>Параметры

*`pImageList`*\
Указатель на список изображений, назначаемый элементу управления "Вкладка".

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на предыдущий список изображений или значение NULL, если предыдущий список изображений отсутствует.

## <a name="ctabctrlsetitem"></a><a name="setitem"></a> `CTabCtrl::SetItem`

Задает некоторые или все атрибуты вкладки.

```cpp
BOOL SetItem(int nItem,   TCITEM* pTabCtrlItem);
```

### <a name="parameters"></a>Параметры

*`nItem`*\
Отсчитываемый от нуля индекс элемента.

*`pTabCtrlItem`*\
Указатель на [`TCITEM`](/windows/win32/api/commctrl/ns-commctrl-tcitemw) структуру, содержащую новые атрибуты элемента. `mask`Член указывает, какие атрибуты задаются. Если `mask` член указывает `TCIF_TEXT` значение, то `pszText` членом является адрес строки, завершающейся нулем, и `cchTextMax` элемент игнорируется.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="example"></a>Пример

  См. пример для [элемента "DataItem](#getitem)".

## <a name="ctabctrlsetitemextra"></a><a name="setitemextra"></a> `CTabCtrl::SetItemExtra`

Задает число байтов на вкладку, зарезервированную для определяемых приложением данных в элементе управления "Вкладка".

```cpp
BOOL SetItemExtra(int nBytes);
```

### <a name="parameters"></a>Параметры

*`nBytes`*\
Число устанавливаемых дополнительных байтов.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение в случае успеха, иначе — 0.

### <a name="remarks"></a>Remarks

Эта функция члена реализует поведение сообщения Win32 [`TCM_SETITEMEXTRA`](/windows/win32/Controls/tcm-setitemextra) , как описано в Windows SDK.

## <a name="ctabctrlsetitemsize"></a><a name="setitemsize"></a> `CTabCtrl::SetItemSize`

Задает ширину и высоту элементов набора вкладок.

```cpp
CSize SetItemSize(CSize size);
```

### <a name="parameters"></a>Параметры

*`size`*\
Новая ширина и высота (в пикселях) элементов набора вкладок.

### <a name="return-value"></a>Возвращаемое значение

Возвращает старую ширину и высоту элементов набора вкладок.

## <a name="ctabctrlsetitemstate"></a><a name="setitemstate"></a> `CTabCtrl::SetItemState`

Задает состояние элемента управления вкладки, идентифицируемого *`nItem`* .

```cpp
BOOL SetItemState(
    int nItem,
    DWORD dwMask,
    DWORD dwState);
```

### <a name="parameters"></a>Параметры

*`nItem`*\
Отсчитываемый от нуля номер индекса элемента, для которого задаются сведения о состоянии.

*`dwMask`*\
Маска, указывающая, какие флаги состояния элемента задаются. Список значений см. в разделе элемент маски [`TCITEM`](/windows/win32/api/commctrl/ns-commctrl-tcitemw) структуры, как описано в Windows SDK.

*`dwState`*\
Ссылка на значение DWORD, содержащее сведения о состоянии. Может иметь одно из следующих значений:

|Значение|Описание|
|-----------|-----------------|
|`TCIS_BUTTONPRESSED`|Элемент управления вкладки выбран.|
|`TCIS_HIGHLIGHTED`|Элемент управления вкладки выделяется, а вкладка и текст рисуются с использованием текущего цвета выделения. При использовании цвета выделения это будет истинной интерполяцией, а не с перекрашенным цветом.|

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

## <a name="ctabctrlsetmintabwidth"></a><a name="setmintabwidth"></a> `CTabCtrl::SetMinTabWidth`

Устанавливает минимальную ширину элементов в элементе управления "Вкладка".

```cpp
int SetMinTabWidth(int cx);
```

### <a name="parameters"></a>Параметры

*`cx`*\
Минимальная ширина, устанавливаемая для элемента управления вкладки. Если этот параметр имеет значение-1, то элемент управления будет использовать ширину табуляции по умолчанию.

### <a name="return-value"></a>Возвращаемое значение

Предыдущая минимальная ширина вкладки.

### <a name="return-value"></a>Возвращаемое значение

Эта функция члена реализует поведение сообщения Win32 [`TCM_SETMINTABWIDTH`](/windows/win32/Controls/tcm-setmintabwidth) , как описано в Windows SDK.

## <a name="ctabctrlsetpadding"></a><a name="setpadding"></a> `CTabCtrl::SetPadding`

Задает объем пространства (заполнение) вокруг значка и метки каждой вкладки в элементе управления "Вкладка".

```cpp
void SetPadding(CSize size);
```

### <a name="parameters"></a>Параметры

*`size`*\
Задает объем пространства (заполнение) вокруг значка и метки каждой вкладки в элементе управления "Вкладка".

## <a name="ctabctrlsettooltips"></a><a name="settooltips"></a> `CTabCtrl::SetToolTips`

Назначает элемент управления «Подсказка» для элемента управления Tab.

```cpp
void SetToolTips(CToolTipCtrl* pWndTip);
```

### <a name="parameters"></a>Параметры

*`pWndTip`*\
Маркер элемента управления "Подсказка".

### <a name="remarks"></a>Remarks

Можно получить элемент управления "Подсказка", связанный с элементом управления "Вкладка", вызвав метод `GetToolTips` .

### <a name="example"></a>Пример

  См. пример для [`CPropertySheet::GetTabControl`](../../mfc/reference/cpropertysheet-class.md#gettabcontrol) .

## <a name="see-also"></a>См. также

[`CWnd` См](../../mfc/reference/cwnd-class.md)\
[`CHeaderCtrl` См](../../mfc/reference/cheaderctrl-class.md)\
[ `CListCtrl` ](../../mfc/reference/clistctrl-class.md) 
 [Диаграмма иерархии](../../mfc/hierarchy-chart.md) классов\