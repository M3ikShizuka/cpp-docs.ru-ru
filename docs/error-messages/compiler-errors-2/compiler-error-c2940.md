---
description: 'Дополнительные сведения о: Ошибка компилятора C2940'
title: Ошибка компилятора C2940
ms.date: 11/04/2016
f1_keywords:
- C2940
helpviewer_keywords:
- C2940
ms.assetid: af6bf2bf-8de6-4cfd-bbf0-4c6b32a30edf
ms.openlocfilehash: 2601e32d2e52d332e4f6443dde23b544d955aac1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97249689"
---
# <a name="compiler-error-c2940"></a>Ошибка компилятора C2940

"класс": идентификатор класса типа переопределен как локальное определение типа (typedef)

Универсальный шаблон или класс шаблона нельзя использовать в качестве локального **`typedef`** .

Следующий пример приводит к возникновению ошибки C2940:

```cpp
// C2940.cpp
template<class T>
struct TC {};
int main() {
   typedef int TC<int>;   // C2940
   typedef int TC;   // OK
}
```

Ошибка C2940 также может возникнуть при использовании универсальных шаблонов:

```cpp
// C2940b.cpp
// compile with: /clr
generic<class T>
ref struct GC { };

int main() {
   typedef int GC<int>;   // C2940
   typedef int GC;
}
```
