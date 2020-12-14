---
description: 'Дополнительные сведения о: Ошибка компилятора C3638'
title: Ошибка компилятора C3638
ms.date: 11/04/2016
f1_keywords:
- C3638
helpviewer_keywords:
- C3638
ms.assetid: 8d8bc5ca-75aa-480e-b6b6-3178fab51b1d
ms.openlocfilehash: 1d1cc59cd8065a5b0e661292b717ba885c6febeb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97239198"
---
# <a name="compiler-error-c3638"></a>Ошибка компилятора C3638

"оператор": стандартные операторы преобразования упаковки и распаковки не могут быть переопределены

Компилятор определяет оператор преобразования для каждого управляемого класса, поддерживающего неявную упаковку-преобразование. Этот оператор нельзя переопределить.

Дополнительные сведения см. в разделе [неявная упаковка](../../extensions/boxing-cpp-component-extensions.md).

Следующий пример приводит к возникновению ошибки C3638:

```cpp
// C3638.cpp
// compile with: /clr
value struct V {
   V(){}
   static operator V^(V);   // C3638
};

int main() {
   V myV;
   V ^ pmyV = myV;   // operator supports implicit boxing
}
```
