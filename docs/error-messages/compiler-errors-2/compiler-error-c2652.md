---
description: 'Дополнительные сведения о: Ошибка компилятора C2652'
title: Ошибка компилятора C2652
ms.date: 11/04/2016
f1_keywords:
- C2652
helpviewer_keywords:
- C2652
ms.assetid: 6e3d1a90-a989-4088-8afd-dc82f6a2d66f
ms.openlocfilehash: 6d0f85a089c527ce299e007ce04d96ac68daaf56
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97286180"
---
# <a name="compiler-error-c2652"></a>Ошибка компилятора C2652

"идентификатор": недопустимый конструктор копии: первый параметр не должен быть "идентификатором"

Первый параметр в конструкторе копий имеет тот же тип, что и класс, структура или объединение, для которого он определен. Первый параметр может быть ссылкой на тип, но не сам тип.

Следующий пример приводит к возникновению ошибки C2651:

```cpp
// C2652.cpp
// compile with: /c
class A {
   A( A );   // C2652 takes an A
};
class B {
   B( B& );   // OK, reference to B
};
```
