---
description: 'Дополнительные сведения о: unchecked_array_iterator классе'
title: Класс unchecked_array_iterator
ms.date: 11/04/2016
f1_keywords:
- stdext::unchecked_array_iterator
ms.assetid: 693b3b30-4e3a-465b-be06-409700bc50b1
ms.openlocfilehash: 6f2bbe4c31a76101a04e8c5be6a4e0dcf67cf87e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97132747"
---
# <a name="unchecked_array_iterator-class"></a>Класс unchecked_array_iterator

Класс `unchecked_array_iterator` позволяет заключить массив или указатель в оболочку из непроверенного итератора. Используйте этот класс в качестве оболочки (с функцией [make_unchecked_array_iterator](../standard-library/iterator-functions.md#make_unchecked_array_iterator)) для необработанных указателей или массивов с целью проверки предупреждений об указателях и управления этими предупреждениями вместо того, чтобы глобально отключать эти предупреждения. Если возможно, используйте проверенную версию этого класса, [checked_array_iterator](../standard-library/checked-array-iterator-class.md).

> [!NOTE]
> Этот класс является расширением стандартной библиотеки C++, которое предоставляется Майкрософт. Код, реализованный с помощью этой функции, нельзя перенести в стандартные среды сборки C, не поддерживающие это расширение Microsoft.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Iterator>
class unchecked_array_iterator;
```

## <a name="remarks"></a>Remarks

Этот класс определяется в пространстве имен [stdext](../standard-library/stdext-namespace.md).

Это непроверенная версия [класса checked_array_iterator](../standard-library/checked-array-iterator-class.md), и она поддерживает те же перегрузки и члены. Дополнительные сведения о функции проверяемого итератора с примерами кода см. в разделе [Проверяемые итераторы](../standard-library/checked-iterators.md).

## <a name="requirements"></a>Требования

**Заголовок:**\<iterator>

**Пространство имен:** stdext

## <a name="see-also"></a>См. также раздел

[\<iterator>](../standard-library/iterator.md)\
[Справочник по стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md)
