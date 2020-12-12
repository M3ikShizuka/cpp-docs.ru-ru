---
description: 'Дополнительные сведения о: &lt; &gt; Операторы IStream'
title: Операторы &lt;istream&gt;
ms.date: 11/04/2016
f1_keywords:
- istream/std::operator&gt;&gt;
ms.assetid: 7174da41-f301-4a34-b631-0ab918b188d2
ms.openlocfilehash: 68bf59480af68248533f55ef32de4525a4d900d5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97277886"
---
# <a name="ltistreamgt-operators"></a>Операторы &lt;istream&gt;

## <a name="operatorgtgt"></a><a name="op_gt_gt"></a> станции&gt;&gt;

Извлекает символы и строки из потока.

```cpp
template <class Elem, class Tr>
basic_istream<Elem, Tr>& operator>>(
    basic_istream<Elem, Tr>& Istr,
    Elem* str);

template <class Elem, class Tr>
basic_istream<Elem, Tr>& operator>>(
    basic_istream<Elem, Tr>& Istr,
    Elem& Ch);

template <class Tr>
basic_istream<char, Tr>& operator>>(
    basic_istream<char, Tr>& Istr,
    signed char* str);

template <class Tr>
basic_istream<char, Tr>& operator>>(
    basic_istream<char, Tr>& Istr,
    signed char& Ch);

template <class Tr>
basic_istream<char, Tr>& operator>>(
    basic_istream<char, Tr>& Istr,
    unsigned char* str);

template <class Tr>
basic_istream<char, Tr>& operator>>(
    basic_istream<char, Tr>& Istr,
    unsigned char& Ch);

template <class Elem, class Tr, class Type>
basic_istream<Elem, Tr>& operator>>(
    basic_istream<char, Tr>&& Istr,
    Type& val);
```

### <a name="parameters"></a>Параметры

*Канал*\
Символ.

*ISTR*\
Поток.

*str*\
Строка.

*Val*\
Тип.

### <a name="return-value"></a>Возвращаемое значение

Поток.

### <a name="remarks"></a>Комментарии

Класс `basic_istream` также определяет несколько операторов извлечения. Дополнительные сведения см. в разделе [basic_istream::operator>>](../standard-library/basic-istream-class.md#op_gt_gt).

Шаблон функции:

```cpp
template <class Elem, class Tr>
basic_istream<Elem, Tr>& operator>>(
    basic_istream<Elem, Tr>& Istr, Elem* str);
```

Извлекает до `N - 1` элементов и сохраняет их в массив, начиная с *str*. Если значение `Istr.` [Width](../standard-library/ios-base-class.md#width) больше нуля, *N* имеет значение `Istr.width` ; в противном случае — размер самого крупного массива `Elem` , который может быть объявлен. Функция всегда сохраняет значение `Elem()` после извлеченных элементов, которые он хранит. Извлечение останавливается на раннем конце файла, на символ со значением `Elem(0)` (который не извлекается) или на любом элементе (который не извлекается), который будет отклонен [WS](../standard-library/istream-functions.md#ws). Если функция не извлекает ни одного элемента, она вызывает `Istr.` [`setstate`](../standard-library/basic-ios-class.md#setstate) `(failbit)` . В любом случае он вызывает `Istr.width(0)` и возвращает *ISTR*.

**Примечание по безопасности** Строка, завершающаяся нулем, извлекаемая из входного потока, не должна превышать размер строки *целевого буфера.* Дополнительные сведения см. в разделе [Как избежать переполнения буфера](/windows/win32/SecBP/avoiding-buffer-overruns).

Шаблон функции:

```cpp
template <class Elem, class Tr>
basic_istream<Elem, Tr>& operator>>(
    basic_istream<Elem, Tr>& Istr, Elem& Ch);
```

Извлекает элемент, если это возможно, и сохраняет его в *CH*. В противном случае он вызывает `is.` [`setstate`](../standard-library/basic-ios-class.md#setstate) `(failbit)` . В любом случае возвращается *ISTR*.

Шаблон функции:

```cpp
template <class Tr>
basic_istream<char, Tr>& operator>>(
    basic_istream<char, Tr>& Istr, signed char* str);
```

Возвращает `Istr >> ( char * ) str`.

Шаблон функции:

```cpp
template <class Tr>
basic_istream<char, Tr>& operator>>(
    basic_istream<char, Tr>& Istr, signed char& Ch);
```

Возвращает `Istr >> ( char& ) Ch`.

Шаблон функции:

```cpp
template <class Tr>
basic_istream<char, Tr>& operator>>(
    basic_istream<char, Tr>& Istr, unsigned char* str);
```

Возвращает `Istr >> ( char * ) str`.

Шаблон функции:

```cpp
template <class Tr>
basic_istream<char, Tr>& operator>>(
    basic_istream<char, Tr>& Istr, unsigned char& Ch);
```

Возвращает `Istr >> ( char& ) Ch`.

Шаблон функции:

```cpp
template <class Elem, class Tr, class Type>
basic_istream<Elem, Tr>& operator>>(
    basic_istream<char, Tr>&& Istr,
    Type& val);
```

Возвращает `Istr >> val` (и преобразует ссылку rvalue в `Istr` значение lvalue в процессе).

### <a name="example"></a>Пример

```cpp
// istream_op_extract.cpp
// compile with: /EHsc
#include <iostream>
using namespace std;

int main( )
{
   ws( cin );
   char c[10];

   cin.width( 9 );
   cin >> c;
   cout << c << endl;
}
```

## <a name="see-also"></a>См. также раздел

[\<istream>](../standard-library/istream.md)
