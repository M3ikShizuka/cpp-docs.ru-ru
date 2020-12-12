---
description: 'Дополнительные сведения см. в статье как: Распаковка'
title: Практическое руководство. Распаковка
ms.date: 11/04/2016
helpviewer_keywords:
- unboxing
ms.assetid: 75794696-9275-47bf-9a7d-5abe6585ab91
ms.openlocfilehash: e5f3ae72f1d7b2340baa868a2e1d009b3534e701
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97286323"
---
# <a name="how-to-unbox"></a>Практическое руководство. Распаковка

Показывает, как распаковать и изменить значение.

## <a name="example"></a>Пример

```cpp
// vcmcppv2_unboxing.cpp
// compile with: /clr
using namespace System;

int main() {
   int ^ i = gcnew int(13);
   int j;
   Console::WriteLine(*i);   // unboxing
   *i = 14;   // unboxing and assignment
   Console::WriteLine(*i);
   j = safe_cast<int>(i);   // unboxing and assignment
   Console::WriteLine(j);
}
```

```Output
13
14
14
```

## <a name="see-also"></a>См. также раздел

[Упаковка-преобразование](../extensions/boxing-cpp-component-extensions.md)
