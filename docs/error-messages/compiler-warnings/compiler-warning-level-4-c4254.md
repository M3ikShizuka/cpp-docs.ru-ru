---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4254'
title: Предупреждение компилятора (уровень 4) C4254
ms.date: 11/04/2016
f1_keywords:
- c4254
helpviewer_keywords:
- C4254
ms.assetid: c7dcef24-d535-4c98-bb41-fc3d2b88fd11
ms.openlocfilehash: 112a8c4af016b15f6a5ec4c6e138381a8ee32405
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97294708"
---
# <a name="compiler-warning-level-4-c4254"></a>Предупреждение компилятора (уровень 4) C4254

"оператор": преобразование из "тип1" в "тип2", возможна утрата данных

Более крупное битовое поле было назначено меньшему битовому полю. Возможна утрата данных.

Это предупреждение отключено по умолчанию. Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

Следующий пример приводит к возникновению ошибки C4254:

```cpp
// C4254.cpp
// compile with: /W4
#pragma warning(default: 4254)

struct X {
   int a : 20;
   int b : 12;
};

int main() {
   X *x = new X();
   x->b = 10;
   x->a = 4;
   x->a = x->b;    // OK
   x->b = x->a;    // C4254
};
```
