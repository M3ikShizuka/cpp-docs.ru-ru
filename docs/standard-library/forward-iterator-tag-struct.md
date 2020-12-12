---
description: 'Дополнительные сведения о: forward_iterator_tag struct'
title: Структура forward_iterator_tag
ms.date: 11/04/2016
f1_keywords:
- xutility/std::forward_iterator_tag
helpviewer_keywords:
- forward_iterator_tag struct
- forward_iterator_tag class
ms.assetid: 68b633ac-b135-4e9e-837d-14248a262ec5
ms.openlocfilehash: 9b8b5ea7ff4e7d68c14c892d4ba6ef96f275b7da
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324300"
---
# <a name="forward_iterator_tag-struct"></a>Структура forward_iterator_tag

Класс, предоставляющий тип возвращаемого значения для функции **iterator_category**, которая представляет собой прямой итератор.

## <a name="syntax"></a>Синтаксис

```cpp
struct forward_iterator_tag    : public input_iterator_tag {};
```

## <a name="remarks"></a>Remarks

Классы категории тегов используются как теги компиляции для выбора алгоритма. Функция шаблона должна найти наиболее точно определенную категорию своего аргумента итератора, чтобы можно было использовать наиболее эффективный алгоритм во время компиляции. Для каждого итератора типа `Iterator` категория `iterator_traits`< `Iterator`> **::iterator_category** должна быть определена как наиболее точный тег категории, который описывает поведение итератора.

Тип аналогичен **итератору** : \< **Iter**> **: iterator_category** , когда **iter** описывает объект, который может использоваться в качестве прямого итератора.

## <a name="example"></a>Пример

См. в разделе [iterator_traits](../standard-library/iterator-traits-struct.md) или [random_access_iterator_tag](../standard-library/random-access-iterator-tag-struct.md) пример использования **iterator_tag**.

## <a name="requirements"></a>Требования

**Заголовок:**\<iterator>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Структура input_iterator_tag](../standard-library/input-iterator-tag-struct.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md)
