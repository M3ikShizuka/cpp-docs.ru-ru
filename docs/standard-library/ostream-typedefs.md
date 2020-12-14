---
description: 'Дополнительные сведения о: &lt; ostream &gt; typedefs'
title: Определения типов &lt;ostream&gt;
ms.date: 11/04/2016
f1_keywords:
- iosfwd/std::ostream
- iosfwd/std::wostream
ms.assetid: 2ec4dc52-a01f-4654-bd65-dd5288777c48
ms.openlocfilehash: 886fb729f389fac161e4d154e00898b530d1d9f7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193023"
---
# <a name="ltostreamgt-typedefs"></a>Определения типов &lt;ostream&gt;

[ostream](#ostream)\
[wostream](#wostream)

## <a name="ostream"></a><a name="ostream"></a> ostream

Создает тип из basic_ostream, который специализируется на **`char`** и `char_traits` специализируется на **`char`** .

```cpp
typedef basic_ostream<char, char_traits<char>> ostream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_ostream](../standard-library/basic-ostream-class.md)шаблона класса, специализированного для элементов типа **`char`** с признаками символа по умолчанию.

## <a name="wostream"></a><a name="wostream"></a> wostream

Создает тип из basic_ostream, который специализируется на **`wchar_t`** и `char_traits` специализируется на **`wchar_t`** .

```cpp
typedef basic_ostream<wchar_t, char_traits<wchar_t>> wostream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_ostream](../standard-library/basic-ostream-class.md)шаблона класса, специализированного для элементов типа **`wchar_t`** с признаками символа по умолчанию.

## <a name="see-also"></a>См. также раздел

[\<ostream>](../standard-library/ostream.md)
