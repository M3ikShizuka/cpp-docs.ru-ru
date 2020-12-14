---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4807'
title: Предупреждение компилятора (уровень 1) C4807
ms.date: 11/04/2016
f1_keywords:
- C4807
helpviewer_keywords:
- C4807
ms.assetid: 089c9f87-fd81-402e-9826-66a8ef1ef1fe
ms.openlocfilehash: 4c015d2ee7c566199411374402719c4a8eaee37f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97238145"
---
# <a name="compiler-warning-level-1-c4807"></a>Предупреждение компилятора (уровень 1) C4807

"операция": небезопасное смешение типа "тип" и битового поля со знаком типа "тип"

Это предупреждение создается при сравнении однобитового битового поля со знаком с **`bool`** переменной. Поскольку однобитовое битовое поле со знаком может содержать только значения-1 или 0, оно опасно для сравнения **`bool`** . Нет предупреждений о смешанных **`bool`** и одноразрядных битовых полей, так как они идентичны **`bool`** и могут содержать только 0 или 1.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению предупреждения C4807:

```cpp
// C4807.cpp
// compile with: /W1
typedef struct bitfield {
   signed mybit : 1;
} mybitfield;

int main() {
   mybitfield bf;
   bool b = true;

   // try..
   // int b = true;

   bf.mybit = -1;
   if (b == bf.mybit) {   // C4807
      b = false;
   }
}
```
