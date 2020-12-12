---
description: 'Дополнительные сведения о: Ошибка компилятора C3766'
title: Ошибка компилятора C3766
ms.date: 11/04/2016
f1_keywords:
- C3766
helpviewer_keywords:
- C3766
ms.assetid: b5af2089-2e1e-4e45-a41d-495b6c55656e
ms.openlocfilehash: f410b79cc0cd54f2702effb91e76f0e5e6908521
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97291757"
---
# <a name="compiler-error-c3766"></a>Ошибка компилятора C3766

"тип" должен предоставлять реализацию метода интерфейса "функция"

Класс, наследующий от интерфейса, должен реализовывать члены интерфейса.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3766.

```cpp
// C3766.cpp
// compile with: /clr /c

delegate void MyDel();

interface struct IFace {
   virtual event MyDel ^ E;
};

ref struct Class1 : public IFace {};   // C3766

// OK
ref struct Class2 : public IFace {
   virtual event MyDel ^ E {
      void add(MyDel ^) {}
      void remove(MyDel ^) {}
   }
};
```
