---
description: 'Дополнительные сведения о: Ошибка компилятора C3154'
title: Ошибка компилятора C3154
ms.date: 11/04/2016
f1_keywords:
- C3154
helpviewer_keywords:
- C3154
ms.assetid: 78005c74-eaaf-4ac2-88ae-6c25d01a302a
ms.openlocfilehash: c43800aba54431041b13e70d9e94c80d98d8ee84
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97203982"
---
# <a name="compiler-error-c3154"></a>Ошибка компилятора C3154

Перед многоточием ожидалось ",". В функциях массива параметров не поддерживается многоточие, не разделенное запятыми.

Функция аргумента переменной не была объявлена правильно.

Дополнительные сведения см. в разделе [списки аргументов переменных (...) (C++/CLI)](../../extensions/variable-argument-lists-dot-dot-dot-cpp-cli.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3154.

```cpp
// C3154.cpp
// compile with: /clr
ref struct R {
   void Func(int ... array<int> ^);   // C3154
   void Func2(int i, ... array<int> ^){}   // OK
   void Func3(array<int> ^){}   // OK
   void Func4(... array<int> ^){}   // OK
};

int main() {
   R ^ r = gcnew R;
   r->Func4(1,2,3);
}
```
