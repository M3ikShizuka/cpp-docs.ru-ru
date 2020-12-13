---
description: 'Дополнительные сведения о: Ошибка компилятора C3286'
title: Ошибка компилятора C3286
ms.date: 11/04/2016
f1_keywords:
- C3286
helpviewer_keywords:
- C3286
ms.assetid: 554328c8-cf44-4f7d-a8d2-def74d28ecdd
ms.openlocfilehash: 38e3b405f9093baa266cf56e5bfc7f44c7566206
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339226"
---
# <a name="compiler-error-c3286"></a>Ошибка компилятора C3286

> "*спецификатор*": переменная итерации не может содержать спецификаторы класса хранения

Класс хранения не может быть указан в переменной итерации. Дополнительные сведения см. в разделе [классы хранения (C++)](../../cpp/storage-classes-cpp.md) и [для каждого, в](../../dotnet/for-each-in.md).

## <a name="example"></a>Пример

В следующем примере создается C3286, а также показывается правильное использование.

```cpp
// C3286.cpp
// compile with: /clr
int main() {
   array<int> ^p = { 1, 2, 3 };
   for each (static int i in p) {}   // C3286
   for each (int j in p) {}   // OK
}
```
