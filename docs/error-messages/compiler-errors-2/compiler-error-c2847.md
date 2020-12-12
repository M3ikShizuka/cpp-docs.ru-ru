---
description: 'Дополнительные сведения о: Ошибка компилятора C2847'
title: Ошибка компилятора C2847
ms.date: 11/04/2016
f1_keywords:
- C2847
helpviewer_keywords:
- C2847
ms.assetid: 9ad9a0e0-8b16-49d9-a5be-f8eda2372aa9
ms.openlocfilehash: fc9b7a75d662778bc532bb35e4520fb5627c9f2a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97260219"
---
# <a name="compiler-error-c2847"></a>Ошибка компилятора C2847

невозможно применить sizeof к управляемому типу или типу WinRT type "class"

Оператор [sizeof](../../cpp/sizeof-operator.md) получает значение объекта во время компиляции. Размер управляемого класса или класса WinRT, интерфейса или типа значения является динамическим, поэтому он не может быть известен во время компиляции.

Так, следующий пример приводит к возникновению ошибки C2847:

```cpp
// C2847.cpp
// compile with: /clr
ref class A {};

int main() {
   A ^ xA = gcnew A;
   sizeof(*xA);   // C2847 cannot use sizeof on managed object
}
```
