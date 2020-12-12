---
description: 'Дополнительные сведения о: Ошибка компилятора C2976'
title: Ошибка компилятора C2976
ms.date: 11/04/2016
f1_keywords:
- C2976
helpviewer_keywords:
- C2976
ms.assetid: d9bf9836-325e-4f72-a7e3-a67cf19d32e7
ms.openlocfilehash: 645b4437bba022e53d018aec18d81b5f108d4d93
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97281903"
---
# <a name="compiler-error-c2976"></a>Ошибка компилятора C2976

"идентификатор": слишком мало аргументов типа

В универсальном шаблоне или отсутствует один или несколько фактических аргументов. Проверьте объявление универсального класса или шаблона, чтобы определить правильное число параметров.

Эта ошибка может быть вызвана отсутствием аргументов шаблона в компонентах стандартной библиотеки C++.

Следующий пример приводит к возникновению ошибки C2976:

```cpp
// C2976.cpp
template <class T>
struct TC {
   T t;
};
int main() {
   TC<>* t;   // C2976
   TC<int>* t2;   // OK
}
```

C2976 также может возникать при использовании универсальных шаблонов:

```cpp
// C2976b.cpp
// compile with: /clr
generic <class T>
ref struct GC {
   T t;
};

int main() {
   GC<>^ g;   // C2976
   GC<int>^ g2;   // OK
}
```
