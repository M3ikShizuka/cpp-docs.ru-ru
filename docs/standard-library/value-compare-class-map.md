---
description: 'Дополнительные сведения о: value_compare классе ( &lt; Map &gt; )'
title: Класс value_compare (&lt;map&gt;)
ms.date: 11/04/2016
f1_keywords:
- std::value_compare
- std.value_compare
- map/std::value_compare
helpviewer_keywords:
- std::value_compare
ms.assetid: ea97c1d0-04b2-4d42-8d96-23522c04cc41
ms.openlocfilehash: c5b7ba865606e0bc5a5c8238de72824f9061c1b5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97312817"
---
# <a name="value_compare-class-ltmapgt"></a>Класс value_compare (&lt;map&gt;)

Предоставляет объект функции, который может сравнить элементы объекта map, сравнивая значения их ключей, чтобы определить их относительный порядок в объекте map.

## <a name="syntax"></a>Синтаксис

```cpp
class value_compare : public binary_function<value_type, value_type, bool>
{
public:
    bool operator()(const value_type& left, const value_type& right) const;
    value_compare(key_compare pred) : comp(pred);
protected:
    key_compare comp;
};
```

## <a name="remarks"></a>Remarks

Критерий сравнения, предоставляемый `value_compare` между `value_types` целыми элементами, содержащимися в сопоставлении, вызывается путем сравнения ключей соответствующих элементов с помощью вспомогательной конструкции класса. Оператор функции-члена использует объект `comp` типа, `key_compare` хранящийся в объекте функции, предоставляемом функцией, `value_compare` для сравнения компонентов ключа сортировки двух элементов.

Для наборов и множественных наборов, которые представляют собой простые контейнеры, в которых значения ключей идентичны значениям элементов, `value_compare` эквивалентно `key_compare`; для сопоставлений и объектов multimap, это не так, так как элементы типа `pair` не эквивалентны значению ключа элемента.

## <a name="example"></a>Пример

См. пример для [value_comp](../standard-library/map-class.md#value_comp) в качестве примера объявления и использования `value_compare`.

## <a name="requirements"></a>Требования

**Заголовок:**\<map>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Структура binary_function](../standard-library/binary-function-struct.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md)
