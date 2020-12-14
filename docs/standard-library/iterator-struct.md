---
description: 'Дополнительные сведения: структура итератора'
title: Структура iterator
ms.date: 11/04/2016
f1_keywords:
- xutility/std::iterator
helpviewer_keywords:
- iterator class
- iterator struct
ms.assetid: c74c8000-8b18-4829-9b71-6103c4229b74
ms.openlocfilehash: 81a35fd749b3393a0235fdac8c4bf13a1ef5af79
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97254330"
---
# <a name="iterator-struct"></a>Структура iterator

Пустая базовая структура, используемая, чтобы гарантировать, что определяемый пользователем класс итератора правильно работает с `iterator_trait` s.

## <a name="syntax"></a>Синтаксис

```cpp
struct iterator {
   typedef Category iterator_category;
   typedef Type value_type;
   typedef Distance difference_type;
   typedef Distance distance_type;
   typedef Pointer pointer;
   typedef Reference reference;
   };
```

## <a name="remarks"></a>Remarks

Данная структура-шаблон используется как базовый тип для всех итераторов. Она определяет типы членов

- `iterator_category` (синоним для параметра-шаблона `Category`).

- `value_type` (синоним для параметра-шаблона `Type`).

- `difference_type` (синоним для параметра-шаблона `Distance`).

- `distance_type` (синоним для параметра-шаблона `Distance`)

- `pointer` (синоним для параметра-шаблона `Pointer`).

- `reference` (синоним для параметра-шаблона `Reference`).

Обратите внимание, что `value_type` не должен быть константным типом, даже если `pointer` точки в объекте **`const`** `Type` и ссылка указывает на объект **`const`** `Type` .

## <a name="example"></a>Пример

См. раздел [iterator_traits](../standard-library/iterator-traits-struct.md) с примером того, как объявить и использовать типы в базовом классе итератора.

## <a name="requirements"></a>Требования

**Заголовок:**\<iterator>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[\<iterator>](../standard-library/iterator.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md)
