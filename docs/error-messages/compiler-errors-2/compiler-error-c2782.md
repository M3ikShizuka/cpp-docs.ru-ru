---
description: 'Дополнительные сведения о: Ошибка компилятора C2782'
title: Ошибка компилятора C2782
ms.date: 11/04/2016
f1_keywords:
- C2782
helpviewer_keywords:
- C2782
ms.assetid: 8b685422-294d-4f64-9f3d-c14eaf03a93d
ms.openlocfilehash: 555ad8b04c83b92eaa6b097c3c7a14036a0cd8d1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298023"
---
# <a name="compiler-error-c2782"></a>Ошибка компилятора C2782

"объявление": параметр шаблона "идентификатор" неоднозначен

Компилятор не может определить тип аргумента шаблона.

Следующий пример приводит к возникновению ошибки C2782:

```cpp
// C2782.cpp
template<typename T>
void f(T, T) {}

int main() {
   f(1, 'c');   // C2782
   // try the following line instead
   // f<int>(1, 'c');
}
```

C2782 также может возникать при использовании универсальных шаблонов:

```cpp
// C2782b.cpp
// compile with: /clr
generic<typename T> void gf(T, T) { }

int main() {
   gf(1, 'c'); // C2782
   // try the following line instead
   // gf<int>(1, 'c');
}
```
