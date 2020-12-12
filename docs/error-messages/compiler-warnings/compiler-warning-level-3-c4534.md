---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4534'
title: Предупреждение компилятора (уровень 3) C4534
ms.date: 11/04/2016
f1_keywords:
- c4534
helpviewer_keywords:
- C4534
ms.assetid: ec2adf3b-d7a1-4005-bb0c-5d219df78dc8
ms.openlocfilehash: 6a13b27716488fa04f6342da76fdcd32c5635f2d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257892"
---
# <a name="compiler-warning-level-3-c4534"></a>Предупреждение компилятора (уровень 3) C4534

"Конструктор" не будет конструктором по умолчанию для класса "класс" из-за аргумента по умолчанию

Неуправляемый класс может иметь конструктор с параметрами, имеющими значения по умолчанию, и компилятор будет использовать его в качестве конструктора по умолчанию. Класс, помеченный с помощью `value` ключевого слова, не будет использовать конструктор со значениями по умолчанию для его параметров в качестве конструктора по умолчанию.

Дополнительные сведения см. в статье [Классы и структуры](../../extensions/classes-and-structs-cpp-component-extensions.md).

Следующий пример приводит к возникновению ошибки C4534:

```cpp
// C4534.cpp
// compile with: /W3 /clr /WX
value class MyClass {
public:
   int ii;
   MyClass(int i = 9) {   // C4534, will not be the default constructor
      i++;
   }
};

int main() {
   MyClass ^ xx = gcnew MyClass;
   xx->ii = 0;
}
```
