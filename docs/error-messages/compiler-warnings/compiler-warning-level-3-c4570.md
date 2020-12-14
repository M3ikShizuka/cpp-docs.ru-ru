---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4570'
title: Предупреждение компилятора (уровень 3) C4570
ms.date: 11/04/2016
f1_keywords:
- C4570
helpviewer_keywords:
- C4570
ms.assetid: feec1225-e6ad-4995-8d96-c22e864a77bd
ms.openlocfilehash: aa776654b77f8d548f197ac2dc35bd4474e92068
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257775"
---
# <a name="compiler-warning-level-3-c4570"></a>Предупреждение компилятора (уровень 3) C4570

"тип": не объявлен явно как абстрактный, но имеет абстрактные функции

Тип, содержащий [абстрактные](../../extensions/abstract-cpp-component-extensions.md) функции, должен быть помечен как abstract.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4570.

```cpp
// C4570.cpp
// compile with: /clr /W3 /c
ref struct X {   // C4570
// try the following line instead
// ref class X abstract {
   virtual void f() abstract;
};
```
