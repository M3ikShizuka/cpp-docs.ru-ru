---
description: 'Дополнительные сведения о: Ошибка компилятора C3541'
title: Ошибка компилятора C3541
ms.date: 11/04/2016
f1_keywords:
- C3541
helpviewer_keywords:
- C3541
ms.assetid: 252cfd4c-5fd2-415e-a17d-6b0c254350db
ms.openlocfilehash: b579697de98556aa99077e43d28e6de828741fb5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97315170"
---
# <a name="compiler-error-c3541"></a>Ошибка компилятора C3541

"тип": typeid нельзя применять к типу, содержащему "Auto"

Оператор [typeid](../../extensions/typeid-cpp-component-extensions.md) не может применяться к указанному типу, так как он содержит **`auto`** спецификатор.

## <a name="example"></a>Пример

В следующем примере выдается C3541.

```cpp
// C3541.cpp
// Compile with /Zc:auto
#include <typeinfo>
int main() {
    auto x = 123;
    typeid(x);    // OK
    typeid(auto); // C3541
    return 0;
}
```

## <a name="see-also"></a>См. также

[Ключевое слово auto](../../cpp/auto-cpp.md)<br/>
[/Zc: Auto (вывод типа переменной)](../../build/reference/zc-auto-deduce-variable-type.md)<br/>
[типа](../../extensions/typeid-cpp-component-extensions.md)
