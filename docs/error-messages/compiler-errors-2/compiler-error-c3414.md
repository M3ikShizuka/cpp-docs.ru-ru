---
description: 'Дополнительные сведения о: Ошибка компилятора C3414'
title: Ошибка компилятора C3414
ms.date: 11/04/2016
f1_keywords:
- C3414
helpviewer_keywords:
- C3414
ms.assetid: 715f5432-b509-4f8f-84f5-e1463bac490f
ms.openlocfilehash: c16f57be5665110d8186bdedbb2ada0ac2fdacaa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321931"
---
# <a name="compiler-error-c3414"></a>Ошибка компилятора C3414

"член": не удается определить импортированную функцию элемента

Элемент был определен в коде, который также определен в сборке, на которую указывает ссылка.

Следующий пример приводит к возникновению ошибки C3414:

```cpp
// C3414a2.cpp
// compile with: /clr /LD
public ref class MyClass {
public:
   void Test(){}
};
```

затем:

```cpp
// C3414b2.cpp
// compile with: /clr
#using <C3414a2.dll>

void MyClass::Test() {    // C3414
}

System::Object::Object() {    // C3414
}
```
