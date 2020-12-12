---
description: 'Дополнительные сведения о: Ошибка компилятора C2055'
title: Ошибка компилятора C2055
ms.date: 11/04/2016
f1_keywords:
- C2055
helpviewer_keywords:
- C2055
ms.assetid: 6cec79cc-6bec-443f-9897-fbf5452718c7
ms.openlocfilehash: 0692488b8e1ea91fe235ade512c5fbe5094cdaef
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97174940"
---
# <a name="compiler-error-c2055"></a>Ошибка компилятора C2055

Ожидался список формальных параметров, а не список типов

Определение функции содержит список типов параметров, а не список формальных параметров. ANSI C требует именования формальных параметров, если они не являются void или многоточием ( `...` ).

Следующий пример приводит к возникновению ошибки C2055:

```c
// C2055.c
// compile with: /c
void func(int, char) {}  // C2055
void func (int i, char c) {}   // OK
```
