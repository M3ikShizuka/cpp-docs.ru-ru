---
description: 'Дополнительные сведения о: Ошибка компилятора C3190'
title: Ошибка компилятора C3190
ms.date: 11/04/2016
f1_keywords:
- C3190
helpviewer_keywords:
- C3190
ms.assetid: 7c701afa-85a7-4f7a-8881-0662436ac244
ms.openlocfilehash: 2a0ed65d67f4847dbe5140561fb2629c19f85c8f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97322014"
---
# <a name="compiler-error-c3190"></a>Ошибка компилятора C3190

"Создание экземпляра" с предоставленными аргументами шаблона не является явным созданием экземпляра какой-либо функции-члена типа "тип"

Компилятор обнаружил попытку сделать явное создание экземпляра функции; Однако указанные аргументы типа не соответствуют ни одной из возможных функций.

Следующий пример приводит к возникновению ошибки C3190:

```cpp
// C3190.cpp
// compile with: /LD
template<class T>
struct A {
   A(int x = 0) {
   }
   A(int x, int y) {
   }
};

template A<float>::A();   // C3190
// try the following line instead
// template A<int>::A(int);

struct Y {
   template<class T> void f(T);
};

template<class T> void Y::f(T) { }

template void Y::f(int,int);   // C3190

template<class OT> class X {
   template<class T> void f2(T,OT);
};

template<class OT> template<class T> void X<OT>::f2(T,OT) {}

template void X<float>::f2<int>(int,char);   // C3190
// try one of the following lines instead
// template void X<char>::f2(int, char);
// template void X<char>::f2<int>(int,char);
// template void X<char>::f2<>(int,char);
```
