---
description: 'Дополнительные сведения о: Ошибка компилятора C2101'
title: Ошибка компилятора C2101
ms.date: 11/04/2016
f1_keywords:
- C2101
helpviewer_keywords:
- C2101
ms.assetid: 42f0136f-8cc1-4f2b-be1c-721ec9278e66
ms.openlocfilehash: b41aa520d0aba3970689bf0bb5d65db5effb36aa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97278575"
---
# <a name="compiler-error-c2101"></a>Ошибка компилятора C2101

"&" в константе

Оператор address-of ( `&` ) должен иметь операнд l-value.

В следующем примере возникает ошибка C2101:

```cpp
// C2101.cpp
int main() {
   char test;
   test = &'a';   // C2101
   test = 'a';   // OK
}
```
