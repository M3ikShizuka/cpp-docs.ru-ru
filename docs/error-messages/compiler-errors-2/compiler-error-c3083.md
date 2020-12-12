---
description: 'Дополнительные сведения о: Ошибка компилятора C3083'
title: Ошибка компилятора C3083
ms.date: 11/04/2016
f1_keywords:
- C3083
helpviewer_keywords:
- C3083
ms.assetid: 05ff791d-52bb-41eb-9511-3ef89d7f4710
ms.openlocfilehash: 76740dfc9f95fd06cafc580acd2ab2a6b705d8ea
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320145"
---
# <a name="compiler-error-c3083"></a>Ошибка компилятора C3083

"функция": символ слева от "::" должен быть типом

Функция была вызвана неправильно.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3083.

```cpp
// C3083.cpp
// compile with: /c
struct N {
   ~N();
};

struct N1 {
   ~N1();
};

N::N::~N() {}   // C3083
N1::~N1() {}   // OK
```
