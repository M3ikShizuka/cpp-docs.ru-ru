---
description: Дополнительные сведения см. в статье как указать выходной параметр
title: Практическое руководство. Определение выходного параметра
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- function parameters
- out parameters
ms.assetid: 02862448-603c-4e9d-a5c5-b45fe38446e3
ms.openlocfilehash: b43930557b4bdfd22bf902a6d9adf95eb8ba4d01
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97286342"
---
# <a name="how-to-specify-an-out-parameter"></a>Практическое руководство. Определение выходного параметра

В этом примере показано, как указать, что параметр функции является `out` параметром, и как вызывать эту функцию из программы C#.

`out`Параметр указывается в C++ с помощью <xref:System.Runtime.InteropServices.OutAttribute> .

## <a name="example"></a>Пример

В первой части этого примера создается DLL-библиотека C++. Он определяет тип, содержащий функцию с `out` параметром.

```cpp
// cpp_out_param.cpp
// compile with: /LD /clr
using namespace System;
public value struct TestStruct {
   static void Test([Runtime::InteropServices::Out] String^ %s) {
      s = "a string";
   }
};
```

Этот исходный файл является клиентом C#, использующим компонент C++, созданный в предыдущем примере.

```csharp
// cpp_out_param_2.cs
// compile with: /reference:cpp_out_param.dll
using System;
class TestClass {
   public static void Main() {
      String t;
      TestStruct.Test(out t);
      System.Console.WriteLine(t);
   }
}
```

```Output
a string
```

## <a name="see-also"></a>См. также раздел

[Использование взаимодействия C++ (неявный PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md)
