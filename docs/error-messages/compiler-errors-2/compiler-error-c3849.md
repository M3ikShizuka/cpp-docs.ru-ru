---
description: 'Дополнительные сведения о: Ошибка компилятора C3849'
title: Ошибка компилятора C3849
ms.date: 11/04/2016
f1_keywords:
- C3849
helpviewer_keywords:
- C3849
ms.assetid: 5347140e-1a81-4841-98c0-b63d98264b64
ms.openlocfilehash: 6dbe4656eea2691c1c77c1afa389be80ab76af18
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97255357"
---
# <a name="compiler-error-c3849"></a>Ошибка компилятора C3849

вызов в стиле функции в выражении типа "тип" приведет к потере квалификаторов const и/или volatile для всех доступных перегрузок операторов

Переменная с указанным типом const константы может вызывать только функции-члены, определенные с теми же или большими квалификациями const-volatile.

Чтобы устранить эту ошибку, укажите соответствующую функцию члена. Невозможно выполнить преобразование для объекта с квалификатором const или volatile, если преобразование приводит к утрате квалификации. Можно получить квалификаторы, но нельзя потерять квалификаторы при преобразовании.

Следующие примеры создают C3849:

```cpp
// C3849.cpp
void glbFunc3(int i, char c)
{
   i;
}
typedef void (* pFunc3)(int, char);

void glbFunc2(int i)
{
   i;
}

typedef void (* pFunc2)(int);

void glbFunc1()
{
}
typedef void (* pFunc1)();

struct S4
{
   operator ()(int i)
   {
      i;
   }

   operator pFunc1() const
   {
      return &glbFunc1;
   }

   operator pFunc2() volatile
   {
      return &glbFunc2;
   }

   operator pFunc3()
   {
      return &glbFunc3;
   }

   // operator pFunc1() const volatile
   // {
   //    return &glbFunc1;
   // }
};

int main()
{
   // Cannot call any of the 4 overloads of "operator ()(.....)" and
   // "operator pFunc()" because none is declared as "const volatile"
   const volatile S4 s4;  // can only call cv member functions of S4
   s4();   // C3849 to resolve, uncomment member function
}
```
