---
description: 'Дополнительные сведения о: Ошибка компилятора C2228'
title: Ошибка компилятора C2228
ms.date: 11/04/2016
f1_keywords:
- C2228
helpviewer_keywords:
- C2228
ms.assetid: 901cadb1-ce90-4ae0-a360-547a9ba2ca18
ms.openlocfilehash: 8bf5c4af88f77237699baae5e7a458fca971f126
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97195064"
---
# <a name="compiler-error-c2228"></a>Ошибка компилятора C2228

слева от ".identifier" должен быть указан класс, структура или объединение

Операнд слева от точки (.) не является классом, структурой или объединением.

Следующий пример приводит к возникновению ошибки C2228:

```cpp
// C2228.cpp
int i;
struct S {
public:
    int member;
} s, *ps = &s;

int main() {
   i.member = 0;   // C2228 i is not a class type
   ps.member = 0;  // C2228 ps is a pointer to a structure

   s.member = 0;   // s is a structure type
   ps->member = 0; // ps points to a structure S
}
```

Эта ошибка также возникает из-за неправильного синтаксиса при использовании управляемых расширений. В то время как в других языках Visual Studio для доступа к члену управляемого класса можно использовать оператор "точка", в C++ указатель на объект означает, что для доступа к члену вы должны использовать оператор ->:

Неправильно: `String * myString = checkedListBox1->CheckedItems->Item[0].ToString();`

Правильно: `String * myString = checkedListBox1->CheckedItems->Item[0]->ToString();`
