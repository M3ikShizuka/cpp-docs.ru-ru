---
description: 'Дополнительные сведения о: CSpinButtonCtrl Class'
title: Класс CSpinButtonCtrl
ms.date: 11/04/2016
f1_keywords:
- CSpinButtonCtrl
- AFXCMN/CSpinButtonCtrl
- AFXCMN/CSpinButtonCtrl::CSpinButtonCtrl
- AFXCMN/CSpinButtonCtrl::Create
- AFXCMN/CSpinButtonCtrl::CreateEx
- AFXCMN/CSpinButtonCtrl::GetAccel
- AFXCMN/CSpinButtonCtrl::GetBase
- AFXCMN/CSpinButtonCtrl::GetBuddy
- AFXCMN/CSpinButtonCtrl::GetPos
- AFXCMN/CSpinButtonCtrl::GetRange
- AFXCMN/CSpinButtonCtrl::SetAccel
- AFXCMN/CSpinButtonCtrl::SetBase
- AFXCMN/CSpinButtonCtrl::SetBuddy
- AFXCMN/CSpinButtonCtrl::SetPos
- AFXCMN/CSpinButtonCtrl::SetRange
helpviewer_keywords:
- CSpinButtonCtrl [MFC], CSpinButtonCtrl
- CSpinButtonCtrl [MFC], Create
- CSpinButtonCtrl [MFC], CreateEx
- CSpinButtonCtrl [MFC], GetAccel
- CSpinButtonCtrl [MFC], GetBase
- CSpinButtonCtrl [MFC], GetBuddy
- CSpinButtonCtrl [MFC], GetPos
- CSpinButtonCtrl [MFC], GetRange
- CSpinButtonCtrl [MFC], SetAccel
- CSpinButtonCtrl [MFC], SetBase
- CSpinButtonCtrl [MFC], SetBuddy
- CSpinButtonCtrl [MFC], SetPos
- CSpinButtonCtrl [MFC], SetRange
ms.assetid: 509bfd76-1c5a-4af6-973f-e133c0b87734
ms.openlocfilehash: cfca3d11e4e22cf0fc09025b27400bcefeb0066b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97342694"
---
# <a name="cspinbuttonctrl-class"></a>Класс CSpinButtonCtrl

Предоставляет функциональные возможности стандартного элемента управления "счетчик" Windows.

## <a name="syntax"></a>Синтаксис

```
class CSpinButtonCtrl : public CWnd
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CSpinButtonCtrl:: CSpinButtonCtrl](#cspinbuttonctrl)|Формирует объект `CSpinButtonCtrl`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CSpinButtonCtrl:: Create](#create)|Создает элемент управления "Счетчик" и прикрепляет его к `CSpinButtonCtrl` объекту.|
|[CSpinButtonCtrl:: Креатикс](#createex)|Создает элемент управления "Счетчик" с заданными расширенными стилями Windows и прикрепляет его к `CSpinButtonCtrl` объекту.|
|[CSpinButtonCtrl:: i](#getaccel)|Получает сведения о ускорении для элемента управления "Счетчик".|
|[CSpinButtonCtrl:: Polybase](#getbase)|Извлекает текущую базу для элемента управления "Счетчик".|
|[CSpinButtonCtrl:: приятель](#getbuddy)|Извлекает указатель на текущее окно контакта.|
|[CSpinButtonCtrl:: Жетпос](#getpos)|Извлекает текущую координату элемента управления "Счетчик".|
|[CSpinButtonCtrl:: Range](#getrange)|Получает верхние и нижние пределы (диапазон) для элемента управления "Счетчик".|
|[CSpinButtonCtrl:: Сетакцел](#setaccel)|Задает ускорение для элемента управления "Счетчик".|
|[CSpinButtonCtrl:: Сетбасе](#setbase)|Задает основание для элемента управления "Счетчик".|
|[CSpinButtonCtrl:: Сетбудди](#setbuddy)|Задает окно собеседника для элемента управления "Счетчик".|
|[CSpinButtonCtrl:: Сетпос](#setpos)|Задает текущую точку для элемента управления.|
|[CSpinButtonCtrl:: SetRange](#setrange)|Задает верхний и нижний пределы (диапазон) для элемента управления "Счетчик".|

## <a name="remarks"></a>Комментарии

Элемент управления "Счетчик" (также известный как элемент управления "вверх-вниз") — это пара кнопок со стрелками, которую пользователь может щелкнуть для увеличения или уменьшения значения, например, в положении прокрутки или числа, отображаемого во вспомогательном элементе управления. Значение, связанное с элементом управления "Счетчик", называется его текущей позицией. Элемент управления "Счетчик" чаще всего используется с сопутствующим элементом управления, называемым "дружественным окном".

Этот элемент управления (и, следовательно, `CSpinButtonCtrl` класс) доступен только для программ, работающих под управлением windows 95/98 и Windows NT версии 3,51 и более поздних версий.

Для пользователя элемент управления "Счетчик" и его окно часто выглядят как один элемент управления. Можно указать, что элемент управления "Счетчик" автоматически позиционируется рядом с окном собеседника и автоматически установил заголовок окна собеседника в его текущую точку. Можно использовать элемент управления "Счетчик" с элементом управления "поле ввода", чтобы запросить у пользователя числовые входные данные.

При нажатии клавиши со стрелкой вверх текущее расположение перемещается в сторону максимума, а щелчок стрелки вниз перемещает текущую точку в сторону минимума. По умолчанию минимальное значение — 100, а максимальное — 0. В любой момент, когда минимальное значение превышает максимальное значение (например, при использовании параметров по умолчанию), при нажатии клавиши со стрелкой вверх уменьшается значение расположения, а при щелчке стрелки вниз увеличивается ее.

Элемент управления "Счетчик" без дружественного окна работает как упрощенная полоса прокрутки. Например, элемент управления "Вкладка" иногда отображает элемент управления "Счетчик", позволяющий пользователю прокручивать дополнительные вкладки в представлении.

Дополнительные сведения об использовании см `CSpinButtonCtrl` . в разделе [элементы управления](../../mfc/controls-mfc.md) и [Использование CSpinButtonCtrl](../../mfc/using-cspinbuttonctrl.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

`CSpinButtonCtrl`

## <a name="requirements"></a>Требования

**Заголовок:** afxcmn.h

## <a name="cspinbuttonctrlcreate"></a><a name="create"></a> CSpinButtonCtrl:: Create

Создает элемент управления "Счетчик" и прикрепляет его к `CSpinButtonCtrl` объекту.

```
virtual BOOL Create(
    DWORD dwStyle,
    const RECT& rect,
    CWnd* pParentWnd,
    UINT nID);
```

### <a name="parameters"></a>Параметры

*двстиле*<br/>
Задает стиль элемента управления "Кнопка". Примените любое сочетание стилей элементов управления "Счетчик" к элементу управления. Эти стили описаны в разделе [стили элементов управления "вверх/вниз](/windows/win32/Controls/up-down-control-styles) " в Windows SDK.

*rect*<br/>
Задает размер и расположение элемента управления "Кнопка". Это может быть либо объект [крект](../../atl-mfc-shared/reference/crect-class.md) , либо структура [Rect](/windows/win32/api/windef/ns-windef-rect)

*ппарентвнд*<br/>
Указатель на родительское окно элемента управления "Кнопка", обычно `CDialog` . Оно не должно иметь значение NULL.

*nID*<br/>
Задает идентификатор элемента управления "кнопка счетчика".

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если инициализация прошла успешно; в противном случае — 0.

### <a name="remarks"></a>Комментарии

`CSpinButtonCtrl`Сначала создается объект в два шага, вызывается конструктор, а затем вызывается метод `Create` , который создает элемент управления "Счетчик" и прикрепляет его к `CSpinButtonCtrl` объекту.

Чтобы создать элемент управления "Счетчик" с расширенными стилями окна, вызовите метод [CSpinButtonCtrl:: креатикс](#createex) вместо `Create` .

## <a name="cspinbuttonctrlcreateex"></a><a name="createex"></a> CSpinButtonCtrl:: Креатикс

Создает элемент управления (дочернее окно) и связывает его с `CSpinButtonCtrl` объектом.

```
virtual BOOL CreateEx(
    DWORD dwExStyle,
    DWORD dwStyle,
    const RECT& rect,
    CWnd* pParentWnd,
    UINT nID);
```

### <a name="parameters"></a>Параметры

*двексстиле*<br/>
Задает расширенный стиль создаваемого элемента управления. Список расширенных стилей Windows см. в разделе параметр *двексстиле* для [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexw) в Windows SDK.

*двстиле*<br/>
Задает стиль элемента управления "Кнопка". Примените любое сочетание стилей элементов управления "Счетчик" к элементу управления. Эти стили описаны в разделе [стили элементов управления "вверх/вниз](/windows/win32/Controls/up-down-control-styles) " в Windows SDK.

*rect*<br/>
Ссылка на структуру [Rect](/windows/win32/api/windef/ns-windef-rect) , описывающую размер и расположение создаваемого окна в клиентских координатах *ппарентвнд*.

*ппарентвнд*<br/>
Указатель на окно, которое является родительским элементом управления.

*nID*<br/>
Идентификатор дочернего окна элемента управления.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Используйте `CreateEx` вместо [CREATE](#create) , чтобы применить расширенные стили Windows, заданные WS_EX_ в расширенном стиле Windows.

## <a name="cspinbuttonctrlcspinbuttonctrl"></a><a name="cspinbuttonctrl"></a> CSpinButtonCtrl:: CSpinButtonCtrl

Формирует объект `CSpinButtonCtrl`.

```
CSpinButtonCtrl();
```

## <a name="cspinbuttonctrlgetaccel"></a><a name="getaccel"></a> CSpinButtonCtrl:: i

Получает сведения о ускорении для элемента управления "Счетчик".

```
UINT GetAccel(
    int nAccel,
    UDACCEL* pAccel) const;
```

### <a name="parameters"></a>Параметры

*накцел*<br/>
Число элементов в массиве, заданном параметром *пакцел*.

*пакцел*<br/>
Указатель на массив структур [удакцел](/windows/win32/api/commctrl/ns-commctrl-udaccel) , которые получают сведения о ускорении.

### <a name="return-value"></a>Возвращаемое значение

Число полученных структур ускорителя.

## <a name="cspinbuttonctrlgetbase"></a><a name="getbase"></a> CSpinButtonCtrl:: Polybase

Извлекает текущую базу для элемента управления "Счетчик".

```
UINT GetBase() const;
```

### <a name="return-value"></a>Возвращаемое значение

Текущее базовое значение.

## <a name="cspinbuttonctrlgetbuddy"></a><a name="getbuddy"></a> CSpinButtonCtrl:: приятель

Извлекает указатель на текущее окно контакта.

```
CWnd* GetBuddy() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на текущее окно контакта.

## <a name="cspinbuttonctrlgetpos"></a><a name="getpos"></a> CSpinButtonCtrl:: Жетпос

Извлекает текущую координату элемента управления "Счетчик".

```
int GetPos() const;  int GetPos32(LPBOOL lpbError = NULL) const;
```

### <a name="parameters"></a>Параметры

*лпберрор*<br/>
Указатель на логическое значение, равное нулю, если значение успешно получено или не равно нулю при возникновении ошибки. Если этот параметр имеет значение NULL, сообщения об ошибках не выводятся.

### <a name="return-value"></a>Возвращаемое значение

Первая версия возвращает 16-разрядное текущее расположение в слове нижнего порядка. При возникновении ошибки слово с высоким порядком не равно нулю.

Вторая версия возвращает 32-разрядное расположение.

### <a name="remarks"></a>Комментарии

При обработке возвращенного значения элемент управления обновляет свое текущее расположение на основе заголовка дружественного окна. Элемент управления возвращает ошибку, если не существует дружественного окна или если в заголовке указано недопустимое или недействительное значение.

## <a name="cspinbuttonctrlgetrange"></a><a name="getrange"></a> CSpinButtonCtrl:: Range

Получает верхние и нижние пределы (диапазон) для элемента управления "Счетчик".

```
DWORD GetRange() const;

void GetRange(
    int& lower,
    int& upper) const;

void GetRange32(
    int& lower,
    int &upper) const;
```

### <a name="parameters"></a>Параметры

*сокращение*<br/>
Ссылка на целое число, которое получает нижний предел для элемента управления.

*границ*<br/>
Ссылка на целое число, которое получает верхний предел для элемента управления.

### <a name="return-value"></a>Возвращаемое значение

Первая версия возвращает 32-разрядное значение, содержащее верхний и нижний пределы. Слово с низким приоритетом является верхним пределом для элемента управления, а максимальное слово — нижнее.

### <a name="remarks"></a>Комментарии

Функция-член `GetRange32` получает диапазон элементов управления "Счетчик" как 32-разрядное целое число.

## <a name="cspinbuttonctrlsetaccel"></a><a name="setaccel"></a> CSpinButtonCtrl:: Сетакцел

Задает ускорение для элемента управления "Счетчик".

```
BOOL SetAccel(
    int nAccel,
    UDACCEL* pAccel);
```

### <a name="parameters"></a>Параметры

*накцел*<br/>
Число структур [удакцел](/windows/win32/api/commctrl/ns-commctrl-udaccel) , заданных параметром *пакцел*.

*пакцел*<br/>
Указатель на массив структур УДАКЦЕЛ, содержащих сведения об ускорении. Элементы должны быть отсортированы в порядке возрастания на основе `nSec` элемента.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

## <a name="cspinbuttonctrlsetbase"></a><a name="setbase"></a> CSpinButtonCtrl:: Сетбасе

Задает основание для элемента управления "Счетчик".

```
int SetBase(int nBase);
```

### <a name="parameters"></a>Параметры

*нбасе*<br/>
Новое базовое значение для элемента управления. Оно может быть равно 10 для десятичного или 16 в шестнадцатеричном формате.

### <a name="return-value"></a>Возвращаемое значение

Предыдущее базовое значение при успешном выполнении или нуль, если задано недопустимое основание.

### <a name="remarks"></a>Комментарии

Базовое значение определяет, будут ли в окне собеседника отображаться числа в десятичных или шестнадцатеричных цифрах. Шестнадцатеричные числа всегда не имеют знака; десятичные числа подписываются.

## <a name="cspinbuttonctrlsetbuddy"></a><a name="setbuddy"></a> CSpinButtonCtrl:: Сетбудди

Задает окно собеседника для элемента управления "Счетчик".

```
CWnd* SetBuddy(CWnd* pWndBuddy);
```

### <a name="parameters"></a>Параметры

*пвндбудди*<br/>
Указатель на новое окно собеседника.

### <a name="return-value"></a>Возвращаемое значение

Указатель на предыдущее окно контакта.

### <a name="remarks"></a>Комментарии

Элемент управления "Счетчик" почти всегда связан с другим окном, например с элементом управления "Правка", в котором отображается некоторое содержимое. Это другое окно называется "приятель" элемента управления "Счетчик".

## <a name="cspinbuttonctrlsetpos"></a><a name="setpos"></a> CSpinButtonCtrl:: Сетпос

Задает текущую точку для элемента управления "Счетчик".

```
int SetPos(int nPos);
int SetPos32(int nPos);
```

### <a name="parameters"></a>Параметры

*nPos*<br/>
Новое расположение элемента управления. Это значение должно находиться в диапазоне, указанном верхним и нижним ограничениями для элемента управления.

### <a name="return-value"></a>Возвращаемое значение

Предыдущее расположение (16-разрядная точность для `SetPos` , 32-разрядная точность для `SetPos32` ).

### <a name="remarks"></a>Комментарии

`SetPos32` Задает 32-разрядное расположение.

## <a name="cspinbuttonctrlsetrange"></a><a name="setrange"></a> CSpinButtonCtrl:: SetRange

Задает верхний и нижний пределы (диапазон) для элемента управления "Счетчик".

```cpp
void SetRange(
    short nLower,
    short nUpper);

void SetRange32(
    int nLower,
    int nUpper);
```

### <a name="parameters"></a>Параметры

*нловер* и *нуппер*<br/>
Верхний и нижний пределы элемента управления. Для `SetRange` ограничения не могут быть больше UD_MAXVAL или меньше UD_MINVAL. Кроме того, разница между двумя ограничениями не может превышать UD_MAXVAL. `SetRange32` не накладывает ограничений на ограничения; Используйте любые целые числа.

### <a name="remarks"></a>Комментарии

Функция-член `SetRange32` задает 32-разрядный диапазон для элемента управления "Счетчик".

> [!NOTE]
> Диапазон по умолчанию для выключателя имеет максимальное значение, равное нулю (0), а минимальное значение — 100. Так как максимальное значение меньше минимального значения, щелчок стрелки вверх приведет к уменьшению места, а щелчок стрелки вниз увеличит его. `CSpinButtonCtrl::SetRange`Для изменения этих значений используйте.

## <a name="see-also"></a>См. также раздел

[Пример CMNCTRL2 для MFC](../../overview/visual-cpp-samples.md)<br/>
[CWnd, класс](../../mfc/reference/cwnd-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CSliderCtrl](../../mfc/reference/csliderctrl-class.md)
