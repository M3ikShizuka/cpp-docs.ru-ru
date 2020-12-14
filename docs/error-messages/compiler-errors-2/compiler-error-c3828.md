---
description: 'Дополнительные сведения о: Ошибка компилятора C3828'
title: Ошибка компилятора C3828
ms.date: 11/04/2016
f1_keywords:
- C3828
helpviewer_keywords:
- C3828
ms.assetid: 8d9cee75-9504-4bc8-88b6-2413618a3f45
ms.openlocfilehash: 90c731ffc636355b5c9a1963facbcccabf356700
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97249325"
---
# <a name="compiler-error-c3828"></a>Ошибка компилятора C3828

"тип объекта": аргументы размещения не допускаются при создании экземпляров управляемых или Винртклассес

При создании объекта управляемого типа или типа среда выполнения Windows нельзя использовать форму размещения оператора [ref new, gcnew](../../extensions/ref-new-gcnew-cpp-component-extensions.md) или [New](../../cpp/new-operator-cpp.md).

В следующем примере показано возникновение ошибки C3828 и приводятся сведения по ее устранению.

```cpp
// C3828a.cpp
// compile with: /clr
ref struct M {
};

ref struct N {
   static array<char>^ bytes = gcnew array<char>(256);
};

int main() {
   M ^m1 = new (&N::bytes) M();   // C3828
   // The following line fixes the error.
   // M ^m1 = gcnew M();
}
```
