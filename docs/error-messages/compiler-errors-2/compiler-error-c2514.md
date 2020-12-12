---
description: 'Дополнительные сведения о: Ошибка компилятора C2514'
title: Ошибка компилятора C2514
ms.date: 11/04/2016
f1_keywords:
- C2514
helpviewer_keywords:
- C2514
ms.assetid: 4b7085e5-6714-4261-80b7-bc72e64ab3e8
ms.openlocfilehash: 3999a5a65df08142b68e7257b257d39d1b5245e9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97212822"
---
# <a name="compiler-error-c2514"></a>Ошибка компилятора C2514

"класс": класс не имеет конструкторов

Класс, структура или объединение не имеет конструктора со списком параметров, который соответствует параметрам, используемым для его создания.

Класс должен быть полностью объявлен, прежде чем его можно будет создать.

Следующий пример приводит к возникновению ошибки C2514:

```cpp
// C2514.cpp
// compile with: /c
class f;

class g {
public:
    g (int x);
};

class fmaker {
   f *func1() {
      return new f(2);   // C2514
   }

   g *func2() {
      return new g(2);   // OK
   }
};
```
