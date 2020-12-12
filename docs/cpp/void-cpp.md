---
description: 'Дополнительные сведения: void (C++)'
title: void (C++)
ms.date: 11/04/2016
f1_keywords:
- void_cpp
helpviewer_keywords:
- void keyword [C++]
- functions [C++], void
- pointers, void
ms.assetid: d203edba-38e6-4056-8b89-011437351057
ms.openlocfilehash: e49dfa03e289cdbace50a24cf6854d25c51b3426
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97213355"
---
# <a name="void-c"></a>void (C++)

При использовании в качестве возвращаемого типа функции **`void`** ключевое слово указывает, что функция не возвращает значение. При использовании для списка параметров функции **`void`** указывает, что функция не принимает параметров. При использовании в объявлении указателя **`void`** указывает, что указатель является универсальным.

Если тип указателя — **void \* *_, указатель может указывать на любую переменную, которая не объявлена с* `const`** ключевым словом _ или **`volatile`** . Указатель на ** \* void* _ не может быть разыменован, если он не приведен к другому типу. Указатель _*void \**_ можно преобразовать в любой другой тип указателя данных.

Указатель _ *`void`* * может указывать на функцию, но не на член класса в C++.

Нельзя объявить переменную типа **`void`** .

## <a name="example"></a>Пример

```cpp
// void.cpp
void vobject;   // C2182
void *pv;   // okay
int *pint; int i;
int main() {
   pv = &i;
   // Cast optional in C required in C++
   pint = (int *)pv;
}
```

## <a name="see-also"></a>См. также раздел

[Ключевые слова](../cpp/keywords-cpp.md)<br/>
[Встроенные типы](../cpp/fundamental-types-cpp.md)
