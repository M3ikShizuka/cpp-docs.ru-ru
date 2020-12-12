---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4401'
title: Предупреждение компилятора (уровень 1) C4401
ms.date: 11/04/2016
f1_keywords:
- C4401
helpviewer_keywords:
- C4401
ms.assetid: 2e7ca136-f144-4b40-b847-82976e8643fc
ms.openlocfilehash: c6314b64ef9a675f8838cc7c3f4c89c2d6063231
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97212744"
---
# <a name="compiler-warning-level-1-c4401"></a>Предупреждение компилятора (уровень 1) C4401

"битовое поле": член является битовым полем

Встроенный код ассемблера пытается получить доступ к члену битового поля. Встроенная сборка не может получить доступ к членам битовых полей, поэтому используется последняя граница упаковки перед элементом битового поля.

Чтобы избежать этого предупреждения, приведите битовое поле к соответствующему типу перед тем, как сделать ссылку во встроенном коде ассемблера. Следующий пример приводит к возникновению ошибки C4401:

```cpp
// C4401.cpp
// compile with: /W1
// processor: x86
typedef struct bitfield {
   signed bit : 1;
} mybitfield;

int main() {
   mybitfield bf;
   bf.bit = 0;
   __asm {
      mov bf.bit,0;   // C4401
   }

   /* use the following __asm block to resolve the warning
   int i = (int)bf.bit;
   __asm {
      mov i,0;
   }
   */
}
```
