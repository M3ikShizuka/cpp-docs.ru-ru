---
description: 'Дополнительные сведения о: Ошибка компилятора C3842'
title: Ошибка компилятора C3842
ms.date: 11/04/2016
f1_keywords:
- C3842
helpviewer_keywords:
- C3842
ms.assetid: 41a1a44a-c618-40a2-8d26-7da27d14095d
ms.openlocfilehash: dd5cff7b4a381ca976138720d8af192d594c7836
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97255422"
---
# <a name="compiler-error-c3842"></a>Ошибка компилятора C3842

function: квалификаторы const и volatile для функций-членов управляемых типов или типов WinRT не поддерживаются

[const](../../cpp/const-cpp.md) и [volatile](../../cpp/volatile-cpp.md) не поддерживаются для функций членов среда выполнения Windows или управляемых типов.

Следующий пример приводит к возникновению ошибки C3842:

```cpp
// C3842a.cpp
// compile with: /clr /c
public ref struct A {
   void f() const {}   // C3842
   void f() volatile {}   // C3842

   void f() {}
};
```
