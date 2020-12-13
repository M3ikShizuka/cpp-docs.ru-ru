---
description: 'Дополнительные сведения о: Ошибка компилятора C2868'
title: Ошибка компилятора C2868
ms.date: 11/04/2016
f1_keywords:
- C2868
helpviewer_keywords:
- C2868
ms.assetid: 6ff5837b-e66d-44d1-9d17-80af35e08d08
ms.openlocfilehash: c6a6368fbdfe61014a606fadce92322234e438f1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333795"
---
# <a name="compiler-error-c2868"></a>Ошибка компилятора C2868

> "*идентификатор*": недопустимый синтаксис для объявления using; Ожидаемое полное имя

Для [объявления с использованием](../../cpp/using-declaration.md) требуется *полное имя*, оператор области действия ( `::` ), разделенный на имена пространств имен, классов или перечислений, которые заканчиваются именем идентификатора. Чтобы ввести имя из глобального пространства имен, можно использовать один оператор разрешения области.

## <a name="example"></a>Пример

В следующем примере показано создание C2868, а также правильное использование:

```cpp
// C2868.cpp
class X {
public:
   int i;
};

class Y : X {
public:
   using X::i;   // OK
};

int main() {
   using X;   // C2868
}
```
