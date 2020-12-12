---
description: 'Дополнительные сведения о инструкции: NULL'
title: Оператор NULL
ms.date: 11/04/2016
helpviewer_keywords:
- expressions [C++], null
- null statement
- null values, expressions
ms.assetid: 606f5953-55f0-40c8-ae03-3ee3a819b851
ms.openlocfilehash: 1aa488da395cf84ae9ef6d78939f1f1e3019c572
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97146176"
---
# <a name="null-statement"></a>Оператор NULL

Оператор null является оператором выражения с отсутствующим *выражением* . Она полезна, если синтаксис языка требует инструкции, но не оценки выражения. Она состоит из точки с запятой.

Инструкции null часто используются как местозаполнители в инструкциях итерации или как инструкции, в которых нужно разместить метки в конце сложных инструкций или функций.

В следующем фрагменте кода показано, как копировать одну строку в другую. Кроме того, код содержит инструкцию null.

```cpp
// null_statement.cpp
char *myStrCpy( char *Dest, const char *Source )
{
    char *DestStart = Dest;

    // Assign value pointed to by Source to
    // Dest until the end-of-string 0 is
    // encountered.
    while( *Dest++ = *Source++ )
        ;   // Null statement.

    return DestStart;
}

int main()
{
}
```

## <a name="see-also"></a>См. также раздел

[Оператор выражения](../cpp/expression-statement.md)
