---
description: 'Дополнительные сведения о: Ошибка компилятора C3231'
title: Ошибка компилятора C3231
ms.date: 11/04/2016
f1_keywords:
- C3231
helpviewer_keywords:
- C3231
ms.assetid: fe5dc352-e634-45fa-9534-3da176294c98
ms.openlocfilehash: 4b6a89ab1c5ecefad62852d8214c8edc3c10ccb1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97304094"
---
# <a name="compiler-error-c3231"></a>Ошибка компилятора C3231

"arg": аргумент типа шаблона не может использовать параметр универсального типа

Экземпляры шаблонов создаются во время компиляции, но экземпляры универсальных объектов создаются во время выполнения. Следовательно, невозможно создать универсальный код, который может вызывать шаблон, поскольку экземпляр шаблона не создается во время выполнения, когда универсальный тип становится известен.

Следующий пример приводит к возникновению ошибки C3231:

```cpp
// C3231.cpp
// compile with: /clr /LD
template <class T> class A;

generic <class T>
ref class C {
   void f() {
      A<T> a;   // C3231
   }
};
```
