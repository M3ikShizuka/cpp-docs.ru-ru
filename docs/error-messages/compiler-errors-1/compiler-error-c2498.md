---
description: 'Дополнительные сведения о: Ошибка компилятора C2498'
title: Ошибка компилятора C2498
ms.date: 11/04/2016
f1_keywords:
- C2498
helpviewer_keywords:
- C2498
ms.assetid: 0839f12c-aaa4-4a02-bb33-7f072715dd14
ms.openlocfilehash: e7cbb811cdaeea703d0f1da1c0f2012ebe8210fa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335097"
---
# <a name="compiler-error-c2498"></a>Ошибка компилятора C2498

"функция": "vtable" можно применять только к объявлениям или определениям классов

Эта ошибка может быть вызвана использованием `__declspec(novtable)` функции с функцией.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2498:

```cpp
// C2498.cpp
// compile with: /c
void __declspec(novtable) f() {}   // C2498
class __declspec(novtable) A {};   // OK
```
