---
description: 'Дополнительные сведения о: Ошибка компилятора C2118'
title: Ошибка компилятора C2118
ms.date: 11/04/2016
f1_keywords:
- C2118
helpviewer_keywords:
- C2118
ms.assetid: bf4315d0-f085-4323-b813-96ee61a13bde
ms.openlocfilehash: 89ddf355e233e4fb2d6f36a53369d85bf8ea019a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170104"
---
# <a name="compiler-error-c2118"></a>Ошибка компилятора C2118

отрицательный индекс

Значение, определяющее размер массива, больше, чем максимальный размер массива или меньше нуля.

Следующий пример приводит к возникновению ошибки C2118:

```cpp
// C2118.cpp
int main() {
   int array1[-1];   // C2118
   int array2[3];   // OK
}
```
