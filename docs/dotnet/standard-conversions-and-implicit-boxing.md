---
description: 'Дополнительные сведения: стандартные преобразования и неявная упаковка-преобразование'
title: Стандартные преобразования и неявная упаковка-преобразование
ms.date: 11/04/2016
helpviewer_keywords:
- boxing, implicit
ms.assetid: 33f7fc7d-5674-44a2-a859-0e6a04fae519
ms.openlocfilehash: 9775effdae92ac9689bc7c08f2ba7887e6b54dbc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335352"
---
# <a name="standard-conversions-and-implicit-boxing"></a>Стандартные преобразования и неявная упаковка-преобразование

Компилятор будет выбирать стандартное преобразование для преобразования, для которого требуется упаковка-преобразование.

## <a name="example"></a>Пример

```cpp
// clr_implicit_boxing_Std_conversion.cpp
// compile with: /clr
int f3(int ^ i) {   // requires boxing
   return 1;
}

int f3(char c) {   // no boxing required, standard conversion
   return 2;
}

int main() {
   int i = 5;
   System::Console::WriteLine(f3(i));
}
```

```Output
2
```

## <a name="see-also"></a>См. также раздел

[Упаковка-преобразование](../extensions/boxing-cpp-component-extensions.md)
