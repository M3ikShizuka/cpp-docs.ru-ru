---
description: 'Дополнительные сведения о: Ошибка компилятора C2274'
title: Ошибка компилятора C2274
ms.date: 11/04/2016
f1_keywords:
- C2274
helpviewer_keywords:
- C2274
ms.assetid: 8e874903-f499-45ef-8291-f821eee4cc1c
ms.openlocfilehash: 31b9d63b9cf87114ce2d1d79f1f38fff97d4ebbb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97268357"
---
# <a name="compiler-error-c2274"></a>Ошибка компилятора C2274

"тип": недопустимо в качестве правой стороны оператора "."

Тип отображается как правый операнд оператора доступа к члену (.).

Эта ошибка может быть вызвана попыткой доступа к преобразованию определяемого пользователем типа. Используйте ключевое слово **`operator`** между точкой и `type` .

При компиляции следующего примера возникнет ошибка C2286:

```cpp
// C2274.cpp
struct MyClass {
   operator int() {
      return 0;
   }
};

int main() {
   MyClass ClassName;
   int i = ClassName.int();   // C2274
   int j = ClassName.operator int();   // OK
}
```
