---
description: 'Дополнительные сведения о: Ошибка компилятора C3363'
title: Ошибка компилятора C3363
ms.date: 11/04/2016
f1_keywords:
- C3363
helpviewer_keywords:
- C3363
ms.assetid: 41aa922f-608e-4f7a-ba66-451fc1161935
ms.openlocfilehash: b746a4c1e220ee05f96f3f2ceae524d5747550d7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335033"
---
# <a name="compiler-error-c3363"></a>Ошибка компилятора C3363

"тип": typeid можно применять только к типу

Неправильно использован оператор [typeid](../../extensions/typeid-cpp-component-extensions.md) .

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3363:

```cpp
// C3363.cpp
// compile with: /clr
int main() {
   System::typeid;   // C3363
}
```
