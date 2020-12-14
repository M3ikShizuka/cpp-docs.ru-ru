---
description: 'Дополнительные сведения о: Ошибка компилятора C2801'
title: Ошибка компилятора C2801
ms.date: 11/04/2016
f1_keywords:
- C2801
helpviewer_keywords:
- C2801
ms.assetid: 35dfc7ea-9e37-4e30-baa1-944dc61302f5
ms.openlocfilehash: ca7e74f99b91b5a6699cdf3361ab64a89b7a7392
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97297477"
---
# <a name="compiler-error-c2801"></a>Ошибка компилятора C2801

"operator оператор" должен быть не статическим членом

Следующие операторы можно перегружать только как нестатические члены:

- Сваивать `=`

- Доступ к членам класса `->`

- Перегрузке индексации `[]`

- Вызов функции `()`

Возможные причины C2801:

- Перегруженный оператор не является членом класса, структуры или объединения.

- Объявлен перегруженный оператор **`static`** .

- Следующий пример приводит к возникновению ошибки C2801:

```cpp
// C2801.cpp
// compile with: /c
operator[]();   // C2801 not a member
class A {
   static operator->();   // C2801 static
   operator()();   // OK
};
```
