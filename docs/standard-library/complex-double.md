---
description: 'Дополнительные сведения: комплексное &lt; двойное&gt;'
title: complex&lt;double&gt;
ms.date: 11/04/2016
f1_keywords:
- complex/std::complex<double>
helpviewer_keywords:
- complex<double> function
ms.assetid: 0d0b9d2a-9b9b-410b-82a0-86b6df127e47
ms.openlocfilehash: 9238e71fcdd70576276eb1ba429a48eeec954601
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97325040"
---
# <a name="complexltdoublegt"></a>complex&lt;double&gt;

Описывает объект, хранящий упорядоченную пару объектов обоих типов **`double`** , первый из которых представляет реальную часть комплексного числа, а второй — мнимую часть.

## <a name="syntax"></a>Синтаксис

```cpp
template <>
class complex<double> {
public:
    constexpr complex(
    double RealVal = 0,
    double ImagVal = 0);

constexpr complex(const complex<double>& complexNum);

constexpr explicit complex(const complex<long double>& complexNum);
// rest same as class template complex
};
```

### <a name="parameters"></a>Параметры

*реалвал*\
Значение типа **`double`** для реальной части создаваемого комплексного числа.

*имагвал*\
Значение типа **`double`** для мнимой части создаваемого комплексного числа.

*комплекснум*\
Комплексное число типа **`float`** или типа **`long double`** , реальные и мнимые части которого используются для инициализации комплексного числа создаваемого типа **`double`** .

## <a name="return-value"></a>Возвращаемое значение

Комплексное число типа **`double`** .

## <a name="remarks"></a>Комментарии

Явная специализация шаблона класса Complex до сложного класса типа **`double`** отличается от шаблона класса только в конструкторах, которые он определяет. Преобразование из **`float`** в **`double`** не может быть неявным, но преобразование из в **`long double`** **`double`** **`explicit`** должно иметь значение. Использование **`explicit`** правил инициации при преобразовании типов с помощью синтаксиса назначения.

Дополнительные сведения о шаблоне класса `complex` см. в разделе [сложный класс](../standard-library/complex-class.md). Список членов шаблона класса `complex` см. в разделе.

## <a name="example"></a>Пример

```cpp
// complex_comp_dbl.cpp
// compile with: /EHsc
#include <complex>
#include <iostream>

int main( )
{
   using namespace std;
   double pi = 3.14159265359;

   // The first constructor specifies real & imaginary parts
   complex <double> c1 ( 4.0 , 5.0 );
   cout << "Specifying initial real & imaginary parts,\n"
        << "as type double gives c1 = " << c1 << endl;

   // The second constructor initializes values of the real &
   // imaginary parts using those of complex number of type float
   complex <float> c2float ( 4.0 , 5.0 );
   complex <double> c2double ( c2float );
   cout << "Implicit conversion from type float to type double,"
        << endl << "gives c2double = " << c2double << endl;

   // The third constructor initializes values of the real &
   // imaginary parts using those of a complex number
   // of type long double
   complex <long double> c3longdouble ( 4.0 , 5.0 );
   complex <double> c3double ( c3longdouble );
   cout << "Explicit conversion from type float to type double,"
        << endl << "gives c3longdouble = " << c3longdouble << endl;

   // The modulus and argument of a complex number can be recovered
   double absc3 = abs ( c3longdouble );
   double argc3 = arg ( c3longdouble );
   cout << "The modulus of c3 is recovered from c3 using: abs ( c3 ) = "
        << absc3 << endl;
   cout << "Argument of c3 is recovered from c3 using:" << endl
        << "arg ( c3 ) = " << argc3 << " radians, which is "
        << argc3 * 180 / pi << " degrees." << endl;
}
/* Output:
Specifying initial real & imaginary parts,
as type double gives c1 = (4,5)
Implicit conversion from type float to type double,
gives c2double = (4,5)
Explicit conversion from type float to type double,
gives c3longdouble = (4,5)
The modulus of c3 is recovered from c3 using: abs ( c3 ) = 6.40312
Argument of c3 is recovered from c3 using:
arg ( c3 ) = 0.896055 radians, which is 51.3402 degrees.
*/
```

## <a name="requirements"></a>Требования

**Заголовок**: \<complex>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[сложный класс](../standard-library/complex-class.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
