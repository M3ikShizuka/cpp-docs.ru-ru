---
description: Дополнительные сведения о классе Array
title: Класс array
ms.date: 11/04/2016
f1_keywords:
- array
- AMP/array
- AMP/Concurrency::array::array
- AMP/Concurrency::array::copy_to
- AMP/Concurrency::array::data
- AMP/Concurrency::array::get_accelerator_view
- AMP/Concurrency::array::get_associated_accelerator_view
- AMP/Concurrency::array::get_cpu_access_type
- AMP/Concurrency::array::get_extent
- AMP/Concurrency::array::reinterpret_as
- AMP/Concurrency::array::section
- AMP/Concurrency::array::view_as
- AMP/Concurrency::array::rank
- AMP/Concurrency::array::accelerator_view
- AMP/Concurrency::array::associated_accelerator_view
- AMP/Concurrency::array::cpu_access_type
- AMP/Concurrency::array::extent
helpviewer_keywords:
- array class
ms.assetid: 0832b6c1-40f0-421d-9104-6b1baa0c63a7
ms.openlocfilehash: df74ab714fc2865cce71300e094b693664694b31
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97247895"
---
# <a name="array-class"></a>Класс array

Представляет контейнер данных, используемый для перемещения данных в ускоритель.

## <a name="syntax"></a>Синтаксис

```cpp
template <typename value_type, int _Rank>
friend class array;
```

### <a name="parameters"></a>Параметры

*value_type*<br/>
Тип элемента данных.

*_Rank*<br/>
Ранг массива.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Конструктор массива](#ctor)|Инициализирует новый экземпляр класса `array`.|
|[Деструктор массива ~](#dtor)|Уничтожает `array` объект.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[copy_to](#copy_to)|Копирует содержимое массива в другой массив.|
|[data](#data)|Возвращает указатель на необработанные данные массива.|
|[get_accelerator_view](#get_accelerator_view)|Возвращает объект [accelerator_view](accelerator-view-class.md) , представляющий расположение, в котором выделяется массив. Доступ к этому свойству можно получить только в ЦП.|
|[get_associated_accelerator_view](#get_associated_accelerator_view)|Возвращает второй [accelerator_view](accelerator-view-class.md) объект, передаваемый в качестве параметра при вызове промежуточного конструктора для создания экземпляра `array` объекта.|
|[get_cpu_access_type](#get_cpu_access_type)|Возвращает [access_type](concurrency-namespace-enums-amp.md#access_type) массива. Доступ к этому методу можно получить только в ЦП.|
|[get_extent](#get_extent)|Возвращает объект [экстента](extent-class.md) массива.|
|[reinterpret_as](#reinterpret_as)|Возвращает одномерный массив, содержащий все элементы в `array` объекте.|
|[раздела](#section)|Возвращает подраздел `array` объекта, который находится в указанном источнике и, при необходимости, с указанным экстентом.|
|[view_as](#view_as)|Возвращает объект [array_view](array-view-class.md) , созданный из `array` объекта.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Оператор std:: vector &lt; value_type&gt;](#operator_vec)|Использует `copy(*this, vector)` для неявного преобразования массива в объект std::[vector](../../../standard-library/vector-class.md) .|
|[оператор ()](#operator_call)|Возвращает значение элемента, заданное параметрами.|
|[станции\[\]](#operator_at)|Возвращает элемент, расположенный по указанному индексу.|
|[Оператор =](#operator_eq)|Копирует содержимое указанного `array` объекта в этот объект.|

### <a name="public-constants"></a>Открытые константы

|Имя|Описание|
|----------|-----------------|
|[Константа Rank](#rank)|Хранит ранг массива.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[accelerator_view](#accelerator_view)|Возвращает объект [accelerator_view](accelerator-view-class.md) , представляющий расположение, в котором выделяется массив. Доступ к этому свойству можно получить только в ЦП.|
|[associated_accelerator_view](#associated_accelerator_view)|Возвращает второй [accelerator_view](accelerator-view-class.md) объект, передаваемый в качестве параметра при вызове промежуточного конструктора для создания экземпляра `array` объекта.|
|[cpu_access_type](#cpu_access_type)|Возвращает [access_type](concurrency-namespace-enums-amp.md#access_type) , который представляет, как ЦП может получить доступ к хранилищу массива.|
|[экстент](#extent)|Возвращает экстент, определяющий форму массива.|

## <a name="remarks"></a>Комментарии

Тип `array<T,N>` представляет собой сжатый и обычный (неровный) *N*-мерный массив, расположенный в определенном месте, например в ускорителе или ЦП. Тип данных элементов массива — `T` , который должен иметь тип, совместимый с целевым ускорителем. Хотя ранг, `N` (массива определяется статически и является частью типа, экстент массива определяется средой выполнения и выражается с помощью класса `extent<N>` .

Массив может иметь любое количество измерений, хотя некоторые функциональные возможности являются специализированными для `array` объектов с рангом 1, 2 и 3. Если опустить аргумент измерения, значение по умолчанию — 1.

Данные массива располагаются последовательно в памяти. Элементы, которые отличаются друг от друга в наименее значимом измерении, являются смежными в памяти.

Массивы логически считаются типами значений, поскольку при копировании массива в другой массив выполняется глубокое копирование. Два массива никогда не указывают на одни и те же данные.

`array<T,N>`Тип используется в нескольких сценариях.

- В качестве контейнера данных, который можно использовать в вычислениях в ускорителе.

- В качестве контейнера данных для хранения памяти на ЦП узла (который может использоваться для копирования в другие массивы и обратно).

- В качестве промежуточного объекта, который будет служить быстрым посредником в копиях типа "узел-устройство".

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`array`

## <a name="requirements"></a>Требования

**Заголовок** : amp.h

**Пространство имен** : Concurrency

## <a name="array"></a><a name="dtor"></a> ~ массив

Уничтожает `array` объект.

```cpp
~array() restrict(cpu);
```

## <a name="accelerator_view"></a><a name="accelerator_view"></a> accelerator_view

Возвращает объект [accelerator_view](accelerator-view-class.md) , представляющий расположение, в котором выделяется массив. Доступ к этому свойству можно получить только в ЦП.

```cpp
__declspec(property(get= get_accelerator_view)) Concurrency::accelerator_view accelerator_view;
```

## <a name="array"></a>Массив <a name="ctor"></a>

Инициализирует новый экземпляр [класса Array](array-class.md). Отсутствует конструктор по умолчанию для `array<T,N>` . Все конструкторы выполняются только на ЦП. Они не могут выполняться на целевом объекте Direct3D.

```cpp
explicit array(
    const Concurrency::extent<_Rank>& _Extent) restrict(cpu);

explicit array(
    int _E0) restrict(cpu);

explicit array(
    int _E0,
    int _E1) restrict(cpu);

explicit array(
    int _E0,
    int _E1,
    int _E2) restrict(cpu);

array(
    const Concurrency::extent<_Rank>& _Extent,
    Concurrency::accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

array(
    int _E0,
    Concurrency::accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

array(
    int _E0,
    int _E1,
    Concurrency::accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

array(
    int _E0,
    int _E1,
    int _E2,
    Concurrency::accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

array(
    const Concurrency::extent<_Rank>& _Extent,
    Concurrency::accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

array(
    int _E0,
    accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

array(
    int _E0,
    int _E1,
    Concurrency::accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

array(
    int _E0,
    int _E1,
    int _E2,
    Concurrency::accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

template <typename _InputIterator>
array(
    const Concurrency::extent<_Rank>& _Extent,
    _InputIterator _Src_first,
    _InputIterator _Src_last) restrict(cpu);

template <typename _InputIterator>
array(
    const Concurrency::extent<_Rank>& _Extent,
    _InputIterator _Src_first) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    _InputIterator _Src_first,
    _InputIterator _Src_last) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    _InputIterator _Src_first) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1,
    _InputIterator _Src_first,
    _InputIterator _Src_last) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1,
    _InputIterator _Src_first) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1,
    int _E2,
    _InputIterator _Src_first,
    _InputIterator _Src_last) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1,
    int _E2,
    _InputIterator _Src_first) restrict(cpu);

template <typename _InputIterator>
array(
    const Concurrency::extent<_Rank>& _Extent,
    _InputIterator _Src_first,
    _InputIterator _Src_last,
    Concurrency::accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

template <typename _InputIterator>
array(
    const Concurrency::extent<_Rank>& _Extent,
    _InputIterator _Src_first,
    Concurrency::accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    _InputIterator _Src_first,
    _InputIterator _Src_last,
    Concurrency::accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    _InputIterator _Src_first,
    Concurrency::accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1,
    _InputIterator _Src_first,
    _InputIterator _Src_last,
    Concurrency::accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1,
    _InputIterator _Src_first,
    Concurrency::accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1,
    int _E2,
    _InputIterator _Src_first,
    _InputIterator _Src_last,
    Concurrency::accelerator_view _Av,
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1,
    int _E2,
    _InputIterator _Src_first,
    Concurrency::accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

template <typename _InputIterator>
array(
    const Concurrency::extent<_Rank>& _Extent,
    _InputIterator _Src_first,
    _InputIterator _Src_last,
    Concurrency::accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

template <typename _InputIterator>
array(
    const Concurrency::extent<_Rank>& _Extent,
    _InputIterator _Src_first,
    Concurrency::accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    _InputIterator _Src_first,
    _InputIterator _Src_last,
    Concurrency::accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0, _InputIterator _Src_first,
    Concurrency::accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1, _InputIterator _Src_first, _InputIterator _Src_last,
    Concurrency::accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1, _InputIterator _Src_first,
    Concurrency::accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1,
    int _E2, _InputIterator _Src_first, _InputIterator _Src_last,
    Concurrency::accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

template <typename _InputIterator>
array(
    int _E0,
    int _E1,
    int _E2, _InputIterator _Src_first,
    Concurrency::accelerator_view _Av,
    Concurrency::accelerator_view _Associated_Av) restrict(cpu);

explicit array(
    const array_view<const value_type, _Rank>& _Src) restrict(cpu);

array(
    const array_view<const value_type, _Rank>& _Src,
    accelerator_view _Av
    access_type _Cpu_access_type = access_type_auto) restrict(cpu);

array(
    const array_view<const value_type, _Rank>& _Src,
    accelerator_view _Av,
    accelerator_view _Associated_Av) restrict(cpu);

array(const array& _Other) restrict(cpu);

array(array&& _Other) restrict(cpu);
```

### <a name="parameters"></a>Параметры

*_Associated_Av*<br/>
Accelerator_view, указывающий предпочтительное целевое расположение массива.

*_Av*<br/>
Объект [accelerator_view](accelerator-view-class.md) , указывающий расположение массива.

*_Cpu_access_type*<br/>
Требуемый [access_type](concurrency-namespace-enums-amp.md#access_type)  для массива ЦП. Этот параметр имеет значение по умолчанию, что `access_type_auto` `access_type` позволяет не выполнять определение ЦП в среде выполнения. Фактический ЦП `access_type` для массива можно запросить с помощью `get_cpu_access_type` метода.

*_Extent*<br/>
Экстент в каждом измерении массива.

*_E0*<br/>
Наиболее важный компонент экстента этого раздела.

*_E1*<br/>
Наиболее важный компонент в области этого раздела.

*_E2*<br/>
Наименее важный компонент экстента этого раздела.

*_InputIterator*<br/>
Тип итератора ввода.

*_Src*<br/>
В объект для копирования.

*_Src_first*<br/>
Начальный итератор в исходный контейнер.

*_Src_last*<br/>
Конечный итератор в исходный контейнер.

*_Other*<br/>
Другой источник данных.

*_Rank*<br/>
Ранг раздела.

*value_type*<br/>
Тип данных копируемых элементов.

## <a name="associated_accelerator_view"></a><a name="associated_accelerator_view"></a> associated_accelerator_view

Возвращает второй [accelerator_view](accelerator-view-class.md) объект, передаваемый в качестве параметра при вызове промежуточного конструктора для создания экземпляра `array` объекта.

```cpp
__declspec(property(get= get_associated_accelerator_view)) Concurrency::accelerator_view associated_accelerator_view;
```

## <a name="copy_to"></a><a name="copy_to"></a> copy_to

Копирует содержимое объекта `array` в другое `array` .

```cpp
void copy_to(
    array<value_type, _Rank>& _Dest) const ;

void copy_to(
    array_view<value_type, _Rank>& _Dest) const ;
```

### <a name="parameters"></a>Параметры

*_Dest*<br/>
Объект [array_view](array-view-class.md) , в который производится копирование.

## <a name="cpu_access_type"></a><a name="cpu_access_type"></a> cpu_access_type

Возвращает access_type ЦП, разрешенный для этого массива.

```cpp
__declspec(property(get= get_cpu_access_type)) access_type cpu_access_type;
```

## <a name="data"></a>Данные <a name="data"></a>.

Возвращает указатель на необработанные данные `array` .

```cpp
value_type* data() restrict(amp, cpu);

const value_type* data() const restrict(amp, cpu);
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на необработанные данные массива.

## <a name="extent"></a><a name="extent"></a> экстент

Возвращает объект [экстента](extent-class.md) , определяющий форму объекта `array` .

```cpp
__declspec(property(get= get_extent)) Concurrency::extent<_Rank> extent;
```

## <a name="get_accelerator_view"></a><a name="get_accelerator_view"></a> get_accelerator_view

Возвращает объект [accelerator_view](accelerator-view-class.md) , представляющий расположение, в которое `array` выделяется объект. Доступ к этому свойству можно получить только в ЦП.

```cpp
Concurrency::accelerator_view get_accelerator_view() const;
```

### <a name="return-value"></a>Возвращаемое значение

`accelerator_view`Объект, представляющий расположение, в которое `array` выделяется объект.

## <a name="get_associated_accelerator_view"></a><a name="get_associated_accelerator_view"></a> get_associated_accelerator_view

Возвращает второй [accelerator_view](accelerator-view-class.md) объект, передаваемый в качестве параметра при вызове промежуточного конструктора для создания экземпляра `array` объекта.

```cpp
Concurrency::accelerator_view get_associated_accelerator_view() const ;
```

### <a name="return-value"></a>Возвращаемое значение

Второй [accelerator_view](accelerator-view-class.md) объект, переданный в промежуточный конструктор.

## <a name="get_cpu_access_type"></a><a name="get_cpu_access_type"></a> get_cpu_access_type

Возвращает access_type ЦП, допустимый для этого массива.

```cpp
access_type get_cpu_access_type() const restrict(cpu);
```

### <a name="return-value"></a>Возвращаемое значение

## <a name="get_extent"></a><a name="get_extent"></a> get_extent

Возвращает объект [экстента](extent-class.md) `array` .

```cpp
Concurrency::extent<_Rank> get_extent() const restrict(amp,cpu);
```

### <a name="return-value"></a>Возвращаемое значение

Метаданные `extent` для объекта `array`.

## <a name="operator-stdvectorltvalue_typegt"></a><a name="operator_vec"></a> Оператор std:: vector &lt; value_type&gt;

Использует `copy(*this, vector)` для неявного преобразования массива в объект std:: Vector.

```cpp
operator std::vector<value_type>() const restrict(cpu);
```

### <a name="parameters"></a>Параметры

*value_type*<br/>
Тип данных элементов вектора.

### <a name="return-value"></a>Возвращаемое значение

Объект типа `vector<T>` , содержащий копию данных, содержащихся в массиве.

## <a name="operator"></a><a name="operator_call"></a> оператор ()

Возвращает значение элемента, заданное параметрами.

```cpp
value_type& operator() (const index<_Rank>& _Index) restrict(amp,cpu);

const value_type& operator() (const index<_Rank>& _Index) cons  t restrict(amp,cpu);

value_type& operator() (int _I0, int _I1) restrict(amp,cpu);

const value_type& operator() (int _I0, int _I1) const restrict(amp,cpu)  ;

value_type& operator() (int _I0, int _I1, int _I2) restrict(amp,cpu);

const value_type& operator() (int _I0, int _I1, int _I2) const restrict(amp,cpu);

typename details::_Projection_result_type<value_type,_Rank>::_Result_type operator()(int _I) restrict(amp,cpu);

typename details::_Projection_result_type<value_type,_Rank>::_Const_result_type operator()(int _I) const restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_Index*<br/>
Расположение элемента.

*_I0*<br/>
Наиболее важный компонент происхождения этого раздела.

*_I1*<br/>
Последующий важный компонент в происхождении этого раздела.

*_I2*<br/>
Наименее важный компонент происхождения этого раздела.

*_I*<br/>
Расположение элемента.

### <a name="return-value"></a>Возвращаемое значение

Значение элемента, заданное параметрами.

## <a name="operator"></a><a name="operator_at"></a> operator[]

Возвращает элемент, расположенный по указанному индексу.

```cpp
value_type& operator[](const index<_Rank>& _Index) restrict(amp,cpu);

const value_type& operator[]
    (const index<_Rank>& _Index) const restrict(amp,cpu);

typename details::_Projection_result_type<value_type,_Rank>::_Result_type operator[](int _i) restrict(amp,cpu);

typename details::_Projection_result_type<value_type,_Rank>::_Const_result_type operator[](int _i) const restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_Index*<br/>
Индекс.

*_I*<br/>
Индекс.

### <a name="return-value"></a>Возвращаемое значение

Элемент, расположенный по указанному индексу.

## <a name="operator"></a><a name="operator_eq"></a> Оператор =

Копирует содержимое указанного `array` объекта.

```cpp
array& operator= (const array& _Other) restrict(cpu);

array& operator= (array&& _Other) restrict(cpu);

array& operator= (
    const array_view<const value_type, _Rank>& _Src) restrict(cpu);
```

### <a name="parameters"></a>Параметры

*_Other*<br/>
Объект, из которого производится `array` копирование.

*_Src*<br/>
Объект, из которого производится `array` копирование.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на этот `array` объект.

## <a name="rank"></a><a name="rank"></a> Рейтинг

Хранит ранг `array` .

```cpp
static const int rank = _Rank;
```

## <a name="reinterpret_as"></a><a name="reinterpret_as"></a> reinterpret_as

Повторно интерпретирует массив с помощью одномерного array_view, который при необходимости может иметь тип значения, отличный от типа исходного массива.

### <a name="syntax"></a>Синтаксис

```cpp
template <typename _Value_type2>
array_view<_Value_type2,1> reinterpret_as() restrict(amp,cpu);

template <typename _Value_type2>
array_view<const _Value_type2, 1> reinterpret_as() const restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_Value_type2*<br/>
Тип данных возвращаемых данных.

### <a name="return-value"></a>Возвращаемое значение

Array_view или const array_view объект, основанный на массиве, с типом элемента, который снова интерпретируется от T до ElementType, а ранг уменьшился с N до 1.

### <a name="remarks"></a>Комментарии

Иногда удобно просматривать многомерный массив, как если бы он был линейным одномерным массивом, возможно, с типом значения, отличным от типа исходного массива. Этот метод можно использовать для достижения этого результата.
**Внимание!** Переинтерпретирование объекта массива с помощью другого типа значения является потенциально небезопасной операцией. Рекомендуется внимательно использовать эту функцию.

Пример кода:

```cpp
struct RGB { float r; float g; float b; };

array<RGB,3>  a = ...;
array_view<float,1> v = a.reinterpret_as<float>();

assert(v.extent == 3*a.extent);
```

## <a name="section"></a>Раздел <a name="section"></a>

Возвращает подраздел `array` объекта, который находится в указанном источнике и, при необходимости, с указанным экстентом.

```cpp
array_view<value_type,_Rank> section(
    const Concurrency::index<_Rank>& _Section_origin,
    const Concurrency::extent<_Rank>& _Section_extent) restrict(amp,cpu);

array_view<const value_type,_Rank> section(
    const Concurrency::index<_Rank>& _Section_origin,
    const Concurrency::extent<_Rank>& _Section_extent) const restrict(amp,cpu);

array_view<value_type,_Rank> section(
    const Concurrency::extent<_Rank>& _Ext) restrict(amp,cpu);

array_view<const value_type,_Rank> section(
    const Concurrency::extent<_Rank>& _Ext) const restrict(amp,cpu);

array_view<value_type,_Rank> section(
    const index<_Rank>& _Idx) restrict(amp,cpu);

array_view<const value_type,_Rank> section(
    const index<_Rank>& _Idx) const restrict(amp,cpu);

array_view<value_type,1> section(
    int _I0,
    int _E0) restrict(amp,cpu);

array_view<const value_type,1> section(
    int _I0,
    int _E0) const restrict(amp,cpu);

array_view<value_type,2> section(
    int _I0,
    int _I1,
    int _E0,
    int _E1) restrict(amp,cpu);

array_view<const value_type,2> section(
    int _I0,
    int _I1,
    int _E0,
    int _E1) const restrict(amp,cpu);

array_view<value_type,3> section(
    int _I0,
    int _I1,
    int _I2,
    int _E0,
    int _E1,
    int _E2) restrict(amp,cpu);

array_view<const value_type,3> section(
    int _I0,
    int _I1,
    int _I2,
    int _E0,
    int _E1,
    int _E2) const restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_E0*<br/>
Наиболее важный компонент экстента этого раздела.

*_E1*<br/>
Наиболее важный компонент в области этого раздела.

*_E2*<br/>
Наименее важный компонент экстента этого раздела.

*_Ext*<br/>
Объект [экстента](extent-class.md) , указывающий экстент раздела. Источник равен 0.

*_Idx*<br/>
Объект [index](index-class.md) , указывающий расположение источника. Подразделы — это оставшаяся часть экстента.

*_I0*<br/>
Наиболее важный компонент происхождения этого раздела.

*_I1*<br/>
Последующий важный компонент в происхождении этого раздела.

*_I2*<br/>
Наименее важный компонент происхождения этого раздела.

*_Rank*<br/>
Ранг раздела.

*_Section_extent*<br/>
Объект [экстента](extent-class.md) , указывающий экстент раздела.

*_Section_origin*<br/>
Объект [index](index-class.md) , указывающий расположение источника.

*value_type*<br/>
Тип данных копируемых элементов.

### <a name="return-value"></a>Возвращаемое значение

Возвращает подраздел `array` объекта, который находится в указанном источнике и, при необходимости, с указанным экстентом. Если указан только `index` объект, подраздел содержит все элементы в связанной сетке, имеющие индексы, превышающие индексы элементов в `index` объекте.

## <a name="view_as"></a><a name="view_as"></a> view_as

Переинтерпретирует этот массив как [array_view](array-view-class.md) другого ранга.

```cpp
template <int _New_rank>
array_view<value_type,_New_rank> view_as(
    const Concurrency::extent<_New_rank>& _View_extent) restrict(amp,cpu);

template <int _New_rank>
array_view<const value_type,_New_rank> view_as(
    const Concurrency::extent<_New_rank>& _View_extent) const restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_New_rank*<br/>
Ранг `extent` объекта, переданного в качестве параметра.

*_View_extent*<br/>
Экстент, используемый для создания нового объекта [array_view](array-view-class.md) .

*value_type*<br/>
Тип данных элементов в исходном `array` объекте и возвращенном `array_view` объекте.

### <a name="return-value"></a>Возвращаемое значение

Созданный объект [array_view](array-view-class.md) .

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency (C++ AMP)](concurrency-namespace-cpp-amp.md)
