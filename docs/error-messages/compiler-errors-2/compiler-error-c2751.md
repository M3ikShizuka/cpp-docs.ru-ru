---
description: 'Дополнительные сведения о: Ошибка компилятора C2751'
title: Ошибка компилятора C2751
ms.date: 11/04/2016
f1_keywords:
- C2751
helpviewer_keywords:
- C2751
ms.assetid: 44a3abdf-8a87-4a09-b34b-532c220c310a
ms.openlocfilehash: 5eb41526946ee4318d8a1e96b04a527c828c914c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97174459"
---
# <a name="compiler-error-c2751"></a>Ошибка компилятора C2751

"параметр": имя параметра функции не может быть полным

В качестве параметра функции нельзя использовать полное имя.

Следующий пример приводит к возникновению ошибки C2751:

```cpp
// C2751.cpp
namespace std {
   template<typename T>
   class list {};
}

#define list std::list
void f(int &list){}   // C2751
```
