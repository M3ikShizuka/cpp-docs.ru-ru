---
description: 'Дополнительные сведения о: Ошибка компилятора C3895'
title: Ошибка компилятора C3895
ms.date: 11/04/2016
f1_keywords:
- C3895
helpviewer_keywords:
- C3895
ms.assetid: 771b9fe5-d6d4-4297-bf57-e2f857722155
ms.openlocfilehash: ae963eb89ee8f0cefc9092e9d3b16aa40885e63c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97315118"
---
# <a name="compiler-error-c3895"></a>Ошибка компилятора C3895

"var": элементы данных типа не могут быть "volatile"

Некоторые типы элементов данных, например [Literal](../../extensions/literal-cpp-component-extensions.md) или [initonly](../../dotnet/initonly-cpp-cli.md), не могут быть [временными](../../cpp/volatile-cpp.md).

Следующий пример приводит к возникновению ошибки C3895:

```cpp
// C3895.cpp
// compile with: /clr
ref struct Y1 {
   initonly
   volatile int data_var2;   // C3895
};
```
