---
description: 'Дополнительные сведения о: Ошибка компилятора C3394'
title: Ошибка компилятора C3394
ms.date: 11/04/2016
f1_keywords:
- C3394
helpviewer_keywords:
- C3394
ms.assetid: 4e025d79-27ba-43c8-b0d9-839ecef98126
ms.openlocfilehash: ea805ef8ff9bf6e19498135ae6fcd9ba7e3ff9e6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97313363"
---
# <a name="compiler-error-c3394"></a>Ошибка компилятора C3394

синтаксическая ошибка в предложении ограничения: для найденного "идентификатор" требуется тип

Ограничение было неправильно сформировано.  Дополнительные сведения см. в статье [Constraints on Generic Type Parameters (C++/CLI)](../../extensions/constraints-on-generic-type-parameters-cpp-cli.md) (Ограничения, применяемые к параметрам универсальных типов (C++/CLI)).

## <a name="example"></a>Пример

В следующем примере возникает ошибка C3394:

```cpp
// C3394.cpp
// compile with: /clr /c
ref class MyClass {};
ref class R {
   generic<typename T>
   where T : static   // C3394
   // try the following line instead
   // where T : MyClass
   void f() {}
};
```
