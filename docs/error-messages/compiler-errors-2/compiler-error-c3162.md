---
description: 'Дополнительные сведения о: Ошибка компилятора C3162'
title: Ошибка компилятора C3162
ms.date: 11/04/2016
f1_keywords:
- C3162
helpviewer_keywords:
- C3162
ms.assetid: 0d4c4a24-1456-4191-b7d8-c38cb7b17c32
ms.openlocfilehash: ca44b27607a34a469a5fd6fc1371e1510452247a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97242318"
---
# <a name="compiler-error-c3162"></a>Ошибка компилятора C3162

"тип": ссылочный тип с деструктором не может использоваться в качестве типа статических данных-члена "член"

Среда CLR не может определить, когда следует запускать пользовательский деструктор, если класс также содержит статическую функцию-член.

Деструктор никогда не будет выполняться, если только объект не будет удален явным образом.

Дополнительные сведения см. в следующих разделах:

- [/clr (компиляция среды выполнения)](../../build/reference/clr-common-language-runtime-compilation.md)

- [Общие вопросы использования Visual C++ для 64-разрядных систем](../../build/common-visual-cpp-64-bit-migration-issues.md)

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3162.

```cpp
// C3162.cpp
// compile with: /clr /c
ref struct A {
   ~A() { System::Console::WriteLine("in destructor"); }
   static A i;   // C3162
   static A^ a = gcnew A;   // OK
};

int main() {
   A ^ a = gcnew A;
   delete a;
}
```
