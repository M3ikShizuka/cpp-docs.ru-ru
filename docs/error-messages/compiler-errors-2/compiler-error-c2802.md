---
description: 'Дополнительные сведения о: Ошибка компилятора C2802'
title: Ошибка компилятора C2802
ms.date: 11/04/2016
f1_keywords:
- C2802
helpviewer_keywords:
- C2802
ms.assetid: 08b68c0e-9382-40ac-8949-39a7a2749e05
ms.openlocfilehash: ff526306b89a5679147a30e7b3cd2f07ddc2b8f5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97297451"
---
# <a name="compiler-error-c2802"></a>Ошибка компилятора C2802

статический член "operator оператор" не имеет формальных параметров

Оператор, объявленный **`static`** функцией-членом, должен иметь хотя бы один параметр.

Следующий пример приводит к возникновению ошибки C2802:

```cpp
// C2802.cpp
// compile with: /clr /c
ref class A {
   static operator+ ();   // C2802
   static operator+ (A^, A^);   // OK
};
```
