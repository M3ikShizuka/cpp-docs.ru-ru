---
description: Дополнительные сведения см. в статье как использовать собственный тип в компиляции/CLR.
title: Как использовать собственный тип в компиляции в среде CLR
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- compilation, native types in /clr
- /clr compiler option [C++], using native types
ms.assetid: 3a505c90-4adb-4942-9cf9-7d1fdcbc01e7
ms.openlocfilehash: 8e8479bb64166faec841d9d69ce38b3e8e57e048
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97286284"
---
# <a name="how-to-use-a-native-type-in-a-clr-compilation"></a>Практическое руководство. Использование собственного типа в компиляции /clr

Можно определить собственный тип в компиляции **/CLR** , и любое использование этого собственного типа из сборки является допустимым. Однако собственные типы не будут доступны для использования в метаданных, на которые имеются ссылки.

Каждая сборка должна содержать определение каждого собственного типа, который будет использоваться.

Дополнительные сведения см. в разделе [/CLR (компиляция среды CLR)](../build/reference/clr-common-language-runtime-compilation.md).

## <a name="examples"></a>Примеры

В этом примере создается компонент, который определяет и использует собственный тип.

```cpp
// use_native_type_in_clr.cpp
// compile with: /clr /LD
public struct NativeClass {
   static int Test() { return 98; }
};

public ref struct ManagedClass {
   static int i = NativeClass::Test();
   void Test() {
      System::Console::WriteLine(i);
   }
};
```

В этом примере определяется клиент, использующий компонент. Обратите внимание, что при доступе к собственному типу возникает ошибка, если он не определен в компилируемого объекта.

```cpp
// use_native_type_in_clr_2.cpp
// compile with: /clr
#using "use_native_type_in_clr.dll"
// Uncomment the following 3 lines to resolve.
// public struct NativeClass {
//    static int Test() { return 98; }
// };

int main() {
   ManagedClass x;
   x.Test();

   System::Console::WriteLine(NativeClass::Test());   // C2653
}
```

## <a name="see-also"></a>См. также раздел

[Использование взаимодействия C++ (неявный PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md)
