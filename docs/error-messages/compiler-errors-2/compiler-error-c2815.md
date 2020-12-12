---
description: 'Дополнительные сведения о: Ошибка компилятора C2815'
title: Ошибка компилятора C2815
ms.date: 11/04/2016
f1_keywords:
- C2815
helpviewer_keywords:
- C2815
ms.assetid: d0256fd6-0721-4c99-b03c-52d96e77a613
ms.openlocfilehash: fd0ee162c10acd89e4746ea906d64ea8ef069271
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194843"
---
# <a name="compiler-error-c2815"></a>Ошибка компилятора C2815

"operator delete": первый формальный параметр должен иметь значение "void *", но был использован "param"

Любая функция [удаления оператора](../../standard-library/new-operators.md#op_delete) , определяемого пользователем, должна принимать первый формальный параметр типа `void *` .

Следующий пример приводит к возникновению ошибки C2815:

```cpp
// C2815.cpp
// compile with: /c
class CMyClass {
public:
   void mf1(int *a);
   void operator delete(CMyClass *);   // C2815
   void operator delete(void *);
};
```
