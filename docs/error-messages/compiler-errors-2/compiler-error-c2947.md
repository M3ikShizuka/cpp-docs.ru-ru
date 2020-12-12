---
description: 'Дополнительные сведения о: Ошибка компилятора C2947'
title: Ошибка компилятора C2947
ms.date: 11/04/2016
f1_keywords:
- C2947
helpviewer_keywords:
- C2947
ms.assetid: 6c056f62-ec90-4883-8a67-aeeb6ec13546
ms.openlocfilehash: 5b1780d49f97bfab33e70a4dd7b1958b56c8df14
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97189487"
---
# <a name="compiler-error-c2947"></a>Ошибка компилятора C2947

Ожидается ">" для завершения конструкции, обнаружен "синтаксис"

Возможно, список аргументов универсального типа или шаблона не был корректно завершен.

C2947 также может формироваться с помощью синтаксических ошибок.

Следующий пример приводит к возникновению ошибки C2947:

```cpp
// C2947.cpp
// compile with: /c
template <typename T>=   // C2947
// try the following line instead
// template <typename T>
struct A {};
```
