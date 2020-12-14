---
description: 'Дополнительные сведения о: Ошибка компилятора C2549'
title: Ошибка компилятора C2549
ms.date: 11/04/2016
f1_keywords:
- C2549
helpviewer_keywords:
- C2549
ms.assetid: 29310094-54a3-4605-bc6d-a312a68daf5d
ms.openlocfilehash: b254b70fd0a8405ec96fffb1f37cb17c5f7b7f2d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97260272"
---
# <a name="compiler-error-c2549"></a>Ошибка компилятора C2549

определяемое пользователем преобразование не может указывать тип возвращаемого значения

Следующий пример приводит к возникновению ошибки C2549:

```cpp
// C2549.cpp
// compile with: /c
class X {
public:
   int operator int() { return value; }   // C2549

   // try the following line instead
   // operator int() { return value; }
private:
   int value;
};
```
