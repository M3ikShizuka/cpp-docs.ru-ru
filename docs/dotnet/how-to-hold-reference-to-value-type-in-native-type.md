---
description: Дополнительные сведения см. в статье как хранить ссылку на тип значения в собственном типе.
title: Практическое руководство. Сохранение ссылки на тип значения в собственном типе
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- value type reference in native type
- reference to value type in native type
ms.assetid: 1eabf8be-7d4f-4339-9027-48d5c4244483
ms.openlocfilehash: 4f012b2590b6085e965f3cd1420dbcba4347c84d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97134892"
---
# <a name="how-to-hold-reference-to-value-type-in-native-type"></a>Практическое руководство. Сохранение ссылки на тип значения в собственном типе

Используйте `gcroot` в упакованном типе для хранения ссылки на тип значения в собственном типе.

## <a name="example"></a>Пример

```cpp
// reference_to_value_in_native.cpp
// compile with: /clr
#using <mscorlib.dll>
#include <vcclr.h>

using namespace System;

public value struct V {
   String ^str;
};

class Native {
public:
   gcroot< V^ > v_handle;
};

int main() {
   Native native;
   V v;
   native.v_handle = v;
   native.v_handle->str = "Hello";
   Console::WriteLine("String in V: {0}", native.v_handle->str);
}
```

```Output
String in V: Hello
```

## <a name="see-also"></a>См. также раздел

[Использование взаимодействия C++ (неявный PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md)
