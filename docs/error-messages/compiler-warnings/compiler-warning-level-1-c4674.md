---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4674'
title: Предупреждение компилятора (уровень 1) C4674
ms.date: 11/04/2016
f1_keywords:
- C4674
helpviewer_keywords:
- C4674
ms.assetid: 638dae0b-b82c-4865-9599-72630827ca09
ms.openlocfilehash: 1df7dd982f52a6987e06e888130953c1a9deb330
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334974"
---
# <a name="compiler-warning-level-1-c4674"></a>Предупреждение компилятора (уровень 1) C4674

"метод": требуется объявление как "static" и наличие строго одного параметра

Неправильная сигнатура оператора преобразования. Метод не считается пользовательским преобразованием. Дополнительные сведения об определении операторов см. в разделе [определяемые пользователем операторы (c++/CLI)](../../dotnet/user-defined-operators-cpp-cli.md) и пользовательские [преобразования (c++/CLI)](../../dotnet/user-defined-conversions-cpp-cli.md).

## <a name="example"></a>Пример

При компиляции следующего примера будет выдано предупреждение C4674.

```cpp
// C4674.cpp
// compile with: /clr /WX /W1 /LD
ref class G {
   int op_Implicit(int i) {   // C4674
      return 0;
   }
};
```
