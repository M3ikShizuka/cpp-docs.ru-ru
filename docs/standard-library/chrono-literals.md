---
description: Дополнительные сведения о `chrono` литералах
title: литералы chrono
f1_keywords:
- chrono/std::literals::chrono_literals
- std::literals::chrono_literals
- chrono_literals
ms.date: 01/15/2021
ms.openlocfilehash: 84540d111b33738c8bb1bcb4b43966e1c50682c0
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98667548"
---
# <a name="chrono-literals"></a>`chrono` литералы

(C++ 14) `<chrono>` Заголовок определяет 12 [определяемых пользователем литералов](../cpp/user-defined-literals-cpp.md) , представляющих часы, минуты, секунды, миллисекунды, микросекунды и наносекундах. Каждый определяемый пользователем литерал имеет целочисленное значение и значение перегрузки с плавающей запятой. Литералы определяются во `literals::chrono_literals` встроенном пространстве имен, которое автоматически добавляется в область, если `std::chrono` находится в области.

## <a name="syntax"></a>Синтаксис

```cpp
inline namespace literals {
  inline namespace chrono_literals {
    // return integral hours
    constexpr chrono::hours operator"" h(unsigned long long Val);

    // return floating-point hours
    constexpr chrono::duration<double, ratio<3600>> operator"" h(long double Val);

    // return integral minutes
    constexpr chrono::minutes(operator"" min)(unsigned long long Val);

    // return floating-point minutes
    constexpr chrono::duration<double, ratio<60>>(operator"" min)(long double Val);

    // return integral seconds
    constexpr chrono::seconds operator"" s(unsigned long long Val);

    // return floating-point seconds
    constexpr chrono::duration<double> operator"" s(long double Val);

    // return integral milliseconds
    constexpr chrono::milliseconds operator"" ms(unsigned long long Val);

    // return floating-point milliseconds
    constexpr chrono::duration<double, milli> operator"" ms(long double Val);

    // return integral microseconds
    constexpr chrono::microseconds operator"" us(unsigned long long Val);

    // return floating-point microseconds
    inline constexpr chrono::duration<double, micro> operator"" us(long double Val);

    // return integral nanoseconds
    inline constexpr chrono::nanoseconds operator"" ns(unsigned long long Val);

    // return floating-point nanoseconds
    constexpr chrono::duration<double, nano> operator"" ns(long double Val);

  } // inline namespace chrono_literals
} // inline namespace literals
```

## <a name="return-value"></a>Возвращаемое значение

Литералы, которые принимают **`long long`** аргумент, возвращают значение или соответствующий тип. Литералы, которые принимают аргумент с плавающей запятой, возвращают [`duration`](../standard-library/duration-class.md) .

## <a name="example"></a>Пример

В следующих примерах показано, как использовать `chrono` литералы.

```cpp
constexpr auto day = 24h;
constexpr auto week = 24h* 7;
constexpr auto my_duration_unit = 108ms;
```
