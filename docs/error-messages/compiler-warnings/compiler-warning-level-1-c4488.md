---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4488'
title: Предупреждение компилятора (уровень 1) C4488
ms.date: 11/04/2016
f1_keywords:
- C4488
helpviewer_keywords:
- C4488
ms.assetid: 55625e46-ddb5-4c7c-99c7-cd4aa9f879bd
ms.openlocfilehash: 60f72a76657e7661beb43441208dda3cddd26f48
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97310932"
---
# <a name="compiler-warning-level-1-c4488"></a>Предупреждение компилятора (уровень 1) C4488

"функция": требуется ключевое слово "keyword" для реализации метода интерфейса "interface_method"

Класс должен реализовывать все члены интерфейса, от которых он наследуется напрямую. Реализованный член должен иметь открытый доступ и должен быть помечен как Virtual.

## <a name="examples"></a>Примеры

C4488 может возникать, если реализованный член не является общедоступным. Следующий пример приводит к возникновению ошибки C4488.

```cpp
// C4488.cpp
// compile with: /clr /c /W1 /WX
interface struct MyI {
   void f1();
};

// implemented member not public
ref class B : MyI { virtual void f1() {} };  // C4488

// OK
ref class C : MyI {
public:
   virtual void f1() {}
};
```

C4488 может возникать, если реализованный член не помечен как Virtual. Следующий пример приводит к возникновению ошибки C4488.

```cpp
// C4488_b.cpp
// compile with: /clr /c /W1 /WX
interface struct MyI {
   void f1();
};

ref struct B : MyI { void f1() {} };   // C4488
ref struct C : MyI { virtual void f1() {} };   // OK
```
