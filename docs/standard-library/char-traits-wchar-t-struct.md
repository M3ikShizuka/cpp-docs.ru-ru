---
description: 'Дополнительные сведения: char_traits &lt; wchar_t &gt; struct'
title: Структура char_traits&lt;wchar_t&gt;
ms.date: 11/04/2016
f1_keywords:
- char_traits<wchar_t>
- iosfwd/std::char_traits<wchar_t>
helpviewer_keywords:
- char_traits<wchar_t> class
ms.assetid: 31f34072-04d6-4871-88fe-48e17d473484
ms.openlocfilehash: 0276f4b50cb0039d0bec49b1b3eb2a0b3b2463aa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97325226"
---
# <a name="char_traitsltwchar_tgt-struct"></a>Структура char_traits&lt;wchar_t&gt;

Класс, являющийся специализацией структуры шаблона, **char_traits \<CharType>** элементу типа **`wchar_t`** .

## <a name="syntax"></a>Синтаксис

```cpp
template <>
struct char_traits<wchar_t>;
```

## <a name="remarks"></a>Remarks

Специализация позволяет структуре использовать преимущества библиотечных функций, которые управляют объектами этого типа **`wchar_t`** .

## <a name="requirements"></a>Требования

**Заголовок:**\<string>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Структура char_traits](../standard-library/char-traits-struct.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
