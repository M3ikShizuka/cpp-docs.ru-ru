---
description: 'Дополнительные сведения о: CD2DGeometry Class'
title: Класс CD2DGeometry
ms.date: 11/04/2016
f1_keywords:
- CD2DGeometry
- AFXRENDERTARGET/CD2DGeometry
- AFXRENDERTARGET/CD2DGeometry::CD2DGeometry
- AFXRENDERTARGET/CD2DGeometry::Attach
- AFXRENDERTARGET/CD2DGeometry::CombineWithGeometry
- AFXRENDERTARGET/CD2DGeometry::CompareWithGeometry
- AFXRENDERTARGET/CD2DGeometry::ComputeArea
- AFXRENDERTARGET/CD2DGeometry::ComputeLength
- AFXRENDERTARGET/CD2DGeometry::ComputePointAtLength
- AFXRENDERTARGET/CD2DGeometry::Destroy
- AFXRENDERTARGET/CD2DGeometry::Detach
- AFXRENDERTARGET/CD2DGeometry::FillContainsPoint
- AFXRENDERTARGET/CD2DGeometry::Get
- AFXRENDERTARGET/CD2DGeometry::GetBounds
- AFXRENDERTARGET/CD2DGeometry::GetWidenedBounds
- AFXRENDERTARGET/CD2DGeometry::IsValid
- AFXRENDERTARGET/CD2DGeometry::Outline
- AFXRENDERTARGET/CD2DGeometry::Simplify
- AFXRENDERTARGET/CD2DGeometry::StrokeContainsPoint
- AFXRENDERTARGET/CD2DGeometry::Tessellate
- AFXRENDERTARGET/CD2DGeometry::Widen
- AFXRENDERTARGET/CD2DGeometry::m_pGeometry
helpviewer_keywords:
- CD2DGeometry [MFC], CD2DGeometry
- CD2DGeometry [MFC], Attach
- CD2DGeometry [MFC], CombineWithGeometry
- CD2DGeometry [MFC], CompareWithGeometry
- CD2DGeometry [MFC], ComputeArea
- CD2DGeometry [MFC], ComputeLength
- CD2DGeometry [MFC], ComputePointAtLength
- CD2DGeometry [MFC], Destroy
- CD2DGeometry [MFC], Detach
- CD2DGeometry [MFC], FillContainsPoint
- CD2DGeometry [MFC], Get
- CD2DGeometry [MFC], GetBounds
- CD2DGeometry [MFC], GetWidenedBounds
- CD2DGeometry [MFC], IsValid
- CD2DGeometry [MFC], Outline
- CD2DGeometry [MFC], Simplify
- CD2DGeometry [MFC], StrokeContainsPoint
- CD2DGeometry [MFC], Tessellate
- CD2DGeometry [MFC], Widen
- CD2DGeometry [MFC], m_pGeometry
ms.assetid: 3f95054b-fdb8-4e87-87f2-9fc3df7279ec
ms.openlocfilehash: 2c902554ba5377ce9f7a4a481d4001a9ef7a47f9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193452"
---
# <a name="cd2dgeometry-class"></a>Класс CD2DGeometry

Оболочка для ID2D1Geometry.

## <a name="syntax"></a>Синтаксис

```
class CD2DGeometry : public CD2DResource;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DGeometry::CD2DGeometry](#cd2dgeometry)|Конструирует объект CD2DGeometry.|
|[CD2DGeometry:: ~ CD2DGeometry](#_dtorcd2dgeometry)|Деструктор Вызывается при уничтожении объекта геометрии D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DGeometry:: Attach](#attach)|Присоединяет существующий интерфейс ресурсов к объекту|
|[CD2DGeometry:: Комбиневисжеометри](#combinewithgeometry)|Объединяет эту геометрию с указанной геометрией и сохраняет результат в ID2D1SimplifiedGeometrySink.|
|[CD2DGeometry:: Компаревисжеометри](#comparewithgeometry)|Описывает пересечение между этой геометрией и заданной геометрией. Сравнение выполняется с заданной допускной обпрозрачкой.|
|[CD2DGeometry:: Компутеареа](#computearea)|Выполняет вычисление области геометрии после преобразования указанной матрицы и плоской с использованием указанного допуска.|
|[CD2DGeometry:: Компутеленгс](#computelength)|Вычисляет длину геометрии так, как будто каждый сегмент был отменен в строке.|
|[CD2DGeometry:: Компутепоинтатленгс](#computepointatlength)|Вычисляет точку и вектор касательно на заданном расстоянии относительно геометрии после преобразования в указанной матрице и плоской с использованием указанного допуска.|
|[CD2DGeometry::D естрой](#destroy)|Уничтожает объект CD2DGeometry. (Переопределяет [CD2DResource::D естрой](../../mfc/reference/cd2dresource-class.md#destroy).)|
|[CD2DGeometry::D етач](#detach)|Отсоединяет интерфейс ресурса от объекта|
|[CD2DGeometry:: Филлконтаинспоинт](#fillcontainspoint)|Указывает, будет ли область, заполненная геометрией, содержать указанную точку с заданной дочерней отклонения.|
|[CD2DGeometry:: Get](#get)|Возвращает интерфейс ID2D1Geometry|
|[CD2DGeometry:: DataBound](#getbounds)||
|[CD2DGeometry:: Жетвиденедбаундс](#getwidenedbounds)|Возвращает границы геометрии после ее расширения с помощью указанной ширины и стиля штриха и преобразуется указанной матрицей.|
|[CD2DGeometry:: IsValid](#isvalid)|Проверяет допустимость ресурса (переопределяет [CD2DResource:: IsValid](../../mfc/reference/cd2dresource-class.md#isvalid).)|
|[CD2DGeometry:: структура](#outline)|Выполняет вычисление контура геометрии и записывает результат в ID2D1SimplifiedGeometrySink.|
|[CD2DGeometry:: Упростите](#simplify)|Создает упрощенную версию геометрии, которая содержит только строки и (необязательно) кубические кривые Безье и записывает результат в ID2D1SimplifiedGeometrySink.|
|[CD2DGeometry:: Строкеконтаинспоинт](#strokecontainspoint)|Определяет, содержит ли штрих геометрии указанную точку с заданной толщиной, стилем и преобразованием штрихов.|
|[CD2DGeometry:: тесселяция](#tessellate)|Создает набор повернутых по часовой стрелке треугольников, покрывающих геометрию после ее преобразования с использованием заданной матрицы и выпрямления с заданным допуском.|
|[CD2DGeometry:: Widening](#widen)|Расширяет геометрию по заданному штриху и записывает результат в ID2D1SimplifiedGeometrySink после его преобразования в указанную матрицу и плоскую с использованием указанного допуска.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DGeometry:: operator ID2D1Geometry *](#operator_id2d1geometry_star)|Возвращает интерфейс ID2D1Geometry|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DGeometry:: m_pGeometry](#m_pgeometry)|Указатель на ID2D1Geometry.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

`CD2DGeometry`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dgeometrycd2dgeometry"></a><a name="_dtorcd2dgeometry"></a> CD2DGeometry:: ~ CD2DGeometry

Деструктор Вызывается при уничтожении объекта геометрии D2D.

```
virtual ~CD2DGeometry();
```

## <a name="cd2dgeometryattach"></a><a name="attach"></a> CD2DGeometry:: Attach

Присоединяет существующий интерфейс ресурсов к объекту

```cpp
void Attach(ID2D1Geometry* pResource);
```

### <a name="parameters"></a>Параметры

*исходный код*<br/>
Существующий интерфейс ресурсов. Не может иметь значение NULL

## <a name="cd2dgeometrycd2dgeometry"></a><a name="cd2dgeometry"></a> CD2DGeometry::CD2DGeometry

Конструирует объект CD2DGeometry.

```
CD2DGeometry(
    CRenderTarget* pParentTarget,
    BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

## <a name="cd2dgeometrycombinewithgeometry"></a><a name="combinewithgeometry"></a> CD2DGeometry:: Комбиневисжеометри

Объединяет эту геометрию с указанной геометрией и сохраняет результат в ID2D1SimplifiedGeometrySink.

```
BOOL CombineWithGeometry(
    CD2DGeometry& inputGeometry,
    D2D1_COMBINE_MODE combineMode,
    const D2D1_MATRIX_3X2_F& inputGeometryTransform,
    ID2D1SimplifiedGeometrySink* geometrySink,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*инпутжеометри*<br/>
Геометрия, объединяемая с данным экземпляром.

*combineMode*<br/>
Тип выполняемой операции объединения.

*инпутжеометритрансформ*<br/>
Преобразование, применяемое к Инпутжеометри перед объединением.

*жеометрисинк*<br/>
Результат операции объединения.

*флаттенингтолеранце*<br/>
Максимальный диапазон для расстояния между точками кусочно-линейной аппроксимации данных геометрий. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dgeometrycomparewithgeometry"></a><a name="comparewithgeometry"></a> CD2DGeometry:: Компаревисжеометри

Описывает пересечение между этой геометрией и заданной геометрией. Сравнение выполняется с заданной допускной обпрозрачкой.

```
D2D1_GEOMETRY_RELATION CompareWithGeometry(
    CD2DGeometry& inputGeometry,
    const D2D1_MATRIX_3X2_F& inputGeometryTransform,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*инпутжеометри*<br/>
Геометрия для проверки.

*инпутжеометритрансформ*<br/>
Преобразование, применяемое к Инпутжеометри.

*флаттенингтолеранце*<br/>
Максимальный диапазон для расстояния между точками кусочно-линейной аппроксимации данных геометрий. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dgeometrycomputearea"></a><a name="computearea"></a> CD2DGeometry:: Компутеареа

Выполняет вычисление области геометрии после преобразования указанной матрицы и плоской с использованием указанного допуска.

```
BOOL ComputeArea(
    const D2D1_MATRIX_3X2_F& worldTransform,
    FLOAT& area,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*ворлдтрансформ*<br/>
Преобразование, применяемое к этой геометрии перед вычислением области.

*гистограмм*<br/>
После возврата из этого метода содержит указатель на область преобразованной плоской версии этой геометрии. Для этого параметра необходимо выделить хранилище.

*флаттенингтолеранце*<br/>
Максимальный диапазон для расстояния между точками кусочно-линейной аппроксимации геометрии. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dgeometrycomputelength"></a><a name="computelength"></a> CD2DGeometry:: Компутеленгс

Вычисляет длину геометрии так, как будто каждый сегмент был отменен в строке.

```
BOOL ComputeLength(
    const D2D1_MATRIX_3X2_F& worldTransform,
    FLOAT& length,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*ворлдтрансформ*<br/>
Преобразование, применяемое к геометрии перед вычислением ее длины.

*length*<br/>
При возврате из этого метода содержит указатель на длину геометрии. Для закрытых геометрических объектов длина включает неявный закрывающий сегмент. Для этого параметра необходимо выделить хранилище.

*флаттенингтолеранце*<br/>
Максимальный диапазон для расстояния между точками кусочно-линейной аппроксимации геометрии. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dgeometrycomputepointatlength"></a><a name="computepointatlength"></a> CD2DGeometry:: Компутепоинтатленгс

Вычисляет точку и вектор касательно на заданном расстоянии относительно геометрии после преобразования в указанной матрице и плоской с использованием указанного допуска.

```
BOOL ComputePointAtLength(
    FLOAT length,
    const D2D1_MATRIX_3X2_F& worldTransform,
    CD2DPointF& point,
    CD2DPointF& unitTangentVector,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*length*<br/>
Расстояние по геометрической части искомой точки и тангенса. Если это расстояние меньше 0, этот метод вычисляет первую точку в геометрии. Если это расстояние больше длины геометрии, этот метод вычисляет последнюю точку в геометрии.

*ворлдтрансформ*<br/>
Преобразование, применяемое к геометрии перед вычислением заданной точки и тангенса.

*точки*<br/>
Расположение с указанным расстоянием по геометрии. Если геометрия пуста, эта точка содержит NaN в качестве значений x и y.

*униттанжентвектор*<br/>
При возврате из этого метода содержит указатель на вектор касательной на указанном расстоянии по геометрии. Если геометрия пуста, этот вектор содержит NaN в качестве значений x и y. Для этого параметра необходимо выделить хранилище.

*флаттенингтолеранце*<br/>
Максимальный диапазон для расстояния между точками кусочно-линейной аппроксимации геометрии. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dgeometrydestroy"></a><a name="destroy"></a> CD2DGeometry::D естрой

Уничтожает объект CD2DGeometry.

```
virtual void Destroy();
```

## <a name="cd2dgeometrydetach"></a><a name="detach"></a> CD2DGeometry::D етач

Отсоединяет интерфейс ресурса от объекта

```
ID2D1Geometry* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный интерфейс ресурсов.

## <a name="cd2dgeometryfillcontainspoint"></a><a name="fillcontainspoint"></a> CD2DGeometry:: Филлконтаинспоинт

Указывает, будет ли область, заполненная геометрией, содержать указанную точку с заданной дочерней отклонения.

```
BOOL FillContainsPoint(
    CD2DPointF point,
    const D2D1_MATRIX_3X2_F& worldTransform,
    BOOL* contains,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*точки*<br/>
Точка для проверки.

*ворлдтрансформ*<br/>
Преобразование, применяемое к геометрии перед тестированием для включения.

*contains*<br/>
При возврате из этого метода содержит логическое значение, равное TRUE, если область, заполненная геометрическим объектом, содержит точку. в противном случае — значение FALSE. Для этого параметра необходимо выделить хранилище.

*флаттенингтолеранце*<br/>
Числовая точность, с которой вычисляется точный геометрический путь и пересечение пути. Точки, на которых отсутствует заливка, меньше, чем допуск, по-прежнему считаются внутри. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dgeometryget"></a><a name="get"></a> CD2DGeometry:: Get

Возвращает интерфейс ID2D1Geometry

```
ID2D1Geometry* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1Geometry или значение NULL, если объект еще не инициализирован.

## <a name="cd2dgeometrygetbounds"></a><a name="getbounds"></a> CD2DGeometry:: DataBound

```
BOOL GetBounds(
const D2D1_MATRIX_3X2_F& worldTransform,
CD2DRectF& bounds) const;
```

### <a name="parameters"></a>Параметры

*ворлдтрансформ*<br/>
*границы*

### <a name="return-value"></a>Возвращаемое значение

## <a name="cd2dgeometrygetwidenedbounds"></a><a name="getwidenedbounds"></a> CD2DGeometry:: Жетвиденедбаундс

Возвращает границы геометрии после ее расширения с помощью указанной ширины и стиля штриха и преобразуется указанной матрицей.

```
BOOL GetWidenedBounds(
    FLOAT strokeWidth,
    ID2D1StrokeStyle* strokeStyle,
    const D2D1_MATRIX_3X2_F& worldTransform,
    CD2DRectF& bounds,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*строкевидс*<br/>
Величина, на которую расширяется геометрия путем обводки ее контура.

*строкестиле*<br/>
Стиль штриха, который расширяет геометрию.

*ворлдтрансформ*<br/>
Преобразование, применяемое к геометрии после преобразования геометрии, и после того, как была выполнена обводка геометрии.

*границы*<br/>
При возврате из этого метода содержит границы расширяющего объекта Geometry. Для этого параметра необходимо выделить хранилище.

*флаттенингтолеранце*<br/>
Максимальный диапазон для расстояния между точками кусочно-линейной аппроксимации данных геометрий. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dgeometryisvalid"></a><a name="isvalid"></a> CD2DGeometry:: IsValid

Проверка действительности ресурсов

```
virtual BOOL IsValid() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если ресурс является допустимым; в противном случае — FALSE.

## <a name="cd2dgeometrym_pgeometry"></a><a name="m_pgeometry"></a> CD2DGeometry:: m_pGeometry

Указатель на ID2D1Geometry.

```
ID2D1Geometry* m_pGeometry;
```

## <a name="cd2dgeometryoperator-id2d1geometry"></a><a name="operator_id2d1geometry_star"></a> CD2DGeometry:: operator ID2D1Geometry *

Возвращает интерфейс ID2D1Geometry

```
operator ID2D1Geometry*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1Geometry или значение NULL, если объект еще не инициализирован.

## <a name="cd2dgeometryoutline"></a><a name="outline"></a> CD2DGeometry:: структура

Выполняет вычисление контура геометрии и записывает результат в ID2D1SimplifiedGeometrySink.

```
BOOL Outline(
    const D2D1_MATRIX_3X2_F& worldTransform,
    ID2D1SimplifiedGeometrySink* geometrySink,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*ворлдтрансформ*<br/>
Преобразование, применяемое к геометрической структуре.

*жеометрисинк*<br/>
ID2D1SimplifiedGeometrySink, к которому добавляется контур, преобразованный в геометрию.

*флаттенингтолеранце*<br/>
Максимальный диапазон для расстояния между точками кусочно-линейной аппроксимации геометрии. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dgeometrysimplify"></a><a name="simplify"></a> CD2DGeometry:: Упростите

Создает упрощенную версию геометрии, которая содержит только строки и (необязательно) кубические кривые Безье и записывает результат в ID2D1SimplifiedGeometrySink.

```
BOOL Simplify(
    D2D1_GEOMETRY_SIMPLIFICATION_OPTION simplificationOption,
    const D2D1_MATRIX_3X2_F& worldTransform,
    ID2D1SimplifiedGeometrySink* geometrySink,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*симплификатионоптион*<br/>
Значение типа, указывающее, должна ли упрощенная геометрия содержать кривые.

*ворлдтрансформ*<br/>
Преобразование, применяемое к упрощенной геометрии.

*жеометрисинк*<br/>
ID2D1SimplifiedGeometrySink, к которому добавляется упрощенная геометрия.

*флаттенингтолеранце*<br/>
Максимальный диапазон для расстояния между точками кусочно-линейной аппроксимации геометрии. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dgeometrystrokecontainspoint"></a><a name="strokecontainspoint"></a> CD2DGeometry:: Строкеконтаинспоинт

Определяет, содержит ли штрих геометрии указанную точку с заданной толщиной, стилем и преобразованием штрихов.

```
BOOL StrokeContainsPoint(
    CD2DPointF point,
    FLOAT strokeWidth,
    ID2D1StrokeStyle* strokeStyle,
    const D2D1_MATRIX_3X2_F& worldTransform,
    BOOL* contains,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*точки*<br/>
Точка для проверки на включение.

*строкевидс*<br/>
Толщина применяемого штриха.

*строкестиле*<br/>
Стиль применяемого начертания.

*ворлдтрансформ*<br/>
Преобразование, применяемое к штриховой геометрии.

*contains*<br/>
При возврате из этого метода содержит логическое значение TRUE, если штрих геометрии содержит указанную точку; в противном случае — значение FALSE. Для этого параметра необходимо выделить хранилище.

*флаттенингтолеранце*<br/>
Числовая точность, с которой вычисляется точный геометрический путь и пересечение пути. Точки, на которых пропущен штрих, меньше, чем допуск, по-прежнему считаются внутри. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dgeometrytessellate"></a><a name="tessellate"></a> CD2DGeometry:: тесселяция

Создает набор повернутых по часовой стрелке треугольников, покрывающих геометрию после ее преобразования с использованием заданной матрицы и выпрямления с заданным допуском.

```
BOOL Tessellate(
    const D2D1_MATRIX_3X2_F& worldTransform,
    ID2D1TessellationSink* tessellationSink,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*ворлдтрансформ*<br/>
Преобразование, применяемое к этой геометрии, или значение NULL.

*тесселлатионсинк*<br/>
ID2D1TessellationSink, к которому добавляется тесселяция.

*флаттенингтолеранце*<br/>
Максимальный диапазон для расстояния между точками кусочно-линейной аппроксимации геометрии. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dgeometrywiden"></a><a name="widen"></a> CD2DGeometry:: Widening

Расширяет геометрию по заданному штриху и записывает результат в ID2D1SimplifiedGeometrySink после его преобразования в указанную матрицу и плоскую с использованием указанного допуска.

```
BOOL Widen(
    FLOAT strokeWidth,
    ID2D1StrokeStyle* strokeStyle,
    const D2D1_MATRIX_3X2_F& worldTransform,
    ID2D1SimplifiedGeometrySink* geometrySink,
    FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE) const;
```

### <a name="parameters"></a>Параметры

*строкевидс*<br/>
Величина, на которую расширяется геометрия.

*строкестиле*<br/>
Стиль начертания, применяемого к геометрии, или значение NULL.

*ворлдтрансформ*<br/>
Преобразование, применяемое к геометрии после расширения.

*жеометрисинк*<br/>
ID2D1SimplifiedGeometrySink, к которому добавляется Расширенная геометрия.

*флаттенингтолеранце*<br/>
Максимальный диапазон для расстояния между точками кусочно-линейной аппроксимации геометрии. Чем меньше значения, тем точнее результаты и медленнее производится выполнение.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
