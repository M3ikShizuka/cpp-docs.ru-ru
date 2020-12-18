---
title: Выбор с использованием _Generic (C11)
description: Описание ключевого слова C11 _Generic, используемого в компиляторе Microsoft Visual C
ms.date: 12/9/2020
helpviewer_keywords:
- _Generic keyword [C]
ms.openlocfilehash: de0e840c19186219d53800b9d008d7695b807bc1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97348898"
---
# <a name="generic-selection-c11"></a>Выбор с использованием _Generic (C11)

Ключевое слово **`_Generic`** используется для написания кода, который выбирает выражение во время компиляции в зависимости от типа аргумента. Это поведение аналогично перегрузке в C++, когда тип аргумента выбирает функцию для вызова, за исключением того, что тип аргумента выбирает выражение для вычисления.

Например, выражение `_Generic(42, int: "integer", char: "character", default: "unknown");` оценивает тип `42` и ищет соответствующий тип `int` в списке. При обнаружении типа возвращается `"integer"`.

## <a name="syntax"></a>Синтаксис

*`generic-selection`*:\
&nbsp;&nbsp;&nbsp;&nbsp;**`_Generic`** **(** *`assignment-expression`, `assoc-list`* **)**

*`assoc-list`*:\
&nbsp;&nbsp;&nbsp;&nbsp;*`association`*\
&nbsp;&nbsp;&nbsp;&nbsp;*`assoc-list`, `association`*

*`association`*:\
&nbsp;&nbsp;&nbsp;&nbsp;*`type-name`* : *`assignment-expression`*\
&nbsp;&nbsp;&nbsp;&nbsp;**`default`** : *`assignment-expression`*

Первое выражение *`assignment-expression`* называется управляющим. Тип управляющего выражения определяется во время компиляции и сопоставляется с *`assoc-list`* , чтобы найти выражение для вычисления и возврата. Значение управляющего выражения не вычисляется. Например, при наличии `_Generic(intFunc(), int: "integer", default: "error");` `intFunc()` не вызывается во время выполнения. 

Когда определяется тип управляющего выражения, `const`, `volatile` и `restrict` удаляются перед сопоставлением с *`assoc-list`* .

Записи в `assoc-list`, которые не были выбраны, не вычисляются.

## <a name="constraints"></a>Ограничения

- *`assoc-list`* не может указывать один и тот же тип более одного раза.
- *`assoc-list`* не может указывать типы, совместимые друг с другом, например перечисление и базовый тип этого перечисления.
- Если при выборе _Generic нет значения по умолчанию, управляющее выражение должно иметь только одно совместимое имя типа в списке универсальных связей.

## <a name="example"></a>Пример

Как один из вариантов, **`_Generic`** можно использовать в макросе. Файл заголовка <tgmath.h> использует **_Generic** для вызова правильной математической функции в зависимости от типа аргумента. Например, макрос для `cos()` сопоставляет вызов, содержащий число с плавающей точкой, с `cosf()`, одновременно сопоставляя вызов, содержащий сложное число двойной точности, с `ccos()`.

В приведенном ниже примере показано, как написать макрос, который определяет тип переданного в него аргумента. Если в *`assoc-list`* нет записей, совпадающих с управляющим выражением, создается `"unknown"`:

```C
// Compile with /std:c11

#include <stdio.h>

/* Get a type name string for the argument x */
#define TYPE_NAME(X) _Generic((X), \
      int: "int", \
      char: "char", \
      double: "double", \
      default: "unknown")

int main()
{
    printf("Type name: %s\n", TYPE_NAME(42.42));

    // The following would result in a compile error because 
    // 42.4 is a double, doesn't match anything in the list, 
    // and there is no default.
    // _Generic(42.4, int: "integer", char: "character"));
}

/* Output:
Type name: double
*/

```

## <a name="see-also"></a>См. также раздел

[`/std` (определение стандартной версии языка)](../build/reference/std-specify-language-standard-version.md)\
[Математические символы универсального типа](../c-runtime-library/tgmath.md)