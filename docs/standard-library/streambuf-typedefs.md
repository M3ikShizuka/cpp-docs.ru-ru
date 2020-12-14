---
description: 'Дополнительные сведения о: &lt; streambuf &gt; typedefs'
title: Определения типов &lt;streambuf&gt;
ms.date: 11/04/2016
f1_keywords:
- iosfwd/std::streambuf
- iosfwd/std::wstreambuf
ms.assetid: 2678e18f-f0f0-4995-bc53-f1bc7dfc4ec6
ms.openlocfilehash: ae5394213143b05704d452e38eaae0b3581849cd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97221973"
---
# <a name="ltstreambufgt-typedefs"></a>Определения типов &lt;streambuf&gt;

[streambuf](#streambuf)\
[встреамбуф](#wstreambuf)

## <a name="streambuf"></a><a name="streambuf"></a> streambuf

Специализация `basic_streambuf` , которая использует **`char`** в качестве параметров шаблона.

```cpp
typedef basic_streambuf<char, char_traits<char>> streambuf;
```

### <a name="remarks"></a>Комментарии

Этот тип является синонимом для шаблона класса [basic_streambuf](../standard-library/basic-streambuf-class.md), специализированного для элементов типа **`char`** с признаками символа по умолчанию.

## <a name="wstreambuf"></a><a name="wstreambuf"></a> встреамбуф

Специализация `basic_streambuf` , которая использует **`wchar_t`** в качестве параметров шаблона.

```cpp
typedef basic_streambuf<wchar_t, char_traits<wchar_t>> wstreambuf;
```

### <a name="remarks"></a>Комментарии

Этот тип является синонимом для шаблона класса [basic_streambuf](../standard-library/basic-streambuf-class.md), специализированного для элементов типа **`wchar_t`** с признаками символа по умолчанию.

## <a name="see-also"></a>См. также раздел

[\<streambuf>](../standard-library/streambuf.md)
