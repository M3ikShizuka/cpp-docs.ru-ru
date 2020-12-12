---
description: 'Дополнительные сведения о: Ошибка компилятора ошибка C2944'
title: Ошибка компилятора C2944
ms.date: 11/04/2016
f1_keywords:
- C2944
helpviewer_keywords:
- C2944
ms.assetid: f209e668-e72f-442a-a438-8c4ff43a404a
ms.openlocfilehash: a25b7da5f2a3a4320b4e85dfc3bd71626795a4d0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97249559"
---
# <a name="compiler-error-c2944"></a>Ошибка компилятора C2944

"класс": идентификатор типа класса переопределен как аргумент значения шаблона

Нельзя использовать универсальный класс или класс шаблона в качестве аргумента значения шаблона вместо символа.

В следующем примере возникает ошибка C2944:

```cpp
// C2944.cpp
// compile with: /c
template<class T>
class TC { };

template <int TC<int> > struct X1 { };   // C2944

template <class T > struct X2 {};
```

Ошибка C2944 также может возникнуть при использовании универсальных шаблонов:

```cpp
// C2944b.cpp
// compile with: /clr /c
generic<class T>
ref class GC {};

template <int GC<int> > struct X2 { };   // C2944
template <class T> struct X3 {};   // OK
```
