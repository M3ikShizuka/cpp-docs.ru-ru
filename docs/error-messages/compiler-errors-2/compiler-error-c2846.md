---
description: 'Дополнительные сведения о: Ошибка компилятора C2846'
title: Ошибка компилятора C2846
ms.date: 11/04/2016
f1_keywords:
- C2846
helpviewer_keywords:
- C2846
ms.assetid: bc090ec2-5410-4112-9ec6-261325374375
ms.openlocfilehash: ecd6d480bdd485e3c623da8563c7f0eefe8e70c8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97260232"
---
# <a name="compiler-error-c2846"></a>Ошибка компилятора C2846

"Constructor": интерфейс не может иметь конструктор

[Интерфейс](../../cpp/interface.md) Visual C++ не может иметь конструктор.

Следующий пример приводит к возникновению ошибки C2846:

```cpp
// C2846.cpp
// compile with: /c
__interface C {
   C();   // C2846 constructor not allowed in an interface
};
```
