---
description: 'Дополнительные сведения о: input_iterator_tag struct'
title: Структура input_iterator_tag
ms.date: 11/04/2016
f1_keywords:
- xutility/std::input_iterator_tag
helpviewer_keywords:
- input_iterator_tag class
- input_iterator_tag struct
ms.assetid: ad68a4c6-f315-4ce1-8b74-c1fc71bd1577
ms.openlocfilehash: 92bd110af71aecfa632b8e739126698eba457019
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97231710"
---
# <a name="input_iterator_tag-struct"></a>Структура input_iterator_tag

Класс, предоставляющий тип возвращаемого значения для `iterator_category` функции, представляющей итератор ввода.

## <a name="syntax"></a>Синтаксис

input_iterator_tag структуры {} ;

## <a name="remarks"></a>Комментарии

Классы категории тегов используются как теги компиляции для выбора алгоритма. Функция шаблона должна найти наиболее точно определенную категорию своего аргумента итератора, чтобы можно было использовать наиболее эффективный алгоритм во время компиляции. Для каждого итератора типа `Iterator` категория `iterator_traits`< `Iterator`> **::iterator_category** должна быть определена как наиболее точный тег категории, который описывает поведение итератора.

Этот тип совпадает с **итератором** : \< **Iter**> **iterator_category** `Iter` , когда описывает объект, который может выступать в качестве итератора ввода.

## <a name="example"></a>Пример

Пример использования s см. в разделе [iterator_traits](../standard-library/iterator-traits-struct.md) или [random_access_iterator_tag](../standard-library/random-access-iterator-tag-struct.md) `iterator_tag` .

## <a name="requirements"></a>Требования

**Заголовок:**\<iterator>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md)
