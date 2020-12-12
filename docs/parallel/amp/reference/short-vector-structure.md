---
description: 'Дополнительные сведения: структура short_vector'
title: Структура short_vector
ms.date: 11/04/2016
f1_keywords:
- short_vector
- AMP_SHORT_VECTORS/short_vector
- AMP_SHORT_VECTORS/Concurrency::graphics::short_vector::short_vector Constructor
ms.assetid: e4f50b8f-1150-437d-b58c-79c5fb883708
ms.openlocfilehash: 54879df686210606c99a1ae5b9ccc7a31f7fca25
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327600"
---
# <a name="short_vector-structure"></a>Структура short_vector

short_vector предоставляет определения метапрограммирование, которые полезны для универсального программирования коротких векторов.

## <a name="syntax"></a>Синтаксис

```cpp
template<
    typename _Scalar_type,
    int _Size
>
struct short_vector;
template<>
struct short_vector<unsigned int, 1>;
template<>
struct short_vector<unsigned int, 2>;
template<>
struct short_vector<unsigned int, 3>;
template<>
struct short_vector<unsigned int, 4>;
template<>
struct short_vector<int, 1>;
template<>
struct short_vector<int, 2>;
template<>
struct short_vector<int, 3>;
template<>
struct short_vector<int, 4>;
template<>
struct short_vector<float, 1>;
template<>
struct short_vector<float, 2>;
template<>
struct short_vector<float, 3>;
template<>
struct short_vector<float, 4>;
template<>
struct short_vector<unorm, 1>;
template<>
struct short_vector<unorm, 2>;
template<>
struct short_vector<unorm, 3>;
template<>
struct short_vector<unorm, 4>;
template<>
struct short_vector<norm, 1>;
template<>
struct short_vector<norm, 2>;
template<>
struct short_vector<norm, 3>;
template<>
struct short_vector<norm, 4>;
template<>
struct short_vector<double, 1>;
template<>
struct short_vector<double, 2>;
template<>
struct short_vector<double, 3>;
template<>
struct short_vector<double, 4>;
```

### <a name="parameters"></a>Параметры

*_Scalar_type*<br/>

*_Size*<br/>

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`type`||

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Конструктор short_vector::short_vector](#ctor)||

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`short_vector`

## <a name="requirements"></a>Требования

**Заголовок:** amp_short_vectors. h

**Пространство имен:** Concurrency:: Graphics

## <a name="short_vectorshort_vector-constructor"></a><a name="ctor"></a> Конструктор short_vector:: short_vector

```cpp
short_vector();
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency::graphics](concurrency-graphics-namespace.md)
