---
description: 'Дополнительные сведения о: Ошибка компилятора C3299'
title: Ошибка компилятора C3299
ms.date: 11/04/2016
f1_keywords:
- C3299
helpviewer_keywords:
- C3299
ms.assetid: 7cabdf01-bceb-404f-9401-cdd9c7fc1641
ms.openlocfilehash: ab86a675eb13b975943130802ae98679dbc1cbb3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337404"
---
# <a name="compiler-error-c3299"></a>Ошибка компилятора C3299

"функция-член": невозможно указать ограничения, они унаследованы из базового метода

При переопределении универсальной функции-члена нельзя указать предложения ограничений (при повторении ограничений подразумевается, что они не наследуются).

В этом случае наследуются предложения ограничений, содержащиеся в переопределяемой универсальной функции.

Дополнительные сведения см. в статье [Constraints on Generic Type Parameters (C++/CLI)](../../extensions/constraints-on-generic-type-parameters-cpp-cli.md) (Ограничения, применяемые к параметрам универсальных типов (C++/CLI)).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3299.

```cpp
// C3299.cpp
// compile with: /clr /c
public ref struct R {
   generic<class T>
   where T : R
   virtual void f();
};

public ref struct S : R {
   generic<class T>
   where T : R   // C3299
   virtual void f() override;
};
```
