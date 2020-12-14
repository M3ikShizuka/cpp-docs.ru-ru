---
description: 'Дополнительные сведения о: Ошибка компилятора C3537'
title: Ошибка компилятора C3537
ms.date: 11/04/2016
f1_keywords:
- C3537
helpviewer_keywords:
- C3537
ms.assetid: f537ebd1-4fb0-4e09-a453-4f38db2c6881
ms.openlocfilehash: 84440b757b85a59f87fcca064911136da6cce269
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97315261"
---
# <a name="compiler-error-c3537"></a>Ошибка компилятора C3537

"тип": невозможно привести к типу, содержащему "Auto"

Невозможно привести переменную к указанному типу, так как тип содержит **`auto`** ключевое слово, и действует параметр компилятора [/Zc: Auto](../../build/reference/zc-auto-deduce-variable-type.md) по умолчанию.

## <a name="example"></a>Пример

Следующий код выдает C3537, так как переменные приведены к типу, содержащему **`auto`** ключевое слово.

```cpp
// C3537.cpp
// Compile with /Zc:auto
int main()
{
   int value = 123;
   auto(value);                        // C3537
   (auto)value;                        // C3537
   auto x1 = auto(value);              // C3537
   auto x2 = (auto)value;              // C3537
   auto x3 = static_cast<auto>(value); // C3537
   return 0;
}
```

## <a name="see-also"></a>См. также

[Ключевое слово auto](../../cpp/auto-cpp.md)
