---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4481'
title: Предупреждение компилятора (уровень 1) C4481
ms.date: 11/04/2016
f1_keywords:
- C4481
helpviewer_keywords:
- C4481
ms.assetid: 7bfd4e0c-b452-4e6c-b7c4-ac5cc93fe4ea
ms.openlocfilehash: 463df18090a4f6f632a80543576db4cb9048e754
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97251301"
---
# <a name="compiler-warning-level-4-c4481"></a>Предупреждение компилятора (уровень 1) C4481

использовано нестандартное расширение: спецификатор переопределения "ключевое слово"

Было использовано ключевое слово, которое не входит в стандарт C++, например один из описателей переопределения, которые также работают в/CLR.  Дополнительные сведения см. в следующих разделах:

- [/clr (компиляция среды выполнения)](../../build/reference/clr-common-language-runtime-compilation.md)

- [Спецификаторы переопределения](../../extensions/override-specifiers-cpp-component-extensions.md)

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4481.

```cpp
// C4481.cpp
// compile with: /W4 /c
class B {
   virtual void f(unsigned);
};

class C : B {
   void f(unsigned) override;   // C4481
   void f2(unsigned);
};
```
