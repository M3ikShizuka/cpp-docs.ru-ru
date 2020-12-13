---
description: 'Дополнительные сведения о: Ошибка компилятора C2033'
title: Ошибка компилятора C2033
ms.date: 11/04/2016
f1_keywords:
- C2033
helpviewer_keywords:
- C2033
ms.assetid: fd5a1637-9db2-4c98-a7cc-b63b39737cd9
ms.openlocfilehash: c7beabafb544f1ad76f6a8eabe24bd20a7e63f62
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175434"
---
# <a name="compiler-error-c2033"></a>Ошибка компилятора C2033

"идентификатор": битовое поле не может иметь косвенное обращение

Битовое поле было объявлено как указатель, что не допускается.

Следующий пример приводит к возникновению ошибки C2033.

```cpp
// C2033.cpp
struct S {
   int *b : 1;  // C2033
};
```

Возможное решение:

```cpp
// C2033b.cpp
// compile with: /c
struct S {
   int b : 1;
};
```
