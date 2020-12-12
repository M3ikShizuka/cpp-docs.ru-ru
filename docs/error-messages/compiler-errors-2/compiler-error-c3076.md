---
description: 'Дополнительные сведения о: Ошибка компилятора C3076'
title: Ошибка компилятора C3076
ms.date: 11/04/2016
f1_keywords:
- C3076
helpviewer_keywords:
- C3076
ms.assetid: 8a87b3e4-2c17-4b87-9622-ef0962d6a34e
ms.openlocfilehash: 27fbfe27d2e8efb1abee611701fdbde8f0d3d09f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320184"
---
# <a name="compiler-error-c3076"></a>Ошибка компилятора C3076

"экземпляр": невозможно внедрить экземпляр ссылочного типа "тип" в собственный тип

Собственный тип не может содержать экземпляр типа CLR.

Дополнительные сведения см. в разделе [Семантика стека C++ для ссылочных типов](../../dotnet/cpp-stack-semantics-for-reference-types.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3076.

```cpp
// C3076.cpp
// compile with: /clr /c
ref struct U {};

struct V {
   U y;   // C3076
};

ref struct W {
   U y;   // OK
};
```
