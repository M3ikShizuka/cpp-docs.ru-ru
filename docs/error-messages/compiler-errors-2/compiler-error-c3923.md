---
description: 'Дополнительные сведения о: Ошибка компилятора C3923'
title: Ошибка компилятора C3923
ms.date: 11/04/2016
f1_keywords:
- C3923
helpviewer_keywords:
- C3923
ms.assetid: db8838e9-6344-4cd6-83e0-a8abeb12c4c0
ms.openlocfilehash: 261ff6d5a3d7f6a246d906b1d91809d8764ca2bd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97220699"
---
# <a name="compiler-error-c3923"></a>Ошибка компилятора C3923

member: в функции-члене класса WinRT или управляемого класса невозможно использовать определения локальных классов, структур или объединений

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3923:

```cpp
// C3923.cpp
// compile with: /clr /c
ref struct x {
   void Test() {
      struct a {};   // C3923
      class b {};   // C3923
      union c {};   // C3923
   }
};
```
