---
description: Дополнительные сведения см. в статье как загрузить неуправляемые ресурсы в массив байтов.
title: Практическое руководство. Загрузка неуправляемых ресурсов в массив байтов
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- native resources, loading into Byte array
- unmanaged resources, loading into Byte array
- native resources
ms.assetid: cdada6cd-6d42-437a-a90f-44a0b18d6a93
ms.openlocfilehash: e5a7a88a505d3f02b8e9287d6407ddbe77b99dee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97258282"
---
# <a name="how-to-load-unmanaged-resources-into-a-byte-array"></a>Практическое руководство. Загрузка неуправляемых ресурсов в массив байтов

В этом разделе обсуждается несколько способов загрузки неуправляемых ресурсов в <xref:System.Byte> массив.

## <a name="examples"></a>Примеры

Если вы знакомы с размером неуправляемого ресурса, можно предварительно выделить массив CLR, а затем загрузить ресурс в массив с помощью указателя на блок массива в массиве CLR.

```cpp
// load_unmanaged_resources_into_Byte_array.cpp
// compile with: /clr
using namespace System;
void unmanaged_func( unsigned char * p ) {
   for ( int i = 0; i < 10; i++ )
      p[ i ] = i;
}

public ref class A {
public:
   void func() {
      array<Byte> ^b = gcnew array<Byte>(10);
      pin_ptr<Byte> p =  &b[ 0 ];
      Byte * np = p;
      unmanaged_func( np );   // pass pointer to the block of CLR array.
      for ( int i = 0; i < 10; i++ )
         Console::Write( b[ i ] );
      Console::WriteLine();
   }
};

int main() {
   A^ g = gcnew A;
   g->func();
}
```

```Output
0123456789
```

В этом примере показано, как скопировать данные из неуправляемого блока памяти в управляемый массив.

```cpp
// load_unmanaged_resources_into_Byte_array_2.cpp
// compile with: /clr
using namespace System;
using namespace System::Runtime::InteropServices;

#include <string.h>
int main() {
   char buf[] = "Native String";
   int len = strlen(buf);
   array<Byte> ^byteArray = gcnew array<Byte>(len + 2);

   // convert any native pointer to IntPtr by doing C-Style cast
   Marshal::Copy( (IntPtr)buf, byteArray, 0, len );
}
```

## <a name="see-also"></a>См. также раздел

[Использование взаимодействия C++ (неявный PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md)
