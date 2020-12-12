---
description: 'Дополнительные сведения о: &lt; IStream &gt; typedefs'
title: Определения типов &lt;istream&gt;
ms.date: 11/04/2016
f1_keywords:
- istream/std::iostream
- istream/std::istream
- istream/std::wiostream
- istream/std::wistream
ms.assetid: 55bc1f84-53a7-46ca-a36f-ac6ef75d0374
ms.openlocfilehash: 576d1be7733a01689b4cfc511049dfad89390f63
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97277860"
---
# <a name="ltistreamgt-typedefs"></a>Определения типов &lt;istream&gt;

[iostream](#iostream)\
[IStream](#istream)\
[виостреам](#wiostream)\
[wistream](#wistream)

## <a name="iostream"></a><a name="iostream"></a> iostream

Тип, `basic_iostream` специализированный для **`char`** .

```cpp
typedef basic_iostream<char, char_traits<char>> iostream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_iostream](../standard-library/basic-iostream-class.md)шаблона класса, специализированного для элементов типа **`char`** с признаками символа по умолчанию.

## <a name="istream"></a><a name="istream"></a> IStream

Тип, `basic_istream` специализированный для **`char`** .

```cpp
typedef basic_istream<char, char_traits<char>> istream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_istream](../standard-library/basic-istream-class.md)шаблона класса, специализированного для элементов типа **`char`** с признаками символа по умолчанию.

## <a name="wiostream"></a><a name="wiostream"></a> виостреам

Тип, `basic_iostream` специализированный для **`wchar_t`** .

```cpp
typedef basic_iostream<wchar_t, char_traits<wchar_t>> wiostream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_iostream](../standard-library/basic-iostream-class.md)шаблона класса, специализированного для элементов типа **`wchar_t`** с признаками символа по умолчанию.

## <a name="wistream"></a><a name="wistream"></a> вистреам

Тип, `basic_istream` специализированный для **`wchar_t`** .

```cpp
typedef basic_istream<wchar_t, char_traits<wchar_t>> wistream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_istream](../standard-library/basic-istream-class.md)шаблона класса, специализированного для элементов типа **`wchar_t`** с признаками символа по умолчанию.

## <a name="see-also"></a>См. также раздел

[\<istream>](../standard-library/istream.md)
