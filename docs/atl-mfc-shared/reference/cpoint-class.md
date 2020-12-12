---
description: 'Дополнительные сведения о: CPoint Class'
title: Класс CPoint
ms.date: 11/04/2016
f1_keywords:
- CPoint
- ATLTYPES/ATL::CPoint
- ATLTYPES/ATL::CPoint::CPoint
- ATLTYPES/ATL::CPoint::Offset
helpviewer_keywords:
- LPPOINT structure
- POINT structure
- CPoint class
ms.assetid: a6d4db93-35cc-444d-9221-c3e160f6edaa
ms.openlocfilehash: 9d1c6ecb628e4d47d80503bb7a441efc4deb1252
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97166763"
---
# <a name="cpoint-class"></a>Класс CPoint

Как и в структуре `POINT` Windows.

## <a name="syntax"></a>Синтаксис

```
class CPoint : public tagPOINT
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CPoint:: CPoint](#cpoint)|Создает документ `CPoint`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CPoint:: offset](#offset)|Добавляет значения в `x` элементы и `y` объекта `CPoint` .|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CPoint:: operator —](#operator_-)|Возвращает разность `CPoint` между и размером, или отрицанием точки, либо разность размера между двумя точками или смещение на отрицательный размер.|
|[CPoint:: operator! =](#operator_neq)|Проверяет на неравенство между двумя точками.|
|[CPoint:: operator +](#operator_add)|Возвращает сумму, а также `CPoint` размер или точку или `CRect` смещение на размер.|
|[CPoint:: operator + =](#operator_add_eq)|Смещение `CPoint` путем добавления размера или точки.|
|[CPoint:: operator-=](#operator_-_eq)|Смещение `CPoint` путем вычитания размера или точки.|
|[CPoint:: operator = =](#operator_eq_eq)|Проверяет равенство между двумя точками.|

## <a name="remarks"></a>Комментарии

Он также включает функции элементов для управления `CPoint` структурами и [точек](/windows/win32/api/windef/ns-windef-point) .

`CPoint`Объект можно использовать везде, где `POINT` используется структура. Операторы этого класса, взаимодействующие с "size", принимают либо объекты [ксизе](../../atl-mfc-shared/reference/csize-class.md) , либо структуры [размера](/windows/win32/api/windef/ns-windef-size) , так как эти два являются взаимозаменяемыми.

> [!NOTE]
> Этот класс является производным от `tagPOINT` структуры. (Имя `tagPOINT` для структуры является менее часто используемым именем `POINT` .) Это означает, что элементы данных `POINT` структуры `x` и `y` являются доступными элементами данных `CPoint` .

> [!NOTE]
> Дополнительные сведения о общих классах служебной программы (например `CPoint` ,) см. в разделе [Общие классы](../../atl-mfc-shared/atl-mfc-shared-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`tagPOINT`

`CPoint`

## <a name="requirements"></a>Требования

**Заголовок:** атлтипес. h

## <a name="cpointcpoint"></a><a name="cpoint"></a> CPoint:: CPoint

Формирует объект `CPoint`.

```
CPoint() throw();
CPoint(int initX, int initY) throw();
CPoint(POINT initPt) throw();
CPoint(SIZE initSize) throw();
CPoint(LPARAM dwPoint) throw();
```

### <a name="parameters"></a>Параметры

*иниткс*<br/>
Определяет значение члена `x` структуры `CPoint`.

*Инициализация*<br/>
Определяет значение члена `y` структуры `CPoint`.

*инитпт*<br/>
Структура [точки](/windows/win32/api/windef/ns-windef-point) или `CPoint` , указывающая значения, используемые для инициализации `CPoint` .

*initSize*<br/>
Структура [размера](/windows/win32/api/windef/ns-windef-size) или [ксизе](../../atl-mfc-shared/reference/csize-class.md) , указывающая значения, используемые для инициализации `CPoint` .

*двпоинт*<br/>
Задает `x` элементу неупорядоченное слово *двпоинт* , а элемент — в `y` слове *двпоинт* с высоким приоритетом.

### <a name="remarks"></a>Комментарии

Если аргументы не указаны, для членов `x` и `y` задается значение 0.

### <a name="example"></a>Пример

```cpp
CPoint   ptTopLeft(0, 0);
// works from a POINT, too

POINT   ptHere;
ptHere.x = 35;
ptHere.y = 95;

CPoint   ptMFCHere(ptHere);

// works from a SIZE
SIZE   sHowBig;
sHowBig.cx = 300;
sHowBig.cy = 10;

CPoint ptMFCBig(sHowBig);
// or from a DWORD

DWORD   dwSize;
dwSize = MAKELONG(35, 95);

CPoint ptFromDouble(dwSize);
ASSERT(ptFromDouble == ptMFCHere);
```

## <a name="cpointoffset"></a><a name="offset"></a> CPoint:: offset

Добавляет значения в `x` элементы и `y` объекта `CPoint` .

```cpp
void Offset(int xOffset, int yOffset) throw();
void Offset(POINT point) throw();
void Offset(SIZE size) throw();
```

### <a name="parameters"></a>Параметры

*ксоффсет*<br/>
Задает величину смещения `x` элемента `CPoint` .

*йоффсет*<br/>
Задает величину смещения `y` элемента `CPoint` .

*точки*<br/>
Задает величину [](/windows/win32/api/windef/ns-windef-point) `CPoint` смещения для `CPoint` .

*size*<br/>
Задает величину ( [size](/windows/win32/api/windef/ns-windef-size) или [ксизе](../../atl-mfc-shared/reference/csize-class.md)) смещения `CPoint` .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#28](../../atl-mfc-shared/codesnippet/cpp/cpoint-class_1.cpp)]

## <a name="cpointoperator-"></a><a name="operator_eq_eq"></a> CPoint:: operator = =

Проверяет равенство между двумя точками.

```
BOOL operator==(POINT point) const throw();
```

### <a name="parameters"></a>Параметры

*точки*<br/>
Содержит структуру [точек](/windows/win32/api/windef/ns-windef-point) или `CPoint` объект.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если точки равны; в противном случае — 0.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#29](../../atl-mfc-shared/codesnippet/cpp/cpoint-class_2.cpp)]

## <a name="cpointoperator-"></a><a name="operator_neq"></a> CPoint:: operator! =

Проверяет на неравенство между двумя точками.

```
BOOL operator!=(POINT point) const throw();
```

### <a name="parameters"></a>Параметры

*точки*<br/>
Содержит структуру [точек](/windows/win32/api/windef/ns-windef-point) или `CPoint` объект.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если точки не равны; в противном случае — 0.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#30](../../atl-mfc-shared/codesnippet/cpp/cpoint-class_3.cpp)]

## <a name="cpointoperator-"></a><a name="operator_add_eq"></a> CPoint:: operator + =

Первая перегрузка добавляет размер в `CPoint` .

```cpp
void operator+=(SIZE size) throw();
void operator+=(POINT point) throw();
```

### <a name="parameters"></a>Параметры

*size*<br/>
Содержит структуру [размера](/windows/win32/api/windef/ns-windef-size) или объект [ксизе](../../atl-mfc-shared/reference/csize-class.md) .

*точки*<br/>
Содержит структуру [точек](/windows/win32/api/windef/ns-windef-point) или объект [CPoint](../../atl-mfc-shared/reference/cpoint-class.md) .

### <a name="remarks"></a>Комментарии

Вторая перегрузка добавляет точку в `CPoint` .

В обоих случаях сложение выполняется путем добавления `x` элемента (или `cx` ) правого операнда к `x` элементу `CPoint` и добавления `y` элемента (или `cy` ) правого операнда в `y` элемент `CPoint` .

Например, добавление `CPoint(5, -7)` в переменную, которая содержит, `CPoint(30, 40)` изменяет переменную на `CPoint(35, 33)` .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#31](../../atl-mfc-shared/codesnippet/cpp/cpoint-class_4.cpp)]

## <a name="cpointoperator--"></a><a name="operator_-_eq"></a> CPoint:: operator-=

Первая перегрузка вычитает размер из `CPoint` .

```cpp
void operator-=(SIZE size) throw();
void operator-=(POINT point) throw();
```

### <a name="parameters"></a>Параметры

*size*<br/>
Содержит структуру [размера](/windows/win32/api/windef/ns-windef-size) или объект [ксизе](../../atl-mfc-shared/reference/csize-class.md) .

*точки*<br/>
Содержит структуру [точек](/windows/win32/api/windef/ns-windef-point) или объект [CPoint](../../atl-mfc-shared/reference/cpoint-class.md) .

### <a name="remarks"></a>Комментарии

Вторая перегрузка вычитает точку из `CPoint` .

В обоих случаях вычитание выполняется путем вычитания `x` элемента (или `cx` ) правого операнда из `x` элемента `CPoint` и вычитания `y` элемента (или `cy` ) правого операнда из `y` элемента `CPoint` .

Например, вычитание `CPoint(5, -7)` из переменной, которая содержит, `CPoint(30, 40)` изменяет переменную на `CPoint(25, 47)` .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#32](../../atl-mfc-shared/codesnippet/cpp/cpoint-class_5.cpp)]

## <a name="cpointoperator-"></a><a name="operator_add"></a> CPoint:: operator +

Этот оператор используется для смещения `CPoint` `CPoint` `CSize` объекта или, а также для смещения a на `CRect` `CPoint` .

```
CPoint operator+(SIZE size) const throw();
CPoint operator+(POINT point) const throw();
CRect operator+(const RECT* lpRect) const throw();
```

### <a name="parameters"></a>Параметры

*size*<br/>
Содержит структуру [размера](/windows/win32/api/windef/ns-windef-size) или объект [ксизе](../../atl-mfc-shared/reference/csize-class.md) .

*точки*<br/>
Содержит структуру [точек](/windows/win32/api/windef/ns-windef-point) или объект [CPoint](../../atl-mfc-shared/reference/cpoint-class.md) .

*лпрект*<br/>
Содержит указатель на структуру [Rect](/windows/win32/api/windef/ns-windef-rect) или объект [крект](../../atl-mfc-shared/reference/crect-class.md) .

### <a name="return-value"></a>Возвращаемое значение

Объект `CPoint` , который смещается по размеру, `CPoint` смещению по точке или `CRect` смещению на точку.

### <a name="remarks"></a>Комментарии

Например, использование одной из первых двух перегрузок для смещения точки на `CPoint(25, -19)` точку `CPoint(15, 5)` или размер `CSize(15, 5)` возвращает значение `CPoint(40, -14)` .

Добавление прямоугольника в точку возвращает прямоугольник после смещения `x` значениями и, `y` заданными в точке. Например, использование последней перегрузки для смещения прямоугольника на `CRect(125, 219, 325, 419)` точку `CPoint(25, -19)` возвращает `CRect(150, 200, 350, 400)` .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#33](../../atl-mfc-shared/codesnippet/cpp/cpoint-class_6.cpp)]

## <a name="cpointoperator--"></a><a name="operator_-"></a> CPoint:: operator —

Используйте одну из первых двух перегрузок для вычитания `CPoint` объекта или `CSize` из `CPoint` .

```
CSize operator-(POINT point) const throw();
CPoint operator-(SIZE size) const throw();
CRect operator-(const RECT* lpRect) const throw();
CPoint operator-() const throw();
```

### <a name="parameters"></a>Параметры

*точки*<br/>
Структура [Point](/windows/win32/api/windef/ns-windef-point) или объект [CPoint](../../atl-mfc-shared/reference/cpoint-class.md) .

*size*<br/>
Структура [размера](/windows/win32/api/windef/ns-windef-size) или объект [ксизе](../../atl-mfc-shared/reference/csize-class.md) .

*лпрект*<br/>
Указатель на структуру [Rect](/windows/win32/api/windef/ns-windef-rect) или объект [крект](../../atl-mfc-shared/reference/crect-class.md) .

### <a name="return-value"></a>Возвращаемое значение

Объект `CSize` , который представляет собой разность между двумя точками, `CPoint` которая смещается от отрицания размера,, `CRect` который смещается на отрицание точки, или `CPoint` , который является отрицанием точки.

### <a name="remarks"></a>Комментарии

Третья перегрузка смещает a на `CRect` противоположность `CPoint` . Наконец, используйте унарный оператор для отрицания `CPoint` .

Например, с помощью первой перегрузки можно найти разницу между двумя точками `CPoint(25, -19)` и `CPoint(15, 5)` возвратами `CSize(10, -24)` .

Вычитание `CSize` из `CPoint` выполняет то же вычисление, что и выше, но возвращает `CPoint` объект, а не `CSize` объект. Например, используйте вторую перегрузку для определения разницы между точкой `CPoint(25, -19)` и размером `CSize(15, 5)` `CPoint(10, -24)` .

Вычитание прямоугольника из точки возвращает смещение прямоугольника по отрицательным `x` `y` значениям и, указанным в точке. Например, использование последней перегрузки для смещения прямоугольника на `CRect(125, 200, 325, 400)` точка `CPoint(25, -19)` возвращает `CRect(100, 219, 300, 419)` .

Используйте унарный оператор для отрицания точки. Например, использование унарного оператора с точкой `CPoint(25, -19)` возвращает `CPoint(-25, 19)` .

### <a name="example"></a>Пример

[!code-cpp[NVC_ATLMFC_Utilities#34](../../atl-mfc-shared/codesnippet/cpp/cpoint-class_7.cpp)]

## <a name="see-also"></a>См. также раздел

[Образец MDI-формы MFC](../../overview/visual-cpp-samples.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Структура точки](/windows/win32/api/windef/ns-windef-point)<br/>
[Класс Крект](../../atl-mfc-shared/reference/crect-class.md)<br/>
[Класс Ксизе](../../atl-mfc-shared/reference/csize-class.md)
