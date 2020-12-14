---
description: 'Дополнительные сведения о: Ошибка компилятора C2581'
title: Ошибка компилятора C2581
ms.date: 11/04/2016
f1_keywords:
- C2581
helpviewer_keywords:
- C2581
ms.assetid: 24a4e4c1-24d3-4e42-b760-7dcaf9740b16
ms.openlocfilehash: 9de6c48c2ade71af238cc62a0f92e642e1262d3b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97282124"
---
# <a name="compiler-error-c2581"></a>Ошибка компилятора C2581

"тип": статическая функция "operator =" недопустима

Оператор присваивания ( `=` ) неверно объявлен как **`static`** . Операторы присваивания не могут иметь значение **`static`** . Дополнительные сведения см. в разделе [определяемые пользователем операторы (C++/CLI)](../../dotnet/user-defined-operators-cpp-cli.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2581.

```cpp
// C2581.cpp
// compile with: /clr /c
ref struct Y {
   static Y ^ operator = (Y^ me, int i);   // C2581
   Y^ operator =(int i);   // OK
};
```
