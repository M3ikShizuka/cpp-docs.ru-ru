---
description: 'Дополнительные сведения о: Ошибка компилятора C2318'
title: Ошибка компилятора C2318
ms.date: 11/04/2016
f1_keywords:
- C2318
helpviewer_keywords:
- C2318
ms.assetid: 169e30b9-df78-46cb-90bf-576ad3c32fd4
ms.openlocfilehash: 3cec8dbb46b10b4889a9cd026144bea228a28f15
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97322153"
---
# <a name="compiler-error-c2318"></a>Ошибка компилятора C2318

нет блока try, связанного с этим блоком catch

**`catch`** Обработчик определен, но не предшествует **`try`** блоку.

В следующем примере возникает ошибка C2318:

```cpp
// C2318.cpp
// compile with: /EHsc
#include <eh.h>
int main() {
   // no try block
   catch( int ) {}   // C2318
}
```

Возможное решение:

```cpp
// C2318b.cpp
// compile with: /EHsc
#include <eh.h>
int main() {
   try{}
   catch( int ) {}
}
```
