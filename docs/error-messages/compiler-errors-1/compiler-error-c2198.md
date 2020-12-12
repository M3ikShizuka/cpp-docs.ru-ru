---
description: 'Дополнительные сведения о: Ошибка компилятора C2198'
title: Ошибка компилятора C2198
ms.date: 11/04/2016
f1_keywords:
- C2198
helpviewer_keywords:
- C2198
ms.assetid: 638a845c-9d7f-4115-a9aa-d72455605668
ms.openlocfilehash: 60c07bdaa422a3844bf17355fd88e7924ce05dc4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170039"
---
# <a name="compiler-error-c2198"></a>Ошибка компилятора C2198

"функция": слишком мало аргументов для вызова

Компилятор обнаружил слишком мало параметров для вызова функции или неправильное объявление функции.

При компиляции следующего примера возникнет ошибка C2198:

```c
// C2198.c
// compile with: /c
void func( int, int );
int main() {
   func( 1 );   // C2198 only one actual parameter
   func( 1, 1 );   // OK
}
```
