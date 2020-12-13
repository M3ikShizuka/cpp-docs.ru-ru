---
description: 'Дополнительные сведения о: Ошибка компилятора C3290'
title: Ошибка компилятора C3290
ms.date: 11/04/2016
f1_keywords:
- C3290
helpviewer_keywords:
- C3290
ms.assetid: 0baf684b-1143-4953-ac99-a2fa267d8017
ms.openlocfilehash: 68c0e79c233f7fbd416f6bdbe42cc555c04731fa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337420"
---
# <a name="compiler-error-c3290"></a>Ошибка компилятора C3290

"тип": тривиальное свойство не может иметь ссылочный тип

Свойство объявлено неправильно. При объявлении обычного свойства компилятор создает переменную, которую будет обновлять свойство. В классе не может присутствовать ссылочная переменная с отслеживанием.

Дополнительные сведения см. в разделе [оператор ссылки на](../../extensions/tracking-reference-operator-cpp-component-extensions.md) [Свойства](../../extensions/property-cpp-component-extensions.md) и отслеживание.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3290:

```cpp
// C3290.cpp
// compile with: /clr /c
ref struct R {};

ref struct X {
   R^ mr;

   property R % y;   // C3290
   property R ^ x;   // OK

   // OK
   property R% prop {
      R% get() {
         return *mr;
      }

      void set(R%) {}
   }
};

int main() {
   X x;
   R% xp = x.prop;
}
```
