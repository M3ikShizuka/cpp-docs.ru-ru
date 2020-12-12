---
description: 'Дополнительные сведения о: ctype_base классе'
title: Класс ctype_base
ms.date: 11/04/2016
f1_keywords:
- locale/std::ctype_base
helpviewer_keywords:
- ctype_base class
ms.assetid: ccffe891-d7ab-4d22-baf8-8eb6d438a96d
ms.openlocfilehash: 430e6fbf77842e61e662fd3024a54b418f487748
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324686"
---
# <a name="ctype_base-class"></a>Класс ctype_base

Класс выступает в качестве базового класса для аспектов шаблона класса [CType](../standard-library/ctype-class.md). Базовый класс для класса ctype, используемый для определения типов перечисления, применяемых для классификации или тестирования символов по отдельности или целыми диапазонами.

## <a name="syntax"></a>Синтаксис

```cpp
struct ctype_base : public locale::facet
{
    enum
    {
        alnum,
        alpha,
        cntrl,
        digit,
        graph,
        lower,
        print,
        punct,
        space,
        upper,
        xdigit
    };
    typedef short mask;

    ctype_base( size_t _Refs = 0 );
    ~ctype_base();
};
```

## <a name="remarks"></a>Remarks

Задает маску перечисления. Каждая константа перечисления характеризует другой способ классификации символов, как определено функциями с похожими именами, объявленными в заголовке \<ctype.h> . Используются следующие константы:

- **space** (функция [isspace](../standard-library/locale-functions.md#isspace))

- **print** (функция [isprint](../standard-library/locale-functions.md#isprint))

- **cntrl** (функция [iscntrl](../standard-library/locale-functions.md#iscntrl))

- **upper** (функция [isupper](../standard-library/locale-functions.md#isupper))

- **lower** (функция [islower](../standard-library/locale-functions.md#islower))

- **digit** (функция [isdigit](../standard-library/locale-functions.md#isdigit))

- **punct** (функция [ispunct](../standard-library/locale-functions.md#ispunct))

- **xdigit** (функция [isxdigit](../standard-library/locale-functions.md#isxdigit))

- **alpha** (функция [isalpha](../standard-library/locale-functions.md#isalpha))

- **alnum** (функция [isalnum](../standard-library/locale-functions.md#isalnum))

- **graph** (функция [isgraph](../standard-library/locale-functions.md#isgraph))

Вы можете охарактеризовать комбинацию классификаций, выполняя операцию OR с этими константами. В частности, всегда верно, что **алнум** = = ( **альфа** &#124; **digit** \) и **Graph** \= \= \( **алнум** &#124; **punct**).

## <a name="requirements"></a>Требования

**Заголовок:**\<locale>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
