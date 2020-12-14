---
description: 'Дополнительные сведения о: &lt; FStream &gt; typedefs'
title: Определения типов &lt;fstream&gt;
ms.date: 11/04/2016
f1_keywords:
- fstream/std::filebuf
- fstream/std::fstream
- fstream/std::ifstream
- fstream/std::ofstream
- fstream/std::wfilebuf
- fstream/std::wfstream
- fstream/std::wifstream
- fstream/std::wofstream
ms.assetid: 8dddef2d-7f17-42a6-ba08-6f6f20597d23
ms.openlocfilehash: cf3a7d686bb1e6d6004aaf91fa50294225f0362d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97232256"
---
# <a name="ltfstreamgt-typedefs"></a>Определения типов &lt;fstream&gt;

[филебуф](#filebuf)\
[FStream](#fstream)\
[ifstream](#ifstream)\
[ofstream](#ofstream)\
[вфилебуф](#wfilebuf)\
[вфстреам](#wfstream)\
[вифстреам](#wifstream)\
[wofstream](#wofstream)

## <a name="filebuf"></a><a name="filebuf"></a> филебуф

Тип, `basic_filebuf` специализированный для **`char`** параметров шаблона.

```cpp
typedef basic_filebuf<char, char_traits<char>> filebuf;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_filebuf](../standard-library/basic-filebuf-class.md)шаблона класса, специализированного для элементов типа **`char`** с признаками символа по умолчанию.

## <a name="fstream"></a><a name="fstream"></a> FStream

Тип, `basic_fstream` специализированный для **`char`** параметров шаблона.

```cpp
typedef basic_fstream<char, char_traits<char>> fstream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_fstream](../standard-library/basic-fstream-class.md)шаблона класса, специализированного для элементов типа **`char`** с признаками символа по умолчанию.

## <a name="ifstream"></a><a name="ifstream"></a> ifstream

Определяет поток, который используется для последовательного чтения однобайтовых символов из файла. `ifstream` — Это typedef, который специализирует шаблон класса `basic_ifstream` для **`char`** .

Также существует `wifstream` Определение типа, которое специализируется `basic_ifstream` на чтении **`wchar_t`** двухбайтовых символов. Дополнительные сведения см. в описании [wifstream](../standard-library/fstream-typedefs.md#wifstream).

```cpp
typedef basic_ifstream<char, char_traits<char>> ifstream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_ifstream](../standard-library/basic-ifstream-class.md)шаблона класса, специализированного для элементов типа Char с признаками символа по умолчанию. Пример:

```cpp
using namespace std;

ifstream infile("existingtextfile.txt");

if (!infile.bad())
{
    // Dump the contents of the file to cout.
    cout << infile.rdbuf();infile.close();
}
```

## <a name="ofstream"></a><a name="ofstream"></a> ofstream

Тип, `basic_ofstream` специализированный для **`char`** параметров шаблона.

```cpp
typedef basic_ofstream<char, char_traits<char>> ofstream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_ofstream](../standard-library/basic-ofstream-class.md)шаблона класса, специализированного для элементов типа **`char`** с признаками символа по умолчанию.

## <a name="wfstream"></a><a name="wfstream"></a> вфстреам

Тип, `basic_fstream` специализированный для **`wchar_t`** параметров шаблона.

```cpp
typedef basic_fstream<wchar_t, char_traits<wchar_t>> wfstream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_fstream](../standard-library/basic-fstream-class.md)шаблона класса, специализированного для элементов типа **`wchar_t`** с признаками символа по умолчанию.

## <a name="wifstream"></a><a name="wifstream"></a> вифстреам

Тип, `basic_ifstream` специализированный для **`wchar_t`** параметров шаблона.

```cpp
typedef basic_ifstream<wchar_t, char_traits<wchar_t>> wifstream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_ifstream](../standard-library/basic-ifstream-class.md)шаблона класса, специализированного для элементов типа **`wchar_t`** с признаками символа по умолчанию.

## <a name="wofstream"></a><a name="wofstream"></a> wofstream

Тип, `basic_ofstream` специализированный для **`wchar_t`** параметров шаблона.

```cpp
typedef basic_ofstream<wchar_t, char_traits<wchar_t>> wofstream;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_ofstream](../standard-library/basic-ofstream-class.md)шаблона класса, специализированного для элементов типа **`wchar_t`** с признаками символа по умолчанию.

## <a name="wfilebuf"></a><a name="wfilebuf"></a> вфилебуф

Тип, `basic_filebuf` специализированный для **`wchar_t`** параметров шаблона.

```cpp
typedef basic_filebuf<wchar_t, char_traits<wchar_t>> wfilebuf;
```

### <a name="remarks"></a>Комментарии

Тип является синонимом [basic_filebuf](../standard-library/basic-filebuf-class.md)шаблона класса, специализированного для элементов типа **`wchar_t`** с признаками символа по умолчанию.

## <a name="see-also"></a>См. также раздел

[\<fstream>](../standard-library/fstream.md)
