---
description: 'Дополнительные сведения: структура duration_values'
title: Структура duration_values
ms.date: 11/04/2016
f1_keywords:
- chrono/std::chrono::duration_values
- chrono/std::chrono::duration_values::max
- chrono/std::chrono::duration_values::min
- chrono/std::chrono::duration_values::zero
ms.assetid: 7f66d2e3-1faf-47c3-b47e-08f2a87f20e8
ms.openlocfilehash: 9bf784b0976a06c6d395498084508251d9ebd4bb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324479"
---
# <a name="duration_values-structure"></a>Структура duration_values

Предоставляет конкретные значения для параметра-шаблона [длительности](../standard-library/duration-class.md)`Rep`.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Rep>
struct duration_values;
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[max](#max)|Статический. Указывает верхний предел для значения типа `Rep`.|
|[min](#min)|Статический. Указывает нижний предел для значения типа `Rep`.|
|[нуль](#zero)|Статический. Возвращает `Rep(0)`.|

## <a name="requirements"></a>Требования

**Заголовок:**\<chrono>

**Пространство имен:** std::chrono

## <a name="duration_valuesmax"></a><a name="max"></a> duration_values:: Max

Статический метод, который возвращает верхнюю границу значений типа `Ref`.

```cpp
static constexpr Rep max();
```

### <a name="return-value"></a>Возвращаемое значение

Фактически возвращает `numeric_limits<Rep>::max()`.

### <a name="remarks"></a>Комментарии

Если `Rep` является пользовательским типом, возвращаемое значение должно быть больше [duration_values::zero](#zero).

## <a name="duration_valuesmin"></a><a name="min"></a> duration_values:: min

Статический метод, который возвращает нижнюю границу для значений типа `Ref`.

```cpp
static constexpr Rep min();
```

### <a name="return-value"></a>Возвращаемое значение

Фактически возвращает `numeric_limits<Rep>::lowest()`.

### <a name="remarks"></a>Комментарии

Если `Rep` является пользовательским типом, возвращаемое значение должно быть меньше или равно [duration_values::zero](#zero).

## <a name="duration_valueszero"></a><a name="zero"></a> duration_values:: Zero

Возвращает `Rep(0)`.

```cpp
static constexpr Rep zero();
```

### <a name="remarks"></a>Комментарии

Если `Rep` является пользовательским типом, возвращаемое значение должно представлять аддитивную бесконечность.

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[\<chrono>](../standard-library/chrono.md)
