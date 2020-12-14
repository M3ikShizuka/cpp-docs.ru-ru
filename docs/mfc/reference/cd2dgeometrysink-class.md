---
description: 'Дополнительные сведения о: CD2DGeometrySink Class'
title: Класс CD2DGeometrySink
ms.date: 11/04/2016
f1_keywords:
- CD2DGeometrySink
- AFXRENDERTARGET/CD2DGeometrySink
- AFXRENDERTARGET/CD2DGeometrySink::CD2DGeometrySink
- AFXRENDERTARGET/CD2DGeometrySink::AddArc
- AFXRENDERTARGET/CD2DGeometrySink::AddBezier
- AFXRENDERTARGET/CD2DGeometrySink::AddBeziers
- AFXRENDERTARGET/CD2DGeometrySink::AddLine
- AFXRENDERTARGET/CD2DGeometrySink::AddLines
- AFXRENDERTARGET/CD2DGeometrySink::AddQuadraticBezier
- AFXRENDERTARGET/CD2DGeometrySink::AddQuadraticBeziers
- AFXRENDERTARGET/CD2DGeometrySink::BeginFigure
- AFXRENDERTARGET/CD2DGeometrySink::Close
- AFXRENDERTARGET/CD2DGeometrySink::EndFigure
- AFXRENDERTARGET/CD2DGeometrySink::Get
- AFXRENDERTARGET/CD2DGeometrySink::IsValid
- AFXRENDERTARGET/CD2DGeometrySink::SetFillMode
- AFXRENDERTARGET/CD2DGeometrySink::SetSegmentFlags
- AFXRENDERTARGET/CD2DGeometrySink::m_pSink
helpviewer_keywords:
- CD2DGeometrySink [MFC], CD2DGeometrySink
- CD2DGeometrySink [MFC], AddArc
- CD2DGeometrySink [MFC], AddBezier
- CD2DGeometrySink [MFC], AddBeziers
- CD2DGeometrySink [MFC], AddLine
- CD2DGeometrySink [MFC], AddLines
- CD2DGeometrySink [MFC], AddQuadraticBezier
- CD2DGeometrySink [MFC], AddQuadraticBeziers
- CD2DGeometrySink [MFC], BeginFigure
- CD2DGeometrySink [MFC], Close
- CD2DGeometrySink [MFC], EndFigure
- CD2DGeometrySink [MFC], Get
- CD2DGeometrySink [MFC], IsValid
- CD2DGeometrySink [MFC], SetFillMode
- CD2DGeometrySink [MFC], SetSegmentFlags
- CD2DGeometrySink [MFC], m_pSink
ms.assetid: e5e07f41-0343-4ab1-9d6b-8c62ed33c04a
ms.openlocfilehash: e7916cdb39272e924a9d6ef6c0a8322d8ce6fb1f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193426"
---
# <a name="cd2dgeometrysink-class"></a>Класс CD2DGeometrySink

Оболочка для ID2D1GeometrySink.

## <a name="syntax"></a>Синтаксис

```
class CD2DGeometrySink;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DGeometrySink::CD2DGeometrySink](#cd2dgeometrysink)|Конструирует объект CD2DGeometrySink из объекта CD2DPathGeometry.|
|[CD2DGeometrySink:: ~ CD2DGeometrySink](#_dtorcd2dgeometrysink)|Деструктор Вызывается при уничтожении объекта приемника геометрии D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DGeometrySink:: Аддарк](#addarc)|Добавляет единичную дугу к геометрии контура|
|[CD2DGeometrySink:: Аддбезиер](#addbezier)|Создает кривую Безье третьего порядка между текущей и заданной конечной точками.|
|[CD2DGeometrySink:: Аддбезиерс](#addbeziers)|Создает последовательность кривых Безье третьего порядка и добавляет их в приемник геометрии.|
|[CD2DGeometrySink:: Аддлине](#addline)|Создает отрезок линии между текущей точкой и заданной конечной точкой и добавляет его в приемник геометрии.|
|[CD2DGeometrySink:: Аддлинес](#addlines)|Создает последовательность строк с использованием указанных точек и добавляет их в приемник геометрии.|
|[CD2DGeometrySink:: Аддкуадратикбезиер](#addquadraticbezier)|Создает кривую Безье второго порядка между текущей и заданной конечной точками.|
|[CD2DGeometrySink:: Аддкуадратикбезиерс](#addquadraticbeziers)|Добавляет последовательность сегментов Безье второго порядка в качестве массива в одном вызове.|
|[CD2DGeometrySink:: Бегинфигуре](#beginfigure)|Запускает новую фигуру в указанной точке.|
|[CD2DGeometrySink:: Close](#close)|Закрывает приемник геометрии|
|[CD2DGeometrySink:: Ендфигуре](#endfigure)|Завершает текущую фигуру; При необходимости закрывает его.|
|[CD2DGeometrySink:: Get](#get)|Возвращает интерфейс ID2D1GeometrySink|
|[CD2DGeometrySink:: IsValid](#isvalid)|Проверяет допустимость приемника геометрии|
|[CD2DGeometrySink:: Сетфиллмоде](#setfillmode)|Указывает метод, используемый для определения того, какие точки находятся внутри геометрии, описываемой этим геометрическим объектом, и какие точки находятся за пределами.|
|[CD2DGeometrySink:: Сетсегментфлагс](#setsegmentflags)|Задает параметры обводки и объединения, применяемые к новым сегментам, добавленным в приемник геометрии.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DGeometrySink:: operator ID2D1GeometrySink *](#operator_id2d1geometrysink_star)|Возвращает интерфейс ID2D1GeometrySink|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DGeometrySink:: m_pSink](#m_psink)|Указатель на ID2D1GeometrySink.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CD2DGeometrySink`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dgeometrysinkcd2dgeometrysink"></a><a name="_dtorcd2dgeometrysink"></a> CD2DGeometrySink:: ~ CD2DGeometrySink

Деструктор Вызывается при уничтожении объекта приемника геометрии D2D.

```
virtual ~CD2DGeometrySink();
```

## <a name="cd2dgeometrysinkaddarc"></a><a name="addarc"></a> CD2DGeometrySink:: Аддарк

Добавляет единичную дугу к геометрии контура

```cpp
void AddArc(const D2D1_ARC_SEGMENT& arc);
```

### <a name="parameters"></a>Параметры

*дуги*<br/>
Сегмент дуги, добавляемый на фигуру

## <a name="cd2dgeometrysinkaddbezier"></a><a name="addbezier"></a> CD2DGeometrySink:: Аддбезиер

Создает кривую Безье третьего порядка между текущей и заданной конечной точками.

```cpp
void AddBezier(const D2D1_BEZIER_SEGMENT& bezier);
```

### <a name="parameters"></a>Параметры

*Безье*<br/>
Структура, описывающая контрольные точки и конечную точку добавляемой кривой Безье.

## <a name="cd2dgeometrysinkaddbeziers"></a><a name="addbeziers"></a> CD2DGeometrySink:: Аддбезиерс

Создает последовательность кривых Безье третьего порядка и добавляет их в приемник геометрии.

```cpp
void AddBeziers(
    const CArray<D2D1_BEZIER_SEGMENT,
    D2D1_BEZIER_SEGMENT>& beziers);
```

### <a name="parameters"></a>Параметры

*кривые Безье*<br/>
Массив сегментов Безье, описывающих создаваемые кривые Безье. Кривая берется из текущей точки геометрического приемника (конечной точки последнего рисуемого сегмента или расположения, заданного параметром Бегинфигуре) в конечную точку первого сегмента Безье в массиве. Если массив содержит дополнительные сегменты Безье, каждый последующий сегмент Безье использует конечную точку предыдущего сегмента Безье в качестве начальной точки.

## <a name="cd2dgeometrysinkaddline"></a><a name="addline"></a> CD2DGeometrySink:: Аддлине

Создает отрезок линии между текущей точкой и заданной конечной точкой и добавляет его в приемник геометрии.

```cpp
void AddLine(CD2DPointF point);
```

### <a name="parameters"></a>Параметры

*точки*<br/>
Конечная точка рисуемой линии.

## <a name="cd2dgeometrysinkaddlines"></a><a name="addlines"></a> CD2DGeometrySink:: Аддлинес

Создает последовательность строк с использованием указанных точек и добавляет их в приемник геометрии.

```cpp
void AddLines(
    const CArray<CD2DPointF,
    CD2DPointF>& points);
```

### <a name="parameters"></a>Параметры

*точки*<br/>
Массив из одной или нескольких точек, описывающих рисуемые линии. Линия отрисовывается из текущей точки геометрического приемника (конечной точки последнего рисуемого сегмента или расположения, заданного параметром Бегинфигуре) до первой точки в массиве. Если массив содержит дополнительные точки, линия рисуется от первой точки к второй точке массива, от второй до третьей точки и т. д. Массив из последовательности конечных точек рисуемых линий.

## <a name="cd2dgeometrysinkaddquadraticbezier"></a><a name="addquadraticbezier"></a> CD2DGeometrySink:: Аддкуадратикбезиер

Создает кривую Безье второго порядка между текущей и заданной конечной точками.

```cpp
void AddQuadraticBezier(const D2D1_QUADRATIC_BEZIER_SEGMENT& bezier);
```

### <a name="parameters"></a>Параметры

*Безье*<br/>
Структура, описывающая контрольную точку и конечную точку добавляемой кривой Безье.

## <a name="cd2dgeometrysinkaddquadraticbeziers"></a><a name="addquadraticbeziers"></a> CD2DGeometrySink:: Аддкуадратикбезиерс

Добавляет последовательность сегментов Безье второго порядка в качестве массива в одном вызове.

```cpp
void AddQuadraticBeziers(
    const CArray<D2D1_QUADRATIC_BEZIER_SEGMENT,
    D2D1_QUADRATIC_BEZIER_SEGMENT>& beziers);
```

### <a name="parameters"></a>Параметры

*кривые Безье*<br/>
Массив последовательности сегментов Безье второго порядка.

## <a name="cd2dgeometrysinkbeginfigure"></a><a name="beginfigure"></a> CD2DGeometrySink:: Бегинфигуре

Запускает новую фигуру в указанной точке.

```cpp
void BeginFigure(
    CD2DPointF startPoint,
    D2D1_FIGURE_BEGIN figureBegin);
```

### <a name="parameters"></a>Параметры

*startPoint*<br/>
Точка, с которой начинается новая фигура.

*фигуребегин*<br/>
Указывает, должна ли новая фигура быть пустой или заполненной.

## <a name="cd2dgeometrysinkcd2dgeometrysink"></a><a name="cd2dgeometrysink"></a> CD2DGeometrySink::CD2DGeometrySink

Конструирует объект CD2DGeometrySink из объекта CD2DPathGeometry.

```
CD2DGeometrySink(CD2DPathGeometry& pathGeometry);
```

### <a name="parameters"></a>Параметры

*pathGeometry*<br/>
Существующий объект CD2DPathGeometry.

## <a name="cd2dgeometrysinkclose"></a><a name="close"></a> CD2DGeometrySink:: Close

Закрывает приемник геометрии

```
BOOL Close();
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение в случае успешного выполнения; в противном случае — FALSE.

## <a name="cd2dgeometrysinkendfigure"></a><a name="endfigure"></a> CD2DGeometrySink:: Ендфигуре

Завершает текущую фигуру; При необходимости закрывает его.

```cpp
void EndFigure(D2D1_FIGURE_END figureEnd);
```

### <a name="parameters"></a>Параметры

*фигуринд*<br/>
Значение, указывающее, закрыта ли текущая фигура. Если рисунок закрыт, линия отображается между текущей точкой и начальной точкой, заданной параметром Бегинфигуре.

## <a name="cd2dgeometrysinkget"></a><a name="get"></a> CD2DGeometrySink:: Get

Возвращает интерфейс ID2D1GeometrySink

```
ID2D1GeometrySink* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1GeometrySink или значение NULL, если объект еще не инициализирован.

## <a name="cd2dgeometrysinkisvalid"></a><a name="isvalid"></a> CD2DGeometrySink:: IsValid

Проверяет допустимость приемника геометрии

```
BOOL IsValid() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если приемник геометрии является допустимым; в противном случае — FALSE.

## <a name="cd2dgeometrysinkm_psink"></a><a name="m_psink"></a> CD2DGeometrySink:: m_pSink

Указатель на ID2D1GeometrySink.

```
ID2D1GeometrySink* m_pSink;
```

## <a name="cd2dgeometrysinkoperator-id2d1geometrysink"></a><a name="operator_id2d1geometrysink_star"></a> CD2DGeometrySink:: operator ID2D1GeometrySink *

Возвращает интерфейс ID2D1GeometrySink

```
operator ID2D1GeometrySink*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1GeometrySink или значение NULL, если объект еще не инициализирован.

## <a name="cd2dgeometrysinksetfillmode"></a><a name="setfillmode"></a> CD2DGeometrySink:: Сетфиллмоде

Указывает метод, используемый для определения того, какие точки находятся внутри геометрии, описываемой этим геометрическим объектом, и какие точки находятся за пределами.

```cpp
void SetFillMode(D2D1_FILL_MODE fillMode);
```

### <a name="parameters"></a>Параметры

*филлмоде*<br/>
Метод, используемый для определения того, является ли заданная точка частью геометрии.

## <a name="cd2dgeometrysinksetsegmentflags"></a><a name="setsegmentflags"></a> CD2DGeometrySink:: Сетсегментфлагс

Задает параметры обводки и объединения, применяемые к новым сегментам, добавленным в приемник геометрии.

```cpp
void SetSegmentFlags(D2D1_PATH_SEGMENT vertexFlags);
```

### <a name="parameters"></a>Параметры

*вертексфлагс*<br/>
Параметры Stroke и JOIN, применяемые к новым сегментам, добавленным в приемник геометрии.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
