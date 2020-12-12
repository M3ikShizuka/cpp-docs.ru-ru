---
description: 'Дополнительные сведения о: Ошибка компилятора C2929'
title: Ошибка компилятора C2929
ms.date: 11/04/2016
f1_keywords:
- C2929
helpviewer_keywords:
- C2929
ms.assetid: 11134027-6adc-4733-b6bd-b94486bd1933
ms.openlocfilehash: b110615a05a416b6bba7256c7f59f734179677a2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320391"
---
# <a name="compiler-error-c2929"></a>Ошибка компилятора C2929

"идентификатор": явное создание экземпляра; не удается принудительно использовать и запретить создание экземпляра члена класса-шаблона

Невозможно явно создать экземпляр идентификатора и при этом запретить его создание.

Следующий пример приводит к возникновению ошибки C2929:

```cpp
// C2929.cpp
// compile with: /c
template<typename T>
class A {
public:
   A() {}
};

template A<int>::A();

extern template A<int>::A();   // C2929
```
