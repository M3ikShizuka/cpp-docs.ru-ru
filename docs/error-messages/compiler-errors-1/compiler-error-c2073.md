---
description: 'Дополнительные сведения о: Ошибка компилятора C2073'
title: Ошибка компилятора C2073
ms.date: 11/04/2016
f1_keywords:
- C2073
helpviewer_keywords:
- C2073
ms.assetid: 57908234-be7a-4ce9-b0a7-8b1ad621865e
ms.openlocfilehash: 791f07040b0a0dd70d2cb0aa8373eb6c342c5b97
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209169"
---
# <a name="compiler-error-c2073"></a>Ошибка компилятора C2073

"идентификатор": элементы частично инициализированного массива должны иметь конструктор по умолчанию

Для массива определяемых пользователем типов или констант указано слишком мало инициализаторов. Если явный инициализатор и соответствующий ему конструктор не указаны для члена массива, необходимо предоставить конструктор по умолчанию.

Следующий пример приводит к возникновению ошибки C2073:

```cpp
// C2073.cpp
class A {
public:
   A( int );   // constructor for ints only
};
A a[3] = { A(1), A(2) };   // C2073, no default constructor
```

```cpp
// C2073b.cpp
// compile with: /c
class B {
public:
   B();   // default constructor declared
   B( int );
};
B b[3] = { B(1), B(2) };   // OK
```
