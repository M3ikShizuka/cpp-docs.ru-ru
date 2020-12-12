---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4645'
title: Предупреждение компилятора (уровень 3) C4645
ms.date: 11/04/2016
f1_keywords:
- C4645
helpviewer_keywords:
- C4645
ms.assetid: fd7c1ddf-f0d0-4e10-bab9-ccb4c3476298
ms.openlocfilehash: 1002abfa66eddbf4891f9d57af96bf0b949cd483
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97305303"
---
# <a name="compiler-warning-level-3-c4645"></a>Предупреждение компилятора (уровень 3) C4645

функция, объявленная с атрибутом __declspec(noreturn) имеет оператор return

В функции, помеченной модификатором " [noreturn](../../cpp/noreturn.md) ", обнаружена инструкция [return](../../cpp/program-termination.md) **`__declspec`** . **`return`** Инструкция была пропущена.

Следующий пример приводит к возникновению ошибки C4645.

```cpp
// C4645.cpp
// compile with:  /W3
void __declspec(noreturn) func() {
   return;   // C4645, delete this line to resolve
}

int main() {
}
```
