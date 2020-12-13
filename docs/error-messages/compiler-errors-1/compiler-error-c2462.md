---
description: 'Дополнительные сведения о: Ошибка компилятора C2462'
title: Ошибка компилятора C2462
ms.date: 11/04/2016
f1_keywords:
- C2462
helpviewer_keywords:
- C2462
ms.assetid: a8601bf8-f5ce-41de-9117-e2632bd4996b
ms.openlocfilehash: f85d8f2e38c38043765b29b6e766c0cbd4fef1fd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97341819"
---
# <a name="compiler-error-c2462"></a>Ошибка компилятора C2462

"идентификатор": невозможно определить тип в "New-Expression"

Нельзя определить тип в поле операнда **`new`** оператора. Помещайте определение типа в отдельную инструкцию.

Следующий пример приводит к возникновению ошибки C2462:

```cpp
// C2462.cpp
int main() {
   new struct S { int i; };   // C2462
}
```
