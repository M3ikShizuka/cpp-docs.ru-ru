---
description: 'Дополнительные сведения о: gslice_array классе'
title: Класс gslice_array
ms.date: 11/04/2016
f1_keywords:
- valarray/std::gslice_array
helpviewer_keywords:
- gslice_array class
ms.assetid: ad1b4514-b14a-4baf-a293-d5a8e8674c75
ms.openlocfilehash: 2c3cf29cd80d874265ec86d5c31a10e5c8359b8e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97232035"
---
# <a name="gslice_array-class"></a>Класс gslice_array

Внутренний, вспомогательный шаблон класса, поддерживающий общие объекты-срезы путем предоставления операций между массивами подмножества, определенными общим срезом valarray.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Type>
class gslice_array : public gsplice {
public:
    typedef Type value_type;
    void operator=(const valarray<Type>& x) const;

    void operator=(const Type& x) const;

    void operator*=(const valarray<Type>& x) const;

    void operator/=(const valarray<Type>& x) const;

    void operator%=(const valarray<Type>& x) const;

    void operator+=(const valarray<Type>& x) const;

    void operator-=(const valarray<Type>& x) const;

    void operator^=(const valarray<Type>& x) const;

    void operator&=(const valarray<Type>& x) const;

    void operator|=(const valarray<Type>& x) const;

    void operator<<=(const valarray<Type>& x) const;

    void operator>>=(const valarray<Type>& x) const;

// The rest is private or implementation defined
}
```

## <a name="remarks"></a>Remarks

Класс описывает объект, хранящий ссылку на объект `va` класса [valarray](../standard-library/valarray-class.md) **\<Type>** , а также объект `gs` класса [gslice](../standard-library/gslice-class.md) , описывающий последовательность элементов для выбора из `valarray<Type>` объекта.

`gslice_array<Type>`Объект создается только путем написания выражения вида « [ва»&#91;GS&#93;](../standard-library/valarray-class.md#op_at). Функции-члены класса gslice_array ведут себя как соответствующие сигнатуры функций, определенные для `valarray<Type>` , за исключением того, что затрагивается только последовательность выбранных элементов.

Шаблон класса создается косвенно определенными valarray операциями и не может использоваться непосредственно в программе. Вместо этого используется внутренний вспомогательный шаблон класса, используемый оператором подстрочного индекса:

`gslice_array`\< **Type**>`valarray` \< **Type**> :: `operator[]` ( **констгслице&**).

`gslice_array<Type>`Объект создается только путем написания выражения формы `va[gsl]` для среза `gsl` valarray `va` . Функции-члены класса gslice_array ведут себя как соответствующие сигнатуры функций, определенные для `valarray<Type>` , за исключением того, что затрагивается только последовательность выбранных элементов. Последовательность, управляемая классом gslice_array, определяется тремя параметрами конструктора среза: индексом первого элемента в первом срезе, количеством элементов в каждом срезе и расстояние между элементами в каждом срезе.

В следующем примере:

```cpp
const size_t lv[] = {2, 3};
const size_t dv[] = {7, 2};
const valarray<size_t> len(lv, 2), str(dv, 2);

// va[gslice(3, len, str)] selects elements with
//   indices 3, 5, 7, 10, 12, 14
```

Чтобы процедура была действительной, индексы должны быть действительными.

## <a name="example"></a>Пример

Пример объявления и использования класса slice_array см. в разделе [gslice::gslice](../standard-library/gslice-class.md#gslice).

## <a name="requirements"></a>Требования

**Заголовок:**\<valarray>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
