---
description: 'Дополнительные сведения о: Ошибка компилятора C3226'
title: Ошибка компилятора C3226
ms.date: 11/04/2016
f1_keywords:
- C3226
helpviewer_keywords:
- C3226
ms.assetid: 636106ca-6f4e-4303-a6a0-8803221ec67d
ms.openlocfilehash: f6c050f4e4c41e9ed5574c56fcc8067759cc172b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97304198"
---
# <a name="compiler-error-c3226"></a>Ошибка компилятора C3226

Объявление шаблона недопустимо внутри универсального объявления

Используйте универсальное объявление в универсальном классе.

Следующий пример приводит к возникновению ошибки C3226:

```cpp
// C3226.cpp
// compile with: /clr
generic <class T>
ref class C {
   template <class T1>   // C3226
   ref struct S1 {};
};
```

В следующем примере показано возможное решение:

```cpp
// C3226b.cpp
// compile with: /clr /c
generic <class T>
ref class C {
   generic <class T1>
   ref struct S1 {};
};
```
