---
description: 'Дополнительные сведения о: Ошибка компилятора C3210'
title: Ошибка компилятора C3210
ms.date: 11/04/2016
f1_keywords:
- C3210
helpviewer_keywords:
- C3210
ms.assetid: c6e9d309-fabc-4e7d-b526-be20d9fe3f6a
ms.openlocfilehash: 5349a7ea8677a8a55511f514e74251375a262fb7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97173913"
---
# <a name="compiler-error-c3210"></a>Ошибка компилятора C3210

"тип": объявление доступа может применяться только к члену базового класса

[Объявление using](../../cpp/using-declaration.md) указано неверно.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3210.

```cpp
// C3210.cpp
// compile with: /c
struct A {
protected:
   int i;
};

struct B {
   using A::i;   // C3210
};

struct C : public A {
   using A::i;   // OK
};
```
