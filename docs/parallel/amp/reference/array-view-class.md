---
description: 'Дополнительные сведения о: array_view классе'
title: Класс array_view
ms.date: 11/04/2016
f1_keywords:
- array_view
- AMP/array_view
- AMP/Concurrency::array_view::array_view
- AMP/Concurrency::array_view::copy_to
- AMP/Concurrency::array_view::data
- AMP/Concurrency::array_view::discard_data
- AMP/Concurrency::array_view::get_extent
- AMP/Concurrency::array_view::get_ref
- AMP/Concurrency::array_view::get_source_accelerator_view
- AMP/Concurrency::array_view::refresh
- AMP/Concurrency::array_view::reinterpret_as
- AMP/Concurrency::array_view::section
- AMP/Concurrency::array_view::synchronize
- AMP/Concurrency::array_view::synchronize_async
- AMP/Concurrency::array_view::synchronize_to
- AMP/Concurrency::array_view::synchronize_to_async
- AMP/Concurrency::array_view::view_as
- AMP/Concurrency::array_view::rank
- AMP/Concurrency::array_view::extent
- AMP/Concurrency::array_view::source_accelerator_view
- AMP/Concurrency::array_view::value_type
helpviewer_keywords:
- array_view class
ms.assetid: 7e7ec9bc-05a2-4372-b05d-752b50006c5a
ms.openlocfilehash: 170eb51a437fd56b9b9e74bb22e5b84d3478b4bd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97247882"
---
# <a name="array_view-class"></a>Класс array_view

Представляет N-мерный вид данных, хранящихся в другом контейнере.

## <a name="syntax"></a>Синтаксис

```cpp
template <
    typename value_type,
    int _Rank = 1
>
class array_view : public _Array_view_base<_Rank, sizeof(value_type)/sizeof(int)>;

template <
    typename value_type,
    int _Rank
>
class array_view<const value_type, _Rank> : public _Array_view_base<_Rank, sizeof(value_type)/sizeof(int)>;
```

### <a name="parameters"></a>Параметры

*value_type*<br/>
Тип данных элементов в `array_view` объекте.

*_Rank*<br/>
Ранг `array_view` объекта.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Конструктор array_view](#ctor)|Инициализирует новый экземпляр класса `array_view`. Отсутствует конструктор по умолчанию для `array<T,N>` . Все конструкторы могут выполняться только на ЦП и не могут выполняться на целевом объекте Direct3D.|
|[Деструктор ~ array_view](#ctor)|Уничтожает `array_view` объект.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[copy_to](#copy_to)|Копирует содержимое `array_view` объекта в указанное место назначения путем вызова `copy(*this, dest)` .|
|[data](#data)|Возвращает указатель на необработанные данные `array_view` .|
|[discard_data](#discard_data)|Отменяет текущие данные, лежащие в этом представлении.|
|[get_extent](#get_extent)|Возвращает объект экстента объекта array_view.|
|[get_ref](#get_ref)|Возвращает ссылку на индексированный элемент.|
|[get_source_accelerator_view](#get_source_accelerator_view)|Возвращает [accelerator_view](accelerator-view-class.md) , где расположен источник данных `array_view` .|
|[обновляется](#refresh)|Уведомляет `array_view` объект о том, что связанная с ним память была изменена за пределами `array_view` интерфейса. Вызов этого метода выводит все кэшированные данные в устаревшем виде.|
|[reinterpret_as](#reinterpret_as)|Возвращает одномерный массив, содержащий все элементы в `array_view` объекте.|
|[раздела](#section)|Возвращает подраздел `array_view` объекта, который находится в указанном источнике и, при необходимости, с указанным экстентом.|
|[полнит](#synchronize)|Синхронизирует все изменения, внесенные в `array_view` объект, с исходными данными.|
|[synchronize_async](#synchronize_async)|Асинхронно синхронизирует все изменения, внесенные в `array_view` объект, с исходными данными.|
|[synchronize_to](#synchronize_to)|Синхронизирует все изменения, внесенные в `array_view` объект, с указанным [accelerator_view](accelerator-view-class.md).|
|[synchronize_to_async](#synchronize_to_async)|Асинхронно синхронизирует все изменения, внесенные в `array_view` объект, с указанным [accelerator_view](accelerator-view-class.md).|
|[view_as](#view_as)|Создает `array_view` объект с другим рангом, используя `array_view` данные этого объекта.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[оператор ()](#operator_call)|Возвращает значение элемента, заданного параметром или параметрами.|
|[станции\[\]](#operator_at)|Возвращает элемент, заданный параметрами.|
|[Оператор =](#operator_eq)|Копирует содержимое указанного `array_view` объекта в этот объект.|

### <a name="public-constants"></a>Открытые константы

|Имя|Описание|
|----------|-----------------|
|[Константа Rank](#rank)|Хранит ранг `array_view` объекта.|

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|[экстент](#extent)|Получает объект `extent`, который определяет форму объекта `array_view`.|
|[source_accelerator_view](#source_accelerator_view)|Возвращает [accelerator_view](accelerator-view-class.md) , где расположен источник данных `array_view`|
|[value_type](#value_type)|Тип значения объекта `array_view` и привязанного массива.|

## <a name="remarks"></a>Комментарии

`array_view`Класс представляет представление данных, содержащихся в объекте [массива](array-class.md) или в подразделе `array` объекта.

Можно получить доступ к `array_view` объекту, где находятся исходные данные (локально) или в другом ускорителе или домене согласования (удаленно). При удаленном доступе к объекту представления копируются и кэшируются по мере необходимости. За исключением последствий автоматического кэширования, `array_view` объекты имеют профиль производительности, аналогичный тому, что и `array` объекты. При доступе к данным через представления возникают небольшие потери производительности.

Существует три сценария удаленного использования.

- Представление указателя системной памяти передается с помощью [parallel_for_each](../../../parallel/concrt/reference/concurrency-namespace-functions.md#parallel_for_each) вызова ускорителя и доступа к нему по сочетанию клавиш.

- Представление массива, расположенного в ускорителе, передается с помощью `parallel_for_each` вызова другого ускорителя и к нему осуществляется доступ.

- Доступ к массиву, расположенному на ускорителе, осуществляется через ЦП.

В любом из этих сценариев представления, на которые имеются ссылки, копируются средой выполнения в удаленное расположение и, если они были изменены вызовами `array_view` объекта, копируются обратно в локальное расположение. Среда выполнения может оптимизировать процесс копирования изменений назад, может копировать только измененные элементы или копировать неизмененные фрагменты. Перекрывающиеся `array_view` объекты в одном источнике данных не гарантируют поддержание ссылочной целостности в удаленном расположении.

Необходимо синхронизировать любой многопоточный доступ к одному и тому же источнику данных.

Среда выполнения предоставляет следующие гарантии относительно кэширования данных в `array_view` объектах:

- Все хорошо синхронизированные доступ к `array` объекту и `array_view` объекту в нем в порядке программ подчиняется последовательной связи «выполняется до».

- Все хорошо синхронизированные обращения к перекрывающимся `array_view` объектам одного и того же ускорителя на одном `array` объекте имеют псевдонимы через `array` объект. Они применяют общее число происходящих перед связью, которая подчиняется порядкам программ. Кэширование отсутствует. Если `array_view` объекты выполняются на разных ускорителях, порядок доступа не определен, создается состояние гонки.

При создании `array_view` объекта с помощью указателя в системной памяти необходимо изменить `array_view` объект представления только с помощью `array_view` указателя. Кроме того, необходимо вызвать `refresh()` для одного из `array_view` объектов, присоединенных к системному указателю, если базовая память, управляемая в машинном формате, изменяется напрямую, а не через `array_view` объект.

Какое-либо действие уведомляет объект о том `array_view` , что базовая память базовой памяти изменилась и все копии, расположенные в ускорителе, устарели. Если следовать этим рекомендациям, представления на основе указателя идентичны тем, которые предоставляются представлениям параллельных массивов данных.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`_Array_view_shape`

`_Array_view_base`

`array_view`

## <a name="requirements"></a>Требования

**Заголовок** : amp.h

**Пространство имен** : Concurrency

## <a name="array_view"></a><a name="dtor"></a> ~ array_view

Уничтожает `array_view` объект.

```cpp
~array_view()restrict(amp,cpu);
```

## <a name="array_view"></a><a name="ctor"></a> array_view

Инициализирует новый экземпляр класса `array_view`.

```cpp
array_view(
    array<value_type, _Rank>& _Src)restrict(amp,cpu);

array_view(
    const array_view& _Other)restrict(amp,cpu);

explicit array_view(
    const Concurrency::extent<_Rank>& _Extent) restrict(cpu);

template <
    typename _Container
>
array_view(
    const Concurrency::extent<_Rank>& _Extent,
    _Container& _Src) restrict(cpu);

array_view(
    const Concurrency::extent<_Rank>& _Extent,
    value_type* _Src)restrict(amp,cpu);

explicit array_view(
    int _E0) restrict(cpu);

template <
    typename _Container
>
explicit array_view(
    _Container& _Src,
    typename std::enable_if<details::_Is_container<_Container>::type::value, void **>::type = 0) restrict(cpu);

template <
    typename _Container
>
explicit array_view(
    int _E0,
    _Container& _Src) restrict(cpu);

explicit array_view(
    int _E0,
    int _E1) __CPU_ONLY;

template <
    typename _Container
>
explicit array_view(
    int _E0,
    int _E1,
    _Container& _Src) restrict(cpu);

explicit array_view(
    int _E0,
    int _E1,
    int _E2) __CPU_ONLY;

template <
    typename _Container
>
explicit array_view(
    int _E0,
    int _E1,
    int _E2,
    _Container& _Src);

explicit array_view(
    int _E0,
    _In_ value_type* _Src)restrict(amp,cpu);

template <
    typename _Arr_type,
    int _Size
>
explicit array_view(
    _In_ _Arr_type (& _Src) [_Size]) restrict(amp,cpu);

explicit array_view(
    int _E0,
    int _E1,
    _In_ value_type* _Src)restrict(amp,cpu);

explicit array_view(
    int _E0,
    int _E1,
    int _E2,
    _In_ value_type* _Src)restrict(amp,cpu);

array_view(
    const array<value_type, _Rank>& _Src)restrict(amp,cpu);

array_view(
    const array_view<value_type, _Rank>& _Src)restrict(amp,cpu);

array_view(
    const array_view<const value_type, _Rank>& _Src)restrict(amp,cpu);

template <
    typename _Container
>
array_view(
    const Concurrency::extent<_Rank>& _Extent,
    const _Container& _Src) restrict(cpu);

template <
    typename _Container
>
explicit array_view(
    const _Container& _Src,
    typename std::enable_if<details::_Is_container<_Container>::type::value, void **>::type = 0) restrict(cpu);

array_view(
    const Concurrency::extent<_Rank>& _Extent,
    const value_type* _Src)restrict(amp,cpu);

template <
    typename _Arr_type,
    int _Size
>
explicit array_view(
    const _In_ _Arr_type (& _Src) [_Size]) restrict(amp,cpu);

template <
    typename _Container
>
array_view(
    int _E0,
    const _Container& _Src);

template <
    typename _Container
>
array_view(
    int _E0,
    int _E1,
    const _Container& _Src);

template <
    typename _Container
>
array_view(
    int _E0,
    int _E1,
    int _E2,
    const _Container& _Src);

array_view(
    int _E0,
    const value_type* _Src)restrict(amp,cpu);

array_view(
    int _E0,
    int _E1,
    const value_type* _Src) restrict(amp,cpu);

array_view(
    int _E0,
    int _E1,
    int _E2,
    const value_type* _Src) restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_Arr_type*<br/>
Тип элемента массива в стиле C, из которого передаются данные.

*_Container*<br/>
Аргумент шаблона, который должен указывать линейный контейнер, который `data()` поддерживает `size()` члены и.

*_E0*<br/>
Наиболее важный компонент экстента этого раздела.

*_E1*<br/>
Наиболее важный компонент в области этого раздела.

*_E2*<br/>
Наименее важный компонент экстента этого раздела.

*_Extent*<br/>
Экстент каждого измерения `array_view` .

*_Other*<br/>
Объект типа, `array_view<T,N>` из которого инициализируется новый `array_view` .

*_Size*<br/>
Размер массива в стиле C, из которого передаются данные.

*_Src*<br/>
Указатель на исходные данные, которые будут скопированы в новый массив.

## <a name="copy_to"></a><a name="copy_to"></a> copy_to

Копирует содержимое `array_view` объекта в указанный целевой объект, вызывая метод `copy(*this, dest)` .

```cpp
void copy_to(
    array<value_type, _Rank>& _Dest) const;

void copy_to(
    array_view<value_type, _Rank>& _Dest) const;
```

### <a name="parameters"></a>Параметры

*_Dest*<br/>
Объект для копирования.

## <a name="data"></a>Данные <a name="data"></a>.

Возвращает указатель на необработанные данные `array_view` .

```cpp
value_type* data() const restrict(amp,
    cpu);

const value_type* data() const restrict(amp,
    cpu);
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на необработанные данные `array_view` .

## <a name="discard_data"></a><a name="discard_data"></a> discard_data

Отменяет текущие данные, лежащие в этом представлении. Это указание оптимизации для среды выполнения, используемое, чтобы избежать копирования текущего содержимого представления на целевой объект `accelerator_view` , к которому он обращается, и его использование рекомендуется, если существующее содержимое не требуется. Этот метод является оператором No-Op при использовании в контексте ограничения (amp)

```cpp
void discard_data() const restrict(cpu);
```

## <a name="extent"></a><a name="extent"></a> экстент

Получает объект `extent`, который определяет форму объекта `array_view`.

```cpp
__declspec(property(get= get_extent)) Concurrency::extent<_Rank> extent;
```

## <a name="get_extent"></a><a name="get_extent"></a> get_extent

Возвращает объект [экстента](extent-class.md) `array_view` объекта.

```cpp
Concurrency::extent<_Rank> get_extent() const restrict(cpu, amp);
```

### <a name="return-value"></a>Возвращаемое значение

`extent`Объект `array_view` объекта

## <a name="get_ref"></a><a name="get_ref"></a> get_ref

Получите ссылку на элемент, индексируемый _Index. В отличие от других операторов индексирования для доступа к array_view ЦП, этот метод не выполняет неявную синхронизацию содержимого этого array_view с ЦП. После доступа к array_view в удаленном расположении или выполнения операции копирования, включающей эту array_view, пользователи должны явным образом синхронизировать array_view с ЦП перед вызовом этого метода. Несоблюдение этого действия приводит к неопределенному поведению.

```cpp
value_type& get_ref(
    const index<_Rank>& _Index) const restrict(amp, cpu);
```

### <a name="parameters"></a>Параметры

*_Index*<br/>
Индекс.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на элемент, индексированный по _Index

## <a name="get_source_accelerator_view"></a><a name="get_source_accelerator_view"></a> get_source_accelerator_view

Возвращает accelerator_view, где расположен источник данных array_view. Если array_view не имеет источника данных, этот API выдает исключение runtime_exception

```cpp
accelerator_view get_source_accelerator_view() const;
```

### <a name="return-value"></a>Возвращаемое значение

## <a name="operator"></a><a name="operator_call"></a> оператор ()

Возвращает значение элемента, заданного параметром или параметрами.

```cpp
value_type& operator() (
    const index<_Rank>& _Index) const restrict(amp,cpu);

typename details::_Projection_result_type<value_type,_Rank>::_Result_type operator() (
    int _I) const restrict(amp,cpu);

value_type& operator() (
    int _I0,
    int _I1) const restrict(amp,cpu);

value_type& operator() (
    int _I0,
    int _I1,
    int _I2) const restrict(amp,cpu);

typename details::_Projection_result_type<value_type,_Rank>::_Const_result_type operator() (
    int _I) const restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_Index*<br/>
Расположение элемента.

*_I0*<br/>
Индекс в первом измерении.

*_I1*<br/>
Индекс во втором измерении.

*_I2*<br/>
Индекс в третьем измерении.

*_I*<br/>
Расположение элемента.

### <a name="return-value"></a>Возвращаемое значение

Значение элемента, заданного параметром или параметрами.

## <a name="operator"></a><a name="operator_at"></a> operator[]

Возвращает элемент, заданный параметрами.

```cpp
typename details::_Projection_result_type<value_type,_Rank>::_Const_result_type operator[] (
    int _I) const restrict(amp,cpu);

value_type& operator[] (
    const index<_Rank>& _Index) const restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_Index*<br/>
Индекс.

*_I*<br/>
Индекс.

### <a name="return-value"></a>Возвращаемое значение

Значение элемента в индексе или `array_view` проецируется на наиболее значимое измерение.

## <a name="operator"></a><a name="operator_eq"></a> Оператор =

Копирует содержимое указанного `array_view` объекта в этот объект.

```cpp
array_view& operator= (
    const array_view& _Other) restrict(amp,cpu);

array_view& operator= (
    const array_view<value_type, _Rank>& _Other) restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_Other*<br/>
Объект, из которого производится `array_view` копирование.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на этот `array_view` объект.

## <a name="rank"></a><a name="rank"></a> Рейтинг

Хранит ранг `array_view` объекта.

```cpp
static const int rank = _Rank;
```

## <a name="refresh"></a><a name="refresh"></a> обновляется

Уведомляет `array_view` объект о том, что связанная с ним память была изменена за пределами `array_view` интерфейса. Вызов этого метода выводит все кэшированные данные в устаревшем виде.

```cpp
void refresh() const restrict(cpu);
```

## <a name="reinterpret_as"></a><a name="reinterpret_as"></a> reinterpret_as

Повторно интерпретирует array_view с помощью одномерного array_view, который может иметь тип значения, отличный от типа исходного array_view.

### <a name="syntax"></a>Синтаксис

```cpp
template <
    typename _Value_type2
>
array_view< _Value_type2, _Rank> reinterpret_as() const restrict(amp,cpu);

template <
    typename _Value_type2
>
array_view<const _Value_type2, _Rank> reinterpret_as() const restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_Value_type2*<br/>
Тип данных нового `array_view` объекта.

### <a name="return-value"></a>Возвращаемое значение

`array_view`Объект или `array_view` объект const, основанный на этом объекте `array_view` , с типом элемента, преобразованным из `T` в `_Value_type2` , и рангом, уменьшенным от *N* до 1.

### <a name="remarks"></a>Комментарии

Иногда удобно просматривать многомерный массив в виде линейного одномерного массива, который может иметь тип значения, отличный от типа исходного массива. Это можно сделать в с `array_view` помощью этого метода.

**Предупреждение об ошибке** Повторное выполнение объекта array_view с использованием другого типа значения является потенциально небезопасной операцией. Эта функция должна использоваться с осторожностью.

Ниже приведен пример:

```cpp
struct RGB { float r; float g; float b; };

array<RGB,3>  a = ...;
array_view<float,1> v = a.reinterpret_as<float>();

assert(v.extent == 3*a.extent);
```

## <a name="section"></a>Раздел <a name="section"></a>

Возвращает подраздел `array_view` объекта, который находится в указанном источнике и, при необходимости, с указанным экстентом.

```cpp
array_view section(
    const Concurrency::index<_Rank>& _Section_origin,
    const Concurrency::extent<_Rank>& _Section_extent) const restrict(amp,cpu);

array_view section(
    const Concurrency::index<_Rank>& _Idx) const restrict(amp,cpu);

array_view section(
    const Concurrency::extent<_Rank>& _Ext) const restrict(amp,cpu);

array_view section(
    int _I0,
    int _E0) const restrict(amp,cpu);

array_view section(
    int _I0,
    int _I1,
    int _E0,
    int _E1) const restrict(amp,cpu);

array_view section(
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

### <a name="return-value"></a>Возвращаемое значение

Подраздел `array_view` объекта, который находится в указанном источнике и, при необходимости, с указанным экстентом. Если указан только `index` объект, подраздел содержит все элементы в связанном экстенте, имеющие индексы, превышающие индексы элементов в `index` объекте.

## <a name="source_accelerator_view"></a><a name="source_accelerator_view"></a> source_accelerator_view

Возвращает accelerator_view источника, с которым связана эта array_view.

```cpp
__declspec(property(get= get_source_accelerator_view)) accelerator_view source_accelerator_view;
```

## <a name="synchronize"></a><a name="synchronize"></a> полнит

Синхронизирует все изменения, внесенные в `array_view` объект, с исходными данными.

```cpp
void synchronize(access_type _Access_type = access_type_read) const restrict(cpu);

void synchronize() const restrict(cpu);
```

### <a name="parameters"></a>Параметры

*_Access_type*<br/>
Предполагаемый [access_type](concurrency-namespace-enums-amp.md#access_type) на целевом [accelerator_view](accelerator-view-class.md). Этот параметр имеет значение по умолчанию `access_type_read` .

## <a name="synchronize_async"></a><a name="synchronize_async"></a> synchronize_async

Асинхронно синхронизирует все изменения, внесенные в `array_view` объект, с исходными данными.

```cpp
concurrency::completion_future synchronize_async(access_type _Access_type = access_type_read) const restrict(cpu);

concurrency::completion_future synchronize_async() const restrict(cpu);
```

### <a name="parameters"></a>Параметры

*_Access_type*<br/>
Предполагаемый [access_type](concurrency-namespace-enums-amp.md#access_type) на целевом [accelerator_view](accelerator-view-class.md). Этот параметр имеет значение по умолчанию `access_type_read` .

### <a name="return-value"></a>Возвращаемое значение

Будущее, на которую следует ожидать завершения операции.

## <a name="synchronize_to"></a><a name="synchronize_to"></a> synchronize_to

Синхронизирует все изменения, внесенные в этот array_view, в указанный accelerator_view.

```cpp
void synchronize_to(
    const accelerator_view& _Accl_view,
    access_type _Access_type = access_type_read) const restrict(cpu);

void synchronize_to(
    const accelerator_view& _Accl_view) const restrict(cpu);
```

### <a name="parameters"></a>Параметры

*_Accl_view*<br/>
Целевой accelerator_view для синхронизации.

*_Access_type*<br/>
Требуемый access_type на целевом accelerator_view. Этот параметр имеет значение по умолчанию access_type_read.

## <a name="synchronize_to_async"></a><a name="synchronize_to_async"></a> synchronize_to_async

Асинхронно синхронизирует любые изменения, внесенные в этот array_view, в указанный accelerator_view.

```cpp
concurrency::completion_future synchronize_to_async(
    const accelerator_view& _Accl_view,
    access_type _Access_type = access_type_read) const restrict(cpu);

concurrency::completion_future synchronize_to_async(
    const accelerator_view& _Accl_view) const restrict(cpu);
```

### <a name="parameters"></a>Параметры

*_Accl_view*<br/>
Целевой accelerator_view для синхронизации.

*_Access_type*<br/>
Требуемый access_type на целевом accelerator_view. Этот параметр имеет значение по умолчанию access_type_read.

### <a name="return-value"></a>Возвращаемое значение

Будущее, на которую следует ожидать завершения операции.

## <a name="value_type"></a><a name="value_type"></a> value_type

Тип значения array_view и привязанного массива.

```cpp
typedef typenamevalue_type value_type;
```

## <a name="view_as"></a><a name="view_as"></a> view_as

Переинтерпретирует этот `array_view` объект как экземпляр с `array_view` другим рангом.

```cpp
template <
    int _New_rank
>
array_view<value_type,_New_rank> view_as(
    const Concurrency::extent<_New_rank>& _View_extent) const restrict(amp,cpu);

template <
    int _New_rank
>
array_view<const value_type,_New_rank> view_as(
    const Concurrency::extent<_New_rank> _View_extent) const restrict(amp,cpu);
```

### <a name="parameters"></a>Параметры

*_New_rank*<br/>
Ранг нового `array_view` объекта.

*_View_extent*<br/>
Изменение формы `extent` .

*value_type*<br/>
Тип данных элементов как в исходном объекте [массива](array-class.md) , так и в возвращенном `array_view` объекте.

### <a name="return-value"></a>Возвращаемое значение

`array_view`Созданный объект.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency (C++ AMP)](concurrency-namespace-cpp-amp.md)
