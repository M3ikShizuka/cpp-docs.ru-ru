---
description: 'Дополнительные сведения о: Ошибка компилятора C2005'
title: Ошибка компилятора C2005
ms.date: 11/04/2016
f1_keywords:
- C2005
helpviewer_keywords:
- C2005
ms.assetid: 090530ed-e0ec-4358-833a-ca24260e7ffe
ms.openlocfilehash: 80ed80433d2e227b4c904d6ce4a68318feb98b05
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298582"
---
# <a name="compiler-error-c2005"></a>Ошибка компилятора C2005

\#в строке ожидался номер строки, обнаружен "token"

`#line`За директивой должен следовать номер строки.

Следующий пример приводит к возникновению ошибки C2005:

```cpp
// C2005.cpp
int main() {
   int i = 0;
   #line i   // C2005
}
```

Возможное решение:

```cpp
// C2005b.cpp
int main() {
   int i = 0;
   #line 0
}
```
