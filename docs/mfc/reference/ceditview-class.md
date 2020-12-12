---
description: 'Дополнительные сведения о: CEditView Class'
title: Класс CEditView
ms.date: 11/04/2016
f1_keywords:
- CEditView
- AFXEXT/CEditView
- AFXEXT/CEditView::CEditView
- AFXEXT/CEditView::FindText
- AFXEXT/CEditView::GetBufferLength
- AFXEXT/CEditView::GetEditCtrl
- AFXEXT/CEditView::GetPrinterFont
- AFXEXT/CEditView::GetSelectedText
- AFXEXT/CEditView::LockBuffer
- AFXEXT/CEditView::PrintInsideRect
- AFXEXT/CEditView::SerializeRaw
- AFXEXT/CEditView::SetPrinterFont
- AFXEXT/CEditView::SetTabStops
- AFXEXT/CEditView::UnlockBuffer
- AFXEXT/CEditView::OnFindNext
- AFXEXT/CEditView::OnReplaceAll
- AFXEXT/CEditView::OnReplaceSel
- AFXEXT/CEditView::OnTextNotFound
- AFXEXT/CEditView::dwStyleDefault
helpviewer_keywords:
- CEditView [MFC], CEditView
- CEditView [MFC], FindText
- CEditView [MFC], GetBufferLength
- CEditView [MFC], GetEditCtrl
- CEditView [MFC], GetPrinterFont
- CEditView [MFC], GetSelectedText
- CEditView [MFC], LockBuffer
- CEditView [MFC], PrintInsideRect
- CEditView [MFC], SerializeRaw
- CEditView [MFC], SetPrinterFont
- CEditView [MFC], SetTabStops
- CEditView [MFC], UnlockBuffer
- CEditView [MFC], OnFindNext
- CEditView [MFC], OnReplaceAll
- CEditView [MFC], OnReplaceSel
- CEditView [MFC], OnTextNotFound
- CEditView [MFC], dwStyleDefault
ms.assetid: bf38255c-fcbe-450c-95b2-3c5e35f86c37
ms.openlocfilehash: b83b83b90fe530d2615a507d80e2af771397d286
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97184716"
---
# <a name="ceditview-class"></a>Класс CEditView

Тип класса представления, который предоставляет функциональные возможности элемента управления "поле ввода" Windows и может использоваться для реализации простой функциональности текстового редактора.

## <a name="syntax"></a>Синтаксис

```
class CEditView : public CCtrlView
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CEditView:: CEditView](#ceditview)|Создает объект типа `CEditView`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CEditView:: строки FindText](#findtext)|Выполняет поиск строки внутри текста.|
|[CEditView:: Жетбуфферленгс](#getbufferlength)|Получает длину символьного буфера.|
|[CEditView:: Жетедитктрл](#geteditctrl)|Предоставляет доступ к `CEdit` части `CEditView` объекта (элемент управления Windows Edit).|
|[CEditView:: Жетпринтерфонт](#getprinterfont)|Извлекает текущий шрифт принтера.|
|[CEditView:: Жетселектедтекст](#getselectedtext)|Извлекает текущий выделенный фрагмент текста.|
|[CEditView:: Локкбуффер](#lockbuffer)|Блокирует буфер.|
|[CEditView::P Ринтинсидерект](#printinsiderect)|Отображает текст внутри данного прямоугольника.|
|[CEditView:: Сериализерав](#serializeraw)|Сериализует `CEditView` объект на диск в виде необработанного текста.|
|[CEditView:: Сетпринтерфонт](#setprinterfont)|Задает новый шрифт принтера.|
|[CEditView:: Сеттабстопс](#settabstops)|Задает позиции табуляции как для экрана, так и для печати.|
|[CEditView:: Унлоккбуффер](#unlockbuffer)|Разблокирует буфер.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[CEditView:: Онфинднекст](#onfindnext)|Находит следующее вхождение текстовой строки.|
|[CEditView:: Онреплацеалл](#onreplaceall)|Заменяет все вхождения заданной строки новой строкой.|
|[CEditView:: Онреплацесел](#onreplacesel)|Заменяет текущий выбор.|
|[CEditView:: Онтекстнотфаунд](#ontextnotfound)|Вызывается, когда операция поиска не может сопоставить какой-либо текст.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[CEditView::d Встиледефаулт](#dwstyledefault)|Стиль по умолчанию для объектов типа `CEditView` .|

## <a name="remarks"></a>Комментарии

`CEditView`Класс предоставляет следующие дополнительные функции:

- Печать.

- Поиск и замена.

Поскольку класс `CEditView` является производным от класса `CView` , объекты класса `CEditView` можно использовать с документами и шаблонами документов.

`CEditView`Текст каждого элемента управления хранится в собственном объекте глобальной памяти. Приложение может иметь любое количество `CEditView` объектов.

Создайте объекты типа, `CEditView` Если требуется окно редактирования с добавленными функциями, описанными выше, или если требуется функциональность простого текстового редактора. `CEditView`Объект может занимать всю клиентскую область окна. Создайте собственные классы из, `CEditView` чтобы добавить или изменить основные функциональные возможности или объявить классы, которые можно добавить в шаблон документа.

Реализация класса по умолчанию `CEditView` обрабатывает следующие команды: ID_EDIT_SELECT_ALL, ID_EDIT_FIND, ID_EDIT_REPLACE, ID_EDIT_REPEAT и ID_FILE_PRINT.

Ограничение по символам по умолчанию для `CEditView` равно (1024 \* 1024-1 = 1048575). Это можно изменить, вызвав функцию EM_LIMITTEXT базового элемента управления Edit. Однако ограничения различаются в зависимости от операционной системы и типа элемента управления "поле ввода" (один или несколько строк). Дополнительные сведения об этих ограничениях см. в разделе [EM_LIMITTEXT](/windows/win32/Controls/em-limittext).

Чтобы изменить это ограничение в элементе управления, переопределите `OnCreate()` функцию для `CEditView` класса и вставьте следующую строку кода:

[!code-cpp[NVC_MFCDocView#65](../../mfc/codesnippet/cpp/ceditview-class_1.cpp)]

Объекты типа `CEditView` (или из типов, производных от `CEditView` ) имеют следующие ограничения.

- `CEditView` не реализует верное значение, которое вы видите при редактировании (WYSIWYG). При наличии выбора между удобочитаемостью на экране и соответствующими печатными выводимыми данными `CEditView` для удобочитаемости экрана.

- `CEditView` может отображать текст только в одном шрифте. Специальное форматирование символов не поддерживается. Дополнительные возможности см. в разделе класс [CRichEditView](../../mfc/reference/cricheditview-class.md) .

- Количество текста, которое `CEditView` может содержать ограничение, ограничено. Ограничения одинаковы для `CEdit` элемента управления.

Дополнительные сведения о `CEditView` см. в разделе [производные классы представлений, доступные в MFC](../../mfc/derived-view-classes-available-in-mfc.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CView](../../mfc/reference/cview-class.md)

[CCtrlView](../../mfc/reference/cctrlview-class.md)

`CEditView`

## <a name="requirements"></a>Требования

**Заголовок:** афксекст. h

## <a name="ceditviewceditview"></a><a name="ceditview"></a> CEditView:: CEditView

Создает объект типа `CEditView`.

```
CEditView();
```

### <a name="remarks"></a>Комментарии

После создания объекта необходимо вызвать функцию [CWnd:: Create](../../mfc/reference/cwnd-class.md#create) перед использованием элемента управления Edit. Если вы наследуете класс от `CEditView` и добавите его в шаблон с помощью `CWinApp::AddDocTemplate` , платформа вызывает и этот конструктор, и `Create` функцию.

## <a name="ceditviewdwstyledefault"></a><a name="dwstyledefault"></a> CEditView::d Встиледефаулт

Содержит стиль объекта по умолчанию `CEditView` .

```
static const DWORD dwStyleDefault;
```

### <a name="remarks"></a>Комментарии

Передайте этот статический член в качестве параметра *двстиле* `Create` функции, чтобы получить стиль по умолчанию для `CEditView` объекта.

## <a name="ceditviewfindtext"></a><a name="findtext"></a> CEditView:: строки FindText

Вызовите `FindText` функцию для поиска в `CEditView` текстовом буфере объекта.

```
BOOL FindText(
    LPCTSTR lpszFind,
    BOOL bNext = TRUE,
    BOOL bCase = TRUE);
```

### <a name="parameters"></a>Параметры

*лпсзфинд*<br/>
Текст, который необходимо найти.

*бнекст*<br/>
Задает направление поиска. Если значение равно TRUE, направление поиска находится в направлении конца буфера. Если значение равно FALSE, направление поиска находится в направлении начала буфера.

*бкасе*<br/>
Указывает, учитывается ли регистр при поиске. Если значение равно TRUE, поиск выполняется с учетом регистра. Если значение равно FALSE, поиск не учитывает регистр.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если искомый текст найден. в противном случае — 0.

### <a name="remarks"></a>Комментарии

Эта функция ищет текст в буфере для текста, указанного параметром *лпсзфинд*, начиная с текущего выбора, в направлении, указанном параметром *бнекст*, и с учетом регистра, заданным параметром *бкасе*. Если текст найден, он устанавливает для выделения найденный текст и возвращает ненулевое значение. Если текст не найден, функция возвращает 0.

Обычно нет необходимости вызывать `FindText` функцию, если не переопределяете `OnFindNext` , что вызывает `FindText` .

## <a name="ceditviewgetbufferlength"></a><a name="getbufferlength"></a> CEditView:: Жетбуфферленгс

Вызовите эту функцию члена для получения количества символов, находящихся в данный момент в буфере элемента управления правки, не включая знак завершения null.

```
UINT GetBufferLength() const;
```

### <a name="return-value"></a>Возвращаемое значение

Длина строки в буфере.

## <a name="ceditviewgeteditctrl"></a><a name="geteditctrl"></a> CEditView:: Жетедитктрл

Вызовите метод `GetEditCtrl` , чтобы получить ссылку на элемент управления Edit, используемый представлением редактирования.

```
CEdit& GetEditCtrl() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на объект `CEdit`.

### <a name="remarks"></a>Комментарии

Этот элемент управления имеет тип [CEdit](../../mfc/reference/cedit-class.md), поэтому вы можете манипулировать элементом управления Windows Edit напрямую с помощью `CEdit` функций-членов.

> [!CAUTION]
> Использование `CEdit` объекта может изменить состояние базового элемента управления "поле ввода Windows". Например, не следует изменять параметры табуляции с помощью функции [CEdit:: сеттабстопс](../../mfc/reference/cedit-class.md#settabstops) , так как она `CEditView` кэширует эти параметры для использования в элементе управления "поле ввода" и при печати. Вместо этого используйте [CEditView:: сеттабстопс](#settabstops).

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCDocView#66](../../mfc/codesnippet/cpp/ceditview-class_2.cpp)]

## <a name="ceditviewgetprinterfont"></a><a name="getprinterfont"></a> CEditView:: Жетпринтерфонт

Вызовите метод, `GetPrinterFont` чтобы получить указатель на объект [кфонт](../../mfc/reference/cfont-class.md) , описывающий текущий шрифт принтера.

```
CFont* GetPrinterFont() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на `CFont` объект, указывающий текущий шрифт принтера; Значение NULL, если шрифт принтера не задан. Указатель может быть временным. Его не требуется сохранять для дальнейшего использования.

### <a name="remarks"></a>Комментарии

Если шрифт принтера не задан, по умолчанию используется режим печати `CEditView` класса с тем же шрифтом, который используется для отображения.

Используйте эту функцию, чтобы определить текущий шрифт принтера. Если он не является нужным шрифтом принтера, используйте [CEditView:: сетпринтерфонт](#setprinterfont) , чтобы изменить его.

## <a name="ceditviewgetselectedtext"></a><a name="getselectedtext"></a> CEditView:: Жетселектедтекст

Вызовите метод `GetSelectedText` , чтобы скопировать выделенный текст в `CString` объект, до конца выделения или символ, предшествующий первому символу возврата каретки в выделенном фрагменте.

```cpp
void GetSelectedText(CString& strResult) const;
```

### <a name="parameters"></a>Параметры

*стрресулт*<br/>
Ссылка на `CString` объект, который должен получить выделенный текст.

## <a name="ceditviewlockbuffer"></a><a name="lockbuffer"></a> CEditView:: Локкбуффер

Вызовите эту функцию-член, чтобы получить указатель на буфер. Буфер не должен изменяться.

```
LPCTSTR LockBuffer() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на буфер элемента управления редактирования.

## <a name="ceditviewonfindnext"></a><a name="onfindnext"></a> CEditView:: Онфинднекст

Ищет текст в буфере для текста, заданного параметром *лпсзфинд*, в направлении, указанном параметром *бнекст*, с учетом регистра, заданным параметром *бкасе*.

```
virtual void OnFindNext(
    LPCTSTR lpszFind,
    BOOL bNext,
    BOOL bCase);
```

### <a name="parameters"></a>Параметры

*лпсзфинд*<br/>
Текст, который необходимо найти.

*бнекст*<br/>
Задает направление поиска. Если значение равно TRUE, направление поиска находится в направлении конца буфера. Если значение равно FALSE, направление поиска находится в направлении начала буфера.

*бкасе*<br/>
Указывает, учитывается ли регистр при поиске. Если значение равно TRUE, поиск выполняется с учетом регистра. Если значение равно FALSE, поиск не учитывает регистр.

### <a name="remarks"></a>Комментарии

Поиск начинается в начале текущего выделения и выполняется посредством вызова [строки FindText](#findtext). В реализации по умолчанию `OnFindNext` вызывает [онтекстнотфаунд](#ontextnotfound) , если текст не найден.

Переопределите, `OnFindNext` чтобы изменить способ `CEditView` поиска в тексте объекта, производного от. `CEditView` вызывается, `OnFindNext` когда пользователь нажимает кнопку "Найти далее" в стандартном диалоговом окне "найти".

## <a name="ceditviewonreplaceall"></a><a name="onreplaceall"></a> CEditView:: Онреплацеалл

`CEditView` вызывается, `OnReplaceAll` когда пользователь нажимает кнопку Заменить все в стандартном диалоговом окне заменить.

```
virtual void OnReplaceAll(
    LPCTSTR lpszFind,
    LPCTSTR lpszReplace,
    BOOL bCase);
```

### <a name="parameters"></a>Параметры

*лпсзфинд*<br/>
Текст, который необходимо найти.

*лпсзреплаце*<br/>
Текст для замены искомого текста.

*бкасе*<br/>
Указывает, учитывается ли регистр при поиске. Если значение равно TRUE, поиск выполняется с учетом регистра. Если значение равно FALSE, поиск не учитывает регистр.

### <a name="remarks"></a>Комментарии

`OnReplaceAll` выполняет поиск текста, указанного параметром *лпсзфинд*, с учетом регистра, указанного параметром *бкасе*, в тексте в буфере. Поиск начинается в начале текущего выделения. При каждом обнаружении искомого текста эта функция заменяет вхождение текста текстом, заданным параметром *лпсзреплаце*. Поиск выполняется через вызов [строки FindText](#findtext). В реализации по умолчанию [онтекстнотфаунд](#ontextnotfound) вызывается, если текст не найден.

Если текущий выделенный фрагмент не соответствует *лпсзфинд*, выборка обновляется до первого вхождения текста, указанного в параметре *лпсзфинд* , а замена не выполняется. Это позволяет пользователю подтвердить, что это необходимо сделать, если выбор не соответствует заменяемому тексту.

Переопределите, `OnReplaceAll` чтобы изменить способ `CEditView` замены текста объектом, производным от.

## <a name="ceditviewonreplacesel"></a><a name="onreplacesel"></a> CEditView:: Онреплацесел

`CEditView` вызывается, `OnReplaceSel` когда пользователь нажимает кнопку "заменить" в стандартном диалоговом окне "заменить".

```
virtual void OnReplaceSel(
    LPCTSTR lpszFind,
    BOOL bNext,
    BOOL bCase,
    LPCTSTR lpszReplace);
```

### <a name="parameters"></a>Параметры

*лпсзфинд*<br/>
Текст, который необходимо найти.

*бнекст*<br/>
Задает направление поиска. Если значение равно TRUE, направление поиска находится в направлении конца буфера. Если значение равно FALSE, направление поиска находится в направлении начала буфера.

*бкасе*<br/>
Указывает, учитывается ли регистр при поиске. Если значение равно TRUE, поиск выполняется с учетом регистра. Если значение равно FALSE, поиск не учитывает регистр.

*лпсзреплаце*<br/>
Текст для замены найденного текста.

### <a name="remarks"></a>Комментарии

После замены выделения эта функция ищет следующий текст в буфере для следующего вхождения текста, указанного параметром *лпсзфинд*, в направлении, указанном параметром *бнекст*, с учетом регистра, заданным параметром *бкасе*. Поиск выполняется через вызов [строки FindText](#findtext). Если текст не найден, вызывается [онтекстнотфаунд](#ontextnotfound) .

Переопределение `OnReplaceSel` позволяет изменить способ `CEditView` замены выделенного текста объектом, производным от.

## <a name="ceditviewontextnotfound"></a><a name="ontextnotfound"></a> CEditView:: Онтекстнотфаунд

Переопределите эту функцию, чтобы изменить реализацию по умолчанию, которая вызывает функцию Windows `MessageBeep` .

```
virtual void OnTextNotFound(LPCTSTR lpszFind);
```

### <a name="parameters"></a>Параметры

*лпсзфинд*<br/>
Текст, который необходимо найти.

## <a name="ceditviewprintinsiderect"></a><a name="printinsiderect"></a> CEditView::P Ринтинсидерект

Вызов `PrintInsideRect` для печати текста в прямоугольнике, указанном параметром *ректлайаут*.

```
UINT PrintInsideRect(
    CDC *pDC,
    RECT& rectLayout,
    UINT nIndexStart,
    UINT nIndexStop);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
Указатель на контекст устройства принтера.

*ректлайаут*<br/>
Ссылка на объект [крект](../../atl-mfc-shared/reference/crect-class.md) или [структуру Rect](/windows/win32/api/windef/ns-windef-rect) , указывающую прямоугольник, в котором должен быть визуализирован текст.

*ниндексстарт*<br/>
Индекс в буфере первого отображаемого символа.

*ниндексстоп*<br/>
Индекс в буфере символа, следующего за последним символом для подготовки к просмотру.

### <a name="return-value"></a>Возвращаемое значение

Индекс следующего печатаемого символа (то есть символа после последнего отрисованного символа).

### <a name="remarks"></a>Комментарии

Если у `CEditView` элемента управления нет стиля ES_AUTOHSCROLL, текст упаковывается внутри прямоугольника отрисовки. Если элемент управления имеет стиль ES_AUTOHSCROLL, текст обрезается по правому краю прямоугольника.

`rect.bottom`Элемент объекта *ректлайаут* изменяется таким образом, чтобы размеры прямоугольника определяли часть исходного прямоугольника, занятого текстом.

## <a name="ceditviewserializeraw"></a><a name="serializeraw"></a> CEditView:: Сериализерав

Вызовите `SerializeRaw` , чтобы `CArchive` объект читал или записал текст в `CEditView` объект в текстовый файл.

```cpp
void SerializeRaw(CArchive& ar);
```

### <a name="parameters"></a>Параметры

*ar*<br/>
Ссылка на `CArchive` объект, в котором хранится сериализованный текст.

### <a name="remarks"></a>Комментарии

`SerializeRaw` отличается от `CEditView` внутренней реализации `Serialize` в тем, что он считывает и записывает только текст без предшествующих данных описания объекта.

## <a name="ceditviewsetprinterfont"></a><a name="setprinterfont"></a> CEditView:: Сетпринтерфонт

Вызовите, `SetPrinterFont` чтобы установить шрифт принтера на шрифт, заданный параметром *пфонт*.

```cpp
void SetPrinterFont(CFont* pFont);
```

### <a name="parameters"></a>Параметры

*пфонт*<br/>
Указатель на объект типа `CFont` . Если значение равно NULL, шрифт, используемый для печати, основан на отображаемом шрифте.

### <a name="remarks"></a>Комментарии

Если вы хотите, чтобы в представлении всегда использовался определенный шрифт для печати, включите вызов `SetPrinterFont` в `OnPreparePrinting` функцию класса. Эта виртуальная функция вызывается перед печатью, поэтому изменение шрифта происходит до вывода содержимого представления.

## <a name="ceditviewsettabstops"></a><a name="settabstops"></a> CEditView:: Сеттабстопс

Вызовите эту функцию, чтобы задать позиции табуляции, используемые для вывода и печати.

```cpp
void SetTabStops(int nTabStops);
```

### <a name="parameters"></a>Параметры

*нтабстопс*<br/>
Ширина каждой позиции табуляции в диалоговых единицах.

### <a name="remarks"></a>Комментарии

Поддерживается только одна ширина табуляции. ( `CEdit` объекты поддерживают несколько заданной ширины табуляции.) Значения ширины находятся в единицах диалогового окна, которые равны одной четверти от средней ширины символов (только для символов верхнего и нижнего регистра) шрифта, используемого во время печати или отображения. Не следует использовать, `CEdit::SetTabStops` так как `CEditView` должен кэшировать значение табуляции.

Эта функция изменяет только вкладки объекта, для которого она вызывается. Чтобы изменить позиции табуляции для каждого `CEditView` объекта в приложении, вызовите функцию каждого объекта `SetTabStops` .

### <a name="example"></a>Пример

Этот фрагмент кода задает позиции табуляции в элементе управления на каждый четвертый символ, аккуратно измеряя шрифт, используемый элементом управления.

[!code-cpp[NVC_MFCDocView#67](../../mfc/codesnippet/cpp/ceditview-class_3.cpp)]

## <a name="ceditviewunlockbuffer"></a><a name="unlockbuffer"></a> CEditView:: Унлоккбуффер

Вызовите эту функцию члена, чтобы разблокировать буфер.

```cpp
void UnlockBuffer() const;
```

### <a name="remarks"></a>Комментарии

Вызов `UnlockBuffer` после завершения использования указателя, возвращенного [локкбуффер](#lockbuffer).

## <a name="see-also"></a>См. также раздел

[Пример SUPERPAD в MFC](../../overview/visual-cpp-samples.md)<br/>
[Класс Кктрлвиев](../../mfc/reference/cctrlview-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CEdit](../../mfc/reference/cedit-class.md)<br/>
[Класс CDocument](../../mfc/reference/cdocument-class.md)<br/>
[Класс CDocTemplate](../../mfc/reference/cdoctemplate-class.md)<br/>
[Класс Кктрлвиев](../../mfc/reference/cctrlview-class.md)<br/>
[Класс CRichEditView](../../mfc/reference/cricheditview-class.md)
