---
description: 'Дополнительные сведения о: Ошибка компилятора C2584'
title: Ошибка компилятора C2584
ms.date: 11/04/2016
f1_keywords:
- C2584
helpviewer_keywords:
- C2584
ms.assetid: 836e2c0a-86c0-4742-b432-beb0191ad20e
ms.openlocfilehash: 7820019c3ec49928f59980adbd9ec814d67c3499
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97177683"
---
# <a name="compiler-error-c2584"></a>Ошибка компилятора C2584

"Класс": прямой базовый "Base2" недоступен; уже является основанием "баз данных"

`Class` уже является производным от `Base1` . `Base2` также является производным от `Base1` . `Class` не может быть производным от `Base2` , так как это означает наследование (косвенно) от `Base1` повторного, что не является допустимым, поскольку `Base1` уже является прямым базовым классом.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2584.

```cpp
// C2584.cpp
// compile with: /c
struct A1 {
   virtual int MyFunction();
};

struct A2 {
    virtual int MyFunction();
};

struct B1: public virtual A1, virtual A2 {
    virtual int MyFunction();
};

struct B2: public virtual A2, virtual A1 {
    virtual int MyFunction();
};

struct C: virtual B1, B2 {
    virtual int MyFunction();
};

struct Z : virtual B2, virtual C {   // C2584
// try the following line insted
// struct Z : virtual C {
    virtual int MyFunction();
};
```
