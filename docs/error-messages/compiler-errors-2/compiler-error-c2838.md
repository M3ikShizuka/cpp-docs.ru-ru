---
description: 'Дополнительные сведения о: Ошибка компилятора C2838'
title: Ошибка компилятора C2838
ms.date: 11/04/2016
f1_keywords:
- C2838
helpviewer_keywords:
- C2838
ms.assetid: 176b2ad6-7a84-4019-b97e-328866054457
ms.openlocfilehash: 70bc1fa038df33cfe63fccd7dc3db8983950b525
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194401"
---
# <a name="compiler-error-c2838"></a>Ошибка компилятора C2838

"член": недопустимое полное имя в объявлении члена

Класс, структура или объединение использует полное имя для повторного объявления члена другого класса, структуры или объединения.

Следующий пример приводит к возникновению ошибки C2838:

```cpp
// C2838.cpp
// compile with: /c
class Bellini {
public:
    void Norma();
};

class Bottesini {
   Bellini::Norma();  // C2838
};
```
