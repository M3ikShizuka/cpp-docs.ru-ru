---
description: 'Дополнительные сведения о: Ошибка компилятора C2923'
title: Ошибка компилятора C2923
ms.date: 11/04/2016
f1_keywords:
- C2923
helpviewer_keywords:
- C2923
ms.assetid: 6b92933b-13ef-4124-99d9-b89f9fdae030
ms.openlocfilehash: 7897ba68998f88f82144278e79c97d8fec9f85d7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97270281"
---
# <a name="compiler-error-c2923"></a>Ошибка компилятора C2923

"тип": "идентификатор" не является допустимым аргументом типа шаблона для параметра "параметр"

В списке аргументов пропущен тип, необходимый для создания экземпляра шаблона или универсального класса. Проверьте объявление шаблона или универсального класса.

Следующий пример приводит к возникновению ошибки C2923:

```cpp
// C2923.cpp
template <class T> struct TC {};
int x;
int main() {
   TC<x>* tc2;   // C2923
   TC<int>* tc2;   // OK
}
```

Ошибка C2923 также может возникнуть при использовании универсальных шаблонов.

```cpp
// C2923b.cpp
// compile with: /clr /c
generic <class T> ref struct GC {};

int x;

int main() {
   GC<x>^ gc2;   // C2923
   GC<int>^ gc2;   // OK
}
```
