---
description: 'Дополнительные сведения о: Ошибка компилятора C3899'
title: Ошибка компилятора C3899
ms.date: 11/04/2016
f1_keywords:
- C3899
helpviewer_keywords:
- C3899
ms.assetid: 14e07e4a-f7a7-4309-baaa-649d69e12e23
ms.openlocfilehash: 04d8af9427d868b0890899d295f3aa6f678eafce
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97260050"
---
# <a name="compiler-error-c3899"></a>Ошибка компилятора C3899

"var": использование l-value элемента данных initonly не допускается непосредственно в параллельной области в классе "класс"

Элемент данных [initonly (C++/CLI)](../../dotnet/initonly-cpp-cli.md) не может быть инициализирован внутри этой части конструктора, находящегося в [параллельной](../../parallel/openmp/reference/openmp-directives.md#parallel) области.  Это обусловлено тем, что компилятор выполняет внутреннее перемещение кода таким образом, что он фактически больше не является частью конструктора.

Чтобы устранить эту проблему, инициализируйте элемент данных initonly в конструкторе, но за пределами параллельной области.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3899.

```cpp
// C3899.cpp
// compile with: /clr /openmp
#include <omp.h>

public ref struct R {
   initonly int x;
   R() {
      x = omp_get_thread_num() + 1000;   // OK
      #pragma omp parallel num_threads(5)
      {
         // cannot assign to 'x' here
         x = omp_get_thread_num() + 1000;   // C3899
         System::Console::WriteLine("thread {0}", omp_get_thread_num());
      }
      x = omp_get_thread_num() + 1000;   // OK
   }
};

int main() {
   R^ r = gcnew R;
   System::Console::WriteLine(r->x);
}
```
