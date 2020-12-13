---
description: 'Дополнительные сведения о: Ошибка компилятора C2180'
title: Ошибка компилятора C2180
ms.date: 11/04/2016
f1_keywords:
- C2180
helpviewer_keywords:
- C2180
ms.assetid: ea71b39e-b977-48a7-b7bd-af68ef5e263b
ms.openlocfilehash: 46ab20e3abfc35355543f90389677737e231257f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335191"
---
# <a name="compiler-error-c2180"></a>Ошибка компилятора C2180

управляющее выражение имеет тип type

Управляющее выражение в **`if`** **`while`** **`for`** операторе,, или **`do`** является выражением, приводимым к типу **`void`** . Чтобы устранить эту проблему, измените управляющее выражение на одно, создающее, **`bool`** или тип, который можно преобразовать в **`bool`** .

Следующий пример приводит к возникновению ошибки C2180:

```c
// C2180.c

int main() {
   while ((void)1)   // C2180
      return 1;
   while (1)         // OK
      return 0;
}
```
