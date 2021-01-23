---
description: Дополнительные сведения о pragma директиве Function в Microsoft C/C++
title: функций pragma
ms.date: 01/22/2021
f1_keywords:
- function_CPP
- vc-pragma.function
helpviewer_keywords:
- function pragma
- pragma, function
no-loc:
- pragma
ms.openlocfilehash: 3d4b1e2f50cd118e613235271428588ac585affc
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98712834"
---
# <a name="function-no-locpragma"></a>`function` pragma

Указывает компилятору создавать вызовы функций, указанных в pragma списке аргументов, вместо их встраивания.

## <a name="syntax"></a>Синтаксис

> **`#pragma function(`***функция1* [ **`,`** *функция2* ...]**`)`**

## <a name="remarks"></a>Примечания

Встроенные функции обычно создаются как встроенный код, а не как вызовы функций. При использовании [ `intrinsic` pragma](intrinsic.md) параметра или компилятора, [`/Oi`](../build/reference/oi-generate-intrinsic-functions.md) чтобы сообщить компилятору о необходимости создания встроенных функций, можно использовать **`function`** pragma для явного принудительного вызова функции. После того как объект **`function`** pragma виден, он вступает в силу в первом определении функции, который содержит указанную подставляемую функцию. Действие переходит к концу исходного файла или к внешнему виду, в `intrinsic` pragma котором указана та же встроенная функция. Можно использовать только **`function`** pragma внешний уровень функции на глобальном уровне.

Список функций, имеющих встроенные формы, см. в [ `intrinsic` pragma ](intrinsic.md)разделе.

## <a name="example"></a>Пример

```cpp
// pragma_directive_function.cpp
#include <ctype.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// use intrinsic forms of memset and strlen
#pragma intrinsic(memset, strlen)

// Find first word break in string, and set remaining
// chars in string to specified char value.
char *set_str_after_word(char *string, char ch) {
   int i;
   int len = strlen(string);  /* NOTE: uses intrinsic for strlen */

   for(i = 0; i < len; i++) {
      if (isspace(*(string + i)))
         break;
   }

   for(; i < len; i++)
      *(string + i) = ch;

   return string;
}

// do not use strlen intrinsic
#pragma function(strlen)

// Set all chars in string to specified char value.
char *set_str(char *string, char ch) {
   // Uses intrinsic for memset, but calls strlen library function
   return (char *) memset(string, ch, strlen(string));
}

int main() {
   char *str = (char *) malloc(20 * sizeof(char));

   strcpy_s(str, sizeof("Now is the time"), "Now is the time");
   printf("str is '%s'\n", set_str_after_word(str, '*'));
   printf("str is '%s'\n", set_str(str, '!'));
}
```

```Output
str is 'Now************'
str is '!!!!!!!!!!!!!!!'
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
