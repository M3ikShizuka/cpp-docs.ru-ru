---
description: 'Дополнительные сведения о: Ошибка компилятора C2229'
title: Ошибка компилятора C2229
ms.date: 11/04/2016
f1_keywords:
- C2229
helpviewer_keywords:
- C2229
ms.assetid: 933c7cf2-a463-4e74-b0b4-59dedad987fb
ms.openlocfilehash: d95d1248ec7e555af0c4ecfffa25dc69af288458
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194986"
---
# <a name="compiler-error-c2229"></a>Ошибка компилятора C2229

тип "идентификатор" имеет недопустимый массив нулевого размера

Член структуры или битового поля содержит массив нулевого размера, который не является последним элементом.

Поскольку массив нулевого размера можно использовать в качестве последнего элемента структуры, необходимо указать его размер при выделении структуры.

Если массив нулевого размера не является последним членом структуры, компилятор не может вычислить смещение для остальных полей.

Следующий пример приводит к возникновению ошибки C2229:

```cpp
// C2229.cpp
struct S {
   int a[0];  // C2229  zero-sized array
   int b[1];
};

struct S2 {
   int a;
   int b[0];
};

int main() {
   // allocate 7 elements for b field
   S2* s2 = (S2*)new int[sizeof(S2) + 7*sizeof(int)];
   s2->b[6] = 100;
}
```
