---
description: 'Дополнительные сведения: char_traits &lt; char16_t &gt; struct'
title: Структура char_traits&lt;char16_t&gt;
ms.date: 11/04/2016
f1_keywords:
- char_traits<char16_t>
- iosfwd/std::char_traits<char16_t>
helpviewer_keywords:
- char_traits<char16_t> class
ms.assetid: 5daf3b62-dd6e-451f-b189-0350a04ff966
ms.openlocfilehash: 2ad725b514d6804edfdea6d4ba72c2cfd44c4f21
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97325266"
---
# <a name="char_traitsltchar16_tgt-struct"></a>Структура char_traits&lt;char16_t&gt;

Структура, которая является специализацией структуры шаблона, **char_traits \<CharType>** к элементу типа **`char16_t`** .

## <a name="syntax"></a>Синтаксис

```cpp
template <>
struct char_traits<char16_t>;
```

## <a name="remarks"></a>Remarks

Специализация позволяет структуре использовать преимущества библиотечных функций, которые управляют объектами типа **`char16_t`** .

## <a name="requirements"></a>Требования

**Заголовок:**\<string>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[\<string>](../standard-library/string.md)\
[Структура char_traits](../standard-library/char-traits-struct.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
