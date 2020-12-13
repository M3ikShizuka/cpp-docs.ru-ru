---
description: 'Дополнительные сведения о: slice_array классе'
title: Класс slice_array
ms.date: 11/04/2016
f1_keywords:
- valarray/std::slice_array
helpviewer_keywords:
- slice_array class
ms.assetid: a182d5f7-f35c-4e76-86f2-b5ac64ddc846
ms.openlocfilehash: 580a09d99b08bc563c64571247d74a980eb229f9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97153984"
---
# <a name="slice_array-class"></a>Класс slice_array

Внутренний, вспомогательный шаблон класса, поддерживающий объекты-срезы путем предоставления операций между массивами подмножества, определяемыми срезом valarray.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Type>
class slice_array : public slice {
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

Класс описывает объект, хранящий ссылку на объект класса [valarray](../standard-library/valarray-class.md) **\<Type>** , а также объект [среза](../standard-library/slice-class.md)класса, который описывает последовательность элементов для выбора из объекта **valarray \<Type>** .

Шаблон класса создается косвенно определенными valarray операциями и не может использоваться непосредственно в программе. Внутренний, вспомогательный шаблон класса, используемый оператором подстрочного индекса:

`slice_array`\< **Type**>`valarray` <  **Введите**:: `operator[]` ( `slice` ).

`slice_array<Type>`Объект создается только путем написания выражения формы [&#91;SL&#93;](../standard-library/valarray-class.md#op_at)для среза `sl` valarray `va` . Функции-члены класса slice_array ведут себя как соответствующие сигнатуры функций, определенные для `valarray<Type>` , за исключением того, что затрагивается только последовательность выбранных элементов. Последовательность, управляемая классом slice_array, определяется тремя параметрами конструктора среза: индексом первого элемента в срезе, количеством элементов и расстоянием между элементами. Slice_array вырезание из valarray `va` , объявленного по **ва**[ `slice` (2, 5, 3)], выбирает элементы с индексами 2, 5, 8, 11 и 14 от `va` . Чтобы процедура была действительной, индексы должны быть действительными.

## <a name="example"></a>Пример

Пример объявления и использования класса slice_array см. в разделе [slice::slice](../standard-library/slice-class.md#slice).

## <a name="requirements"></a>Требования

**Заголовок:**\<valarray>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
