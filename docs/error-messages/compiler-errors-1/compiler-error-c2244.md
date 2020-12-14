---
description: 'Дополнительные сведения о: Ошибка компилятора C2244'
title: Ошибка компилятора C2244
ms.date: 11/04/2016
f1_keywords:
- C2244
helpviewer_keywords:
- C2244
ms.assetid: d9911c12-ceb5-4f93-ac47-b44a485215c2
ms.openlocfilehash: 9f541eca155b9d728f0bbf7cb1578a6e3424c49c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97302247"
---
# <a name="compiler-error-c2244"></a>Ошибка компилятора C2244

"идентификатор": не удается сопоставить определение функции с существующим объявлением

Необычное использование унарного оператора + было использовано перед вызовом функции, не имеющим круглых скобок.

Эта ошибка возникает только в проектах C++.

Следующий пример приводит к возникновению ошибки C2244:

```cpp
// C2244.cpp
int func(char) {
   return 0;
}

int func(int) {
   return 0;
}

int main() {
   +func;   // C2244
}
```

C2244 также может возникать, если для функции-члена шаблона класса используется неправильная сигнатура функции.

```cpp
// C2244b.cpp
// compile with: /c
template<class T>
class XYZ {
   void func(T t);
};

template<class T>
void XYZ<T>::func(int i) {}   // C2244 wrong function signature
// try the following line instead
// void XYZ<T>::func(T t) {}
```

C2244 также может возникать, если для шаблона функции-члена используется неправильная сигнатура функции.

```cpp
// C2244c.cpp
// compile with: /c
class ABC {
   template<class T>
   void func(int i, T t);
};

template<class T>
void ABC::func(int i) {}   // C2244 wrong signature
// try the following line instead
// void ABC::func(int i, T t) {}
```

Нельзя частично специализацию шаблона функции.

```cpp
// C2244d.cpp
template<class T, class U>
class QRS {
   void func(T t, U u);
};

template<class T>
void QRS<T,int>::func(T t, int u) {}   // C2244
```
