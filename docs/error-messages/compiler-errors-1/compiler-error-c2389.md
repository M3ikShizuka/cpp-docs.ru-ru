---
description: 'Дополнительные сведения о: Ошибка компилятора C2389'
title: Ошибка компилятора C2389
ms.date: 11/04/2016
f1_keywords:
- C2389
helpviewer_keywords:
- C2389
ms.assetid: 6122dc81-4ee3-49a5-a67d-d867808c9bac
ms.openlocfilehash: 1f9d34be47376564bf7c6fc221cf6f5b01e7850f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97123972"
---
# <a name="compiler-error-c2389"></a>Ошибка компилятора C2389

"оператор": недопустимый операнд nullptr

**`nullptr`** не может быть операндом.

В следующем примере возникает ошибка C2389:

```cpp
// C2389.cpp
// compile with: /clr
int main() {
   throw nullptr;   // C2389
}
```
