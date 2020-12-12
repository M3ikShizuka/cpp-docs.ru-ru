---
description: 'Дополнительные сведения о: Ошибка компилятора C3412'
title: Ошибка компилятора C3412
ms.date: 11/04/2016
f1_keywords:
- C3412
helpviewer_keywords:
- C3412
ms.assetid: aa4dd43b-54ce-4cda-85c1-1a77dd6e34fa
ms.openlocfilehash: aa0dc6cfeac193afc99d003cd821663bcfc139c8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97313194"
---
# <a name="compiler-error-c3412"></a>Ошибка компилятора C3412

"шаблон": не удается заспециализациь шаблона в текущей области

Шаблон не может быть специализированным в области видимости класса, только в области глобальных или пространств имен.

## <a name="examples"></a>Примеры

Следующий пример приводит к возникновению ошибки C3412.

```cpp
// C3412.cpp
template <class T>
struct S {
   template <>
   struct S<int> {};   // C3412 in a class
};
```

В следующем примере показано возможное решение.

```cpp
// C3412b.cpp
// compile with: /c
template <class T>
struct S {};

template <>
struct S<int> {};
```
