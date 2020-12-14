---
description: 'Дополнительные сведения о: Ошибка компилятора C2803'
title: Ошибка компилятора C2803
ms.date: 11/04/2016
f1_keywords:
- C2803
helpviewer_keywords:
- C2803
ms.assetid: 2cdbe374-8cc4-4c4e-ba15-062a7479e937
ms.openlocfilehash: 405c14d05bad4c505d847b8ab2648a7ace3b9a4b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97297438"
---
# <a name="compiler-error-c2803"></a>Ошибка компилятора C2803

"operator оператор" должен иметь хотя бы один формальный параметр типа класса

Перегруженный оператор не имеет параметра типа класса.

Необходимо передать хотя бы один параметр по ссылке (не используя указатели, но ссылки) или по значению, чтобы иметь возможность писать "a < b" (а и b типа класса A).

Если оба параметра являются указателями, это будет чистое сравнение адресов указателей и не будет использовать определенное пользователем преобразование.

Следующий пример приводит к возникновению ошибки C2803:

```cpp
// C2803.cpp
// compile with: /c
class A{};
bool operator< (const A *left, const A *right);   // C2803
// try the following line instead
// bool operator< (const A& left, const A& right);
```
