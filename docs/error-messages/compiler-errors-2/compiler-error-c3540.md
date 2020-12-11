---
description: 'Дополнительные сведения о: Ошибка компилятора C3540'
title: Ошибка компилятора C3540
ms.date: 11/04/2016
f1_keywords:
- C3540
helpviewer_keywords:
- C3540
ms.assetid: 3c0c959c-e3b7-40eb-b922-ccac44bd9d85
ms.openlocfilehash: 85106061b2631d3a392b05a50c49f24566cdd4cb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97112457"
---
# <a name="compiler-error-c3540"></a>Ошибка компилятора C3540

"тип": sizeof нельзя применить к типу, содержащему "Auto"

Оператор [sizeof](../../cpp/sizeof-operator.md) нельзя применить к указанному типу, так как он содержит **`auto`** спецификатор.

## <a name="example"></a>Пример

В следующем примере выдается C3540.

```cpp
// C3540.cpp
// Compile with /Zc:auto
int main() {
    auto x = 123;
    sizeof(x);    // OK
    sizeof(auto); // C3540
    return 0;
}
```

## <a name="see-also"></a>См. также

[Ключевое слово auto](../../cpp/auto-cpp.md)<br/>
[/Zc: Auto (вывод типа переменной)](../../build/reference/zc-auto-deduce-variable-type.md)<br/>
[Оператор sizeof](../../cpp/sizeof-operator.md)
