---
description: 'Дополнительные сведения о: Ошибка компилятора C2990'
title: Ошибка компилятора C2990
ms.date: 11/04/2016
f1_keywords:
- C2990
helpviewer_keywords:
- C2990
ms.assetid: 674e9f6a-6743-4af0-a7ed-cbe11103a2f8
ms.openlocfilehash: 80aa15940420e9d3e452f2c3a93eefe94fd1561b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97328249"
---
# <a name="compiler-error-c2990"></a>Ошибка компилятора C2990

"класс": тип, не являющийся классом, уже объявлен как тип класса

Класс, не являющийся универсальным или шаблоном, переопределяет универсальный шаблон или класс шаблона. Проверьте файлы заголовков на наличие конфликтов.

Следующий пример приводит к возникновению ошибки C2990:

```cpp
// C2990.cpp
// compile with: /c
template <class T>
class C{};
class C{};   // C2990
```

C2990 также может возникать при использовании универсальных шаблонов:

```cpp
// C2990b.cpp
// compile with: /clr /c
generic <class T>
ref struct GC;

ref struct GC {};   // C2990
```

C2990 также может возникать из-за критического изменения в компиляторе Microsoft C++ для Visual Studio 2005; Теперь компилятор требует, чтобы несколько объявлений одного типа совпадали с спецификацией шаблона.

Следующий пример приводит к возникновению ошибки C2990:

```cpp
// C2990c.cpp
// compile with: /c
template<class T>
class A;

template<class T>
struct A2 {
   friend class A;   // C2990
};

// OK
template<class T>
struct B {
   template<class T>
   friend class A;
};
```
