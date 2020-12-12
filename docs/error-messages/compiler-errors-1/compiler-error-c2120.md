---
description: 'Дополнительные сведения о: Ошибка компилятора C2120'
title: Ошибка компилятора C2120
ms.date: 11/04/2016
f1_keywords:
- C2120
helpviewer_keywords:
- C2120
ms.assetid: b0f3f66c-6cd2-4f48-9ea3-c270b53c2b8c
ms.openlocfilehash: 064c0587275d85c3cff520075352825d17d41aef
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170062"
---
# <a name="compiler-error-c2120"></a>Ошибка компилятора C2120

"void" недопустимо для всех типов

**`void`** Тип используется в объявлении с другим типом.

Следующий пример приводит к возникновению ошибки C2120:

```cpp
// C2120.cpp
int main() {
   void int i;   // C2120
   int j;   // OK
}
```
