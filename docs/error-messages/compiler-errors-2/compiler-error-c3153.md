---
description: 'Дополнительные сведения о: Ошибка компилятора C3153'
title: Ошибка компилятора C3153
ms.date: 11/04/2016
f1_keywords:
- C3153
helpviewer_keywords:
- C3153
ms.assetid: d775d97e-2480-484f-81f1-88406b10f947
ms.openlocfilehash: 93b028e08963a8d124defe660966a75595c57771
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97322050"
---
# <a name="compiler-error-c3153"></a>Ошибка компилятора C3153

"интерфейс": невозможно создать экземпляр интерфейса

Невозможно создать экземпляр интерфейса. Чтобы использовать члены интерфейса, создайте класс из интерфейса, реализуйте члены интерфейса, а затем используйте элементы.

Следующий пример приводит к возникновению ошибки C3153:

```cpp
// C3153.cpp
// compile with: /clr
interface class A {
};

int main() {
   A^ a = gcnew A;   // C3153
}
```
