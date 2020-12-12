---
description: 'Дополнительные сведения о: Ксизе Class'
title: Класс Ксизе
ms.date: 10/18/2018
f1_keywords:
- CSize
- ATLTYPES/ATL::CSize
- ATLTYPES/ATL::CSize::CSize
helpviewer_keywords:
- SIZE
- dimensions, MFC
- dimensions
- CSize class
ms.assetid: fb2cf85a-0bc1-46f8-892b-309c108b52ae
ms.openlocfilehash: 0a63a7e0c48948406bf5650a1b095713f701a325
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97166646"
---
# <a name="csize-class"></a>Класс Ксизе

Аналог структуры [SIZE](/windows/win32/api/windef/ns-windef-size) в ОС Windows, реализующий относительные координаты или положение.

## <a name="syntax"></a>Синтаксис

```
class CSize : public tagSIZE
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ксизе:: Ксизе](#csize)|Формирует объект `CSize`.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Ксизе:: operator —](#operator_-)|Вычитает два размера.|
|[Ксизе:: operator! =](#operator_neq)|Проверяет на неравенство между `CSize` и размером.|
|[Ксизе:: operator +](#operator_add)|Складывает два размера.|
|[Ксизе:: operator + =](#operator_add_eq)|Добавляет размер в `CSize` .|
|[Ксизе:: operator-=](#operator_-_eq)|Вычитает размер из `CSize` .|
|[Ксизе:: operator = =](#operator_eq_eq)|Проверяет равенство между `CSize` и размером.|

## <a name="remarks"></a>Комментарии

Этот класс является производным от `SIZE` структуры. Это означает, что можно передать `CSize` в параметр, который вызывает метод для `SIZE` и что элементы данных `SIZE` структуры являются доступными элементами данных `CSize` .

`cx`Члены и `cy` `SIZE` (и `CSize` ) являются открытыми. Кроме того, `CSize` реализует функции элементов для управления `SIZE` структурой.

> [!NOTE]
> Дополнительные сведения о общих классах служебной программы (например `CSize` ,) см. в разделе [Общие классы](../../atl-mfc-shared/atl-mfc-shared-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`tagSIZE`

`CSize`

## <a name="requirements"></a>Требования

**Заголовок:** атлтипес. h

## <a name="csizecsize"></a><a name="csize"></a> Ксизе:: Ксизе

Формирует объект `CSize`.

```
CSize() throw();
CSize( int initCX, int initCY) throw();
CSize( SIZE initSize) throw();
CSize( POINT initPt) throw();
CSize( DWORD dwSize) throw();
```

### <a name="parameters"></a>Параметры

*инитккс*<br/>
Задает `cx` элемент для `CSize` .

*инитци*<br/>
Задает `cy` элемент для `CSize` .

*initSize*<br/>
Структура [размера](/windows/win32/api/windef/ns-windef-size) или `CSize` объект, используемый для инициализации `CSize` .

*инитпт*<br/>
Структура [точки](/windows/win32/api/windef/ns-windef-point) или `CPoint` объект, используемый для инициализации `CSize` .

*двсизе*<br/>
DWORD, используемый для инициализации `CSize` . Слово с низким приоритетом является `cx` элементом, а старшим словом является `cy` элемент.

### <a name="remarks"></a>Комментарии

Значение, если аргументы не заданы `cx` и `cy` инициализируются нулем.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#97](../../atl-mfc-shared/codesnippet/cpp/csize-class_1.cpp)]

## <a name="csizeoperator-"></a><a name="operator_eq_eq"></a> Ксизе:: operator = =

Проверяет равенство двух размеров.

```
BOOL operator==(SIZE size) const throw();
```

### <a name="remarks"></a>Комментарии

Возвращает ненулевое значение, если размеры равны, осервизе 0.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#98](../../atl-mfc-shared/codesnippet/cpp/csize-class_2.cpp)]

## <a name="csizeoperator-"></a><a name="operator_neq"></a> Ксизе:: operator! =

Проверяет на неравенство между двумя размерами.

```
BOOL operator!=(SIZE size) const throw();
```

### <a name="remarks"></a>Комментарии

Возвращает ненулевое значение, если размеры не равны; в противном случае — значение 0.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#99](../../atl-mfc-shared/codesnippet/cpp/csize-class_3.cpp)]

## <a name="csizeoperator-"></a><a name="operator_add_eq"></a> Ксизе:: operator + =

Добавляет размер к этому `CSize` .

```cpp
void operator+=(SIZE size) throw();
```

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#100](../../atl-mfc-shared/codesnippet/cpp/csize-class_4.cpp)]

## <a name="csizeoperator--"></a><a name="operator_-_eq"></a> Ксизе:: operator-=

Вычитает размер из этого `CSize` .

```cpp
void operator-=(SIZE size) throw();
```

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#101](../../atl-mfc-shared/codesnippet/cpp/csize-class_5.cpp)]

## <a name="csizeoperator-"></a><a name="operator_add"></a> Ксизе:: operator +

Эти операторы добавляют это `CSize` значение к значению параметра.

```
CSize operator+(SIZE size) const throw();
CPoint operator+(POINT point) const throw();
CRect operator+(const RECT* lpRect) const throw();
```

### <a name="remarks"></a>Комментарии

См. следующие описания отдельных операторов.

- **оператор + (** *size* **)**

  Эта операция добавляет два `CSize` значения.

- **оператор + (** *Point* **)**

  Эта операция смещает (перемещает) значение [точки](/windows/win32/api/windef/ns-windef-point) (или [CPoint](../../atl-mfc-shared/reference/cpoint-class.md)) на это `CSize` значение. `cx`Члены и `cy` этого `CSize` значения добавляются к `x` `y` элементам данных и `POINT` значения. Он аналогичен версии [CPoint:: operator +](../../atl-mfc-shared/reference/cpoint-class.md#operator_add) , принимающей параметр [size](/windows/win32/api/windef/ns-windef-size) .

- **operator + (** *лпрект* **)**

   Эта операция смещает (перемещает) значение [Rect](/windows/win32/api/windef/ns-windef-rect) (или [крект](../../atl-mfc-shared/reference/crect-class.md)) на это `CSize` значение. `cx`Элементы и `cy` этого `CSize` значения добавляются в `left` элементы данных,, `top` `right` и `bottom` `RECT` значения. Он аналогичен версии [крект:: operator +](../../atl-mfc-shared/reference/crect-class.md#operator_add) , принимающей параметр [size](/windows/win32/api/windef/ns-windef-size) .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#102](../../atl-mfc-shared/codesnippet/cpp/csize-class_6.cpp)]

## <a name="csizeoperator--"></a><a name="operator_-"></a> Ксизе:: operator —

Первые три из этих операторов вычитают это `CSize` значение в качестве значения параметра.

```
CSize operator-(SIZE size) const throw();
CPoint operator-(POINT point) const throw();
CRect operator-(const RECT* lpRect) const throw();
CSize operator-() const throw();
```

### <a name="remarks"></a>Комментарии

Четвертый оператор, унарный минус, изменяет знак `CSize` значения. См. следующие описания отдельных операторов.

- **operator — (** *size* **)**

  Эта операция вычитает два `CSize` значения.

- **оператор-(** *Point* **)**

  Эта операция смещает (перемещает) значение [точки](/windows/win32/api/windef/ns-windef-point) или [CPoint](../../atl-mfc-shared/reference/cpoint-class.md) на обратный инверсия этого `CSize` значения. `cx`Значение и `cy` для этого `CSize` значения вычитаются из `x` `y` элементов данных и в `POINT` значении. Он аналогичен версии [CPoint:: operator-](../../atl-mfc-shared/reference/cpoint-class.md#operator_-) , принимающей параметр [size](/windows/win32/api/windef/ns-windef-size) .

- **operator — (** *лпрект* **)**

  Эта операция смещает (перемещает) значение [Rect](/windows/win32/api/windef/ns-windef-rect) или [крект](../../atl-mfc-shared/reference/crect-class.md) на обратный инверсия этого `CSize` значения. `cx`Элементы и `cy` этого `CSize` значения вычитаются из `left` элементов данных,, `top` `right` и `bottom` `RECT` значения. Он аналогичен версии [крект:: operator-](../../atl-mfc-shared/reference/crect-class.md#operator_-) , принимающей параметр [size](/windows/win32/api/windef/ns-windef-size) .

- **operator-()**

  Эта операция возвращает добавочное обратное значение этого `CSize` значения.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#103](../../atl-mfc-shared/codesnippet/cpp/csize-class_7.cpp)]

## <a name="see-also"></a>См. также раздел

[Образец MDI-формы MFC](../../overview/visual-cpp-samples.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Крект](../../atl-mfc-shared/reference/crect-class.md)<br/>
[Класс CPoint](../../atl-mfc-shared/reference/cpoint-class.md)
