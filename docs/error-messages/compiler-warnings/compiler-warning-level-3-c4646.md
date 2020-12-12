---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4646'
title: Предупреждение компилятора (уровень 3) C4646
ms.date: 11/04/2016
f1_keywords:
- C4646
helpviewer_keywords:
- C4646
ms.assetid: 23677e8e-603e-40e0-b99a-2e4894a1278e
ms.openlocfilehash: 045c5d4557a50824235833528f8b46ff77b683e1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97301832"
---
# <a name="compiler-warning-level-3-c4646"></a>Предупреждение компилятора (уровень 3) C4646

функция, объявленная с атрибутом __declspec(noreturn) имеет тип, отличный от void

Функция, помеченная [](../../cpp/noreturn.md) **`__declspec`** модификатором noreturn, должна иметь тип возвращаемого значения [void](../../cpp/void-cpp.md) .

В следующем примере возникает ошибка C4646.

```cpp
// C4646.cpp
// compile with: /W3 /WX
int __declspec(noreturn) TestFunction()
{   // C4646  make return type void
}
```
