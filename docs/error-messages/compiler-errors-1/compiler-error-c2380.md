---
description: 'Дополнительные сведения о: Ошибка компилятора C2380'
title: Ошибка компилятора C2380
ms.date: 11/04/2016
f1_keywords:
- C2380
helpviewer_keywords:
- C2380
ms.assetid: 717b1e6e-ddfe-4bac-a5f3-7f9a4dcb1572
ms.openlocfilehash: 4455fef072b6d8f686d5f43130db8d02aba69fd1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97174693"
---
# <a name="compiler-error-c2380"></a>Ошибка компилятора C2380

типы перед "идентификатором" (конструктор с возвращаемым типом или недопустимое переопределение текущего имени класса?)

Конструктор возвращает значение или переопределяет имя класса.

При компиляции следующего примера возникнет ошибка C2326:

```cpp
// C2380.cpp
// compile with: /c
class C {
public:
   int C();   // C2380, specifies an int return
   int C;   // C2380, redefinition of i
   C();   // OK
};
```
