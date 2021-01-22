---
description: 'Дополнительные сведения: &lt; сложные&gt;'
title: '&lt;complex&gt;'
ms.date: 01/15/2021
f1_keywords:
- <complex>
- complex/std::literals::complex_literals
- std::literals::complex_literals
- complex_literals
- complex/std::literals::complex_literals::operator "i
- std::literals::complex_literals::operator i
- complex/std::literals::complex_literals::operator "if
- std::literals::complex_literals::operator if
- complex/std::literals::complex_literals::operator "i
- std::literals::complex_literals::operator i
helpviewer_keywords:
- complex header
ms.openlocfilehash: 4fb309d46ff6f7cba84dc8a4f0c7cf41fbf7d4d6
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98667380"
---
# `<complex>`

Определяет шаблон класса контейнера `complex` и его вспомогательные шаблоны.

## <a name="requirements"></a>Требования

**Заголовок**: \<complex>

**Пространство имен:** std

## <a name="remarks"></a>Примечания

*Комплексное число* — это упорядоченная пара вещественных чисел. В чисто двумернаяных терминах *сложная плоскость* — это реальная, двухмерная плоскость. Отличия комплексной плоскости от вещественной состоят в том, что у нее есть дополнительная алгебраическая структура. У этой структуры есть две основные операции.

- Сложение, определенное как (*a*, *б*) + (*c*, *d*) = (*a*  +  *c*, *b*  +  *d*)

- Умножение, определенное как (*a*, *б*) \* (*c*, *d*) = (*AC*  -  *BD*, *AD*  +  *BC*)

Набор комплексных чисел с операциями сложного сложения и комплексного умножения — это *поле* в стандартном алгебраическиеном смысле:

- Операции сложения и умножения коммутативны и ассоциативны, а умножение распределяется над сложением точно так же, как для вещественного сложения и умножения в поле вещественных чисел.

- Комплексное число (0, 0) представляет собой аддитивный идентификатор, а число (1, 0) — мультипликативный идентификатор.

- Аддитивный инверсия для комплексного числа (*a*, *b*) имеет значение (-*a*,-*b*) и мультипликативные обратно для всех таких комплексных чисел, кроме (0, 0)

   (*a*/(*a*<sup>2</sup>  +  *b*<sup>2</sup>), –*b*/(*a*<sup>2</sup>  +  *b*<sup>2</sup>))

Представляя комплексное число *z* = (*a*, *b*) в виде *z*  =  *a*  +  *BI*, где <sup>2</sup> =-1, правила для сквозной области набора реальных чисел можно применить к набору комплексных чисел и их компонентам. Пример:

   (1 + 2 *i*) \* (2 + 3 *i*) = 1 \* (2 + 3 *я*) + 2 *i* (2 + 3 я) \* = (2 + 3 *i)*+ (4-*я* + 6 *i*<sup>)</sup>= (2-6) + (3 + 4)*i* =-4 +7

Система комплексных чисел является полем, но не является упорядоченным полем. Порядок комплексных чисел не упорядочен, как и для поля реальных чисел и его подмножества, поэтому неравенство нельзя применить к комплексным числам, так как они являются реальными числами.

Существует три общие формы представления комплексного числа *z*:

- Декартка: *z*  =    +  *Бизнес-аналитика*

- Полярная: *z*  =  *r* (COS *p*  +  *i* Sin *p*)

- Экспонента :  =   \* <sup>*IP-адрес*</sup> z r e

В этих стандартных представлениях комплексных чисел используются следующие термины.

- Вещественный компонент арифметического представления или действительная часть *a*.

- Мнимый компонент арифметического представления или мнимая часть *b*.

- Модуль или абсолютное значение комплексного числа *r*.

- Аргумент или угол этапа *p* в радианах.

Если не указано иное, функции, которые могут вернуть несколько значений, должны возвращать значение участника для своих аргументов больше-π и меньше или равно + π, чтобы они оставались однозначными. Все углы должны быть выражены в радианах, где в окружности есть 2π радианы (360 градусов).

## <a name="members"></a>Члены

### <a name="functions"></a>Функции

| Имя | Описание |
|--|--|
| [`abs`](../standard-library/complex-functions.md#abs) | Вычисляет модуль комплексного числа. |
| [`acos`](../standard-library/complex-functions.md#acos) |  |
| [`acosh`](../standard-library/complex-functions.md#acosh) |  |
| [`arg`](../standard-library/complex-functions.md#arg) | Извлекает аргумент из комплексного числа. |
| [`asin`](../standard-library/complex-functions.md#asin) |  |
| [`asinh`](../standard-library/complex-functions.md#asinh) |  |
| [`atan`](../standard-library/complex-functions.md#atan) |  |
| [`atanh`](../standard-library/complex-functions.md#atanh) |  |
| [`conj`](../standard-library/complex-functions.md#conj) | Возвращает комплексно-сопряженную величину комплексного числа. |
| [`cos`](../standard-library/complex-functions.md#cos) | Возвращает косинус комплексного числа. |
| [`cosh`](../standard-library/complex-functions.md#cosh) | Возвращает гиперболический косинус комплексного числа. |
| [`exp`](../standard-library/complex-functions.md#exp) | Возвращает экспоненциальную функцию комплексного числа. |
| [`imag`](../standard-library/complex-functions.md#imag) | Извлекает мнимую часть комплексного числа. |
| [`log`](../standard-library/complex-functions.md#log) | Возвращает натуральный логарифм комплексного числа. |
| [`log10`](../standard-library/complex-functions.md#log10) | Возвращает десятичный логарифм комплексного числа. |
| [`norm`](../standard-library/complex-functions.md#norm) | Извлекает норму комплексного числа. |
| [`polar`](../standard-library/complex-functions.md#polar) | Возвращает комплексное число, соответствующее указанному модулю и аргументу, в декартовой форме. |
| [`pow`](../standard-library/complex-functions.md#pow) | Вычисляет комплексное число, получаемое в результате возведения основания (комплексное число) в степень другого комплексного числа. |
| [`proj`](../standard-library/complex-functions.md#proj) |  |
| [`real`](../standard-library/complex-functions.md#real) | Извлекает вещественную часть комплексного числа. |
| [`sin`](../standard-library/complex-functions.md#sin) | Возвращает синус комплексного числа. |
| [`sinh`](../standard-library/complex-functions.md#sinh) | Возвращает гиперболический синус комплексного числа. |
| [`sqrt`](../standard-library/complex-functions.md#sqrt) | Возвращает квадратный корень комплексного числа. |
| [`tan`](../standard-library/complex-functions.md#tan) | Возвращает тангенс комплексного числа. |
| [tanh](../standard-library/complex-functions.md#tanh) | Возвращает гиперболический тангенс комплексного числа. |

### <a name="operators"></a>Операторы

| Имя | Описание |
|--|--|
| [`operator!=`](../standard-library/complex-operators.md#op_neq) | Проверяет на неравенство два комплексных числа, по крайней мере одно из которых может принадлежать к подмножеству типа для вещественной и мнимой частей. |
| [`operator*`](../standard-library/complex-operators.md#op_star) | Умножает два комплексных числа, по крайней мере одно из которых может принадлежать к подмножеству типа для вещественной и мнимой частей. |
| [`operator+`](../standard-library/complex-operators.md#op_add) | Складывает два комплексных числа, по крайней мере одно из которых может принадлежать к подмножеству типа для вещественной и мнимой частей. |
| [`operator-`](../standard-library/complex-operators.md#operator-) | Вычитает два комплексных числа, по крайней мере одно из которых может принадлежать к подмножеству типа для вещественной и мнимой частей. |
| [`operator/`](../standard-library/complex-operators.md#op_div) | Делит два комплексных числа, по крайней мере одно из которых может принадлежать к подмножеству типа для вещественной и мнимой частей. |
| [`operator<<`](../standard-library/complex-operators.md#op_lt_lt) | Функция шаблона, вставляющая комплексное число в поток вывода. |
| [`operator==`](../standard-library/complex-operators.md#op_eq_eq) | Проверяет на равенство два комплексных числа, по крайней мере одно из которых может принадлежать к подмножеству типа для вещественной и мнимой частей. |
| [`operator>>`](../standard-library/complex-operators.md#op_gt_gt) | Функция шаблона, извлекающая комплексное число из входного потока. |

### <a name="classes"></a>Классы

| name | Описание |
|--|--|
| [`complex<double>`](../standard-library/complex-double.md) | В явном специализированном шаблоне класса описывается объект, хранящий упорядоченную пару объектов типа **`double`** , где первый представляет реальную часть комплексного числа, а вторая — мнимую часть. |
| [`complex<float>`](../standard-library/complex-float.md) | В явном специализированном шаблоне класса описывается объект, хранящий упорядоченную пару объектов типа **`float`** , где первый представляет реальную часть комплексного числа, а вторая — мнимую часть. |
| [`complex<long double>`](../standard-library/complex-long-double.md) | В явном специализированном шаблоне класса описывается объект, хранящий упорядоченную пару объектов типа **`long double`** , где первый представляет реальную часть комплексного числа, а вторая — мнимую часть. |
| [`complex`](../standard-library/complex-class.md) | Шаблон класса описывает объект, используемый для представления комплексной системы счисления и выполнения сложных арифметических операций. |

### <a name="literals"></a>Литералы

\<complex>Заголовок определяет следующие пользовательские [литералы](../cpp/user-defined-literals-cpp.md). Литералы создают комплексное число с реальной частью нуля и мнимой частью, которая имеет значение входного параметра.

| Объявление | Описание |
|--|--|
| `constexpr complex<long double> operator""il(long double d)`<br />`constexpr complex<long double> operator""il(unsigned long long d)` | Возвращаемый результат: `complex<long double>{0.0L, static_cast<long double>(d)}` |
| `constexpr complex<double> operator""i(long double d)`<br />`constexpr complex<double> operator""i(unsigned long long d)` | Возвращает `complex<double>{0.0, static_cast<double>(d)}`. |
| `constexpr complex<float> operator""if(long double d)`<br />`constexpr complex<float> operator""if(unsigned long long d)` | Возвращает `complex<float>{0.0f, static_cast<float>(d)}`. |

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
