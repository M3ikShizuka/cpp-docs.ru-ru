---
description: 'Дополнительные сведения о: Ошибка компилятора C2879'
title: Ошибка компилятора C2879
ms.date: 11/04/2016
f1_keywords:
- C2879
helpviewer_keywords:
- C2879
ms.assetid: ac92b645-2394-49de-8632-43d44e0553ed
ms.openlocfilehash: 6060678f71bf36d0af2e94e380a046ea7916ef05
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194375"
---
# <a name="compiler-error-c2879"></a>Ошибка компилятора C2879

"символ": для определения псевдонима пространства имен альтернативное имя может быть задано только для существующего пространства имен

Нельзя создать [псевдоним пространства имен](../../cpp/namespaces-cpp.md#namespace_aliases) для символа, отличного от пространства имен.

Следующий пример приводит к возникновению ошибки C2879:

```cpp
// C2879.cpp
int main() {
   int i;
   namespace A = i;   // C2879 i is not a namespace
}
```
