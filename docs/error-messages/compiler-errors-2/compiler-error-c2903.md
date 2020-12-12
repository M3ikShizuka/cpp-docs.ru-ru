---
description: 'Дополнительные сведения о: Ошибка компилятора C2903'
title: Ошибка компилятора C2903
ms.date: 11/04/2016
f1_keywords:
- C2903
helpviewer_keywords:
- C2903
ms.assetid: bf6b223f-4921-48c7-82b9-ff318b42c801
ms.openlocfilehash: 0013be28857ac8e138a78cb7a4e3502cdc04536b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97270736"
---
# <a name="compiler-error-c2903"></a>Ошибка компилятора C2903

"идентификатор: символ не является ни шаблоном класса, ни шаблоном функции

Код пытается явно создать экземпляр объекта, который не является шаблоном.

В следующем примере возникает ошибка C2903:

```cpp
// C2903.cpp
// compile with: /c
namespace N {
   template<class T> class X {};
   class Y {};
}
void g() {
   N::template Y y;   // C2903
   N::X<N::Y> y;   // OK
}
```

Ошибка C2903 также может возникнуть при использовании универсальных шаблонов:

```cpp
// C2903b.cpp
// compile with: /clr /c
namespace N {
   class Y {};
   generic<class T> ref class Z {};
}

void f() {
   N::generic Y y;   // C2903
   N:: generic Z<int>^ z;   // OK
}
```
