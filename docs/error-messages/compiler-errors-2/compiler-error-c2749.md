---
description: 'Дополнительные сведения о: Ошибка компилятора C2749'
title: Ошибка компилятора C2749
ms.date: 11/04/2016
f1_keywords:
- C2749
helpviewer_keywords:
- C2749
ms.assetid: a81aef36-cdca-4d78-89d5-b72eff2500b2
ms.openlocfilehash: 582bc035411c8ee77684f89ca841260a4391340a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97122893"
---
# <a name="compiler-error-c2749"></a>Ошибка компилятора C2749

"тип": может создавать или перехватывать только обработчики для управляемого класса с/CLR: Сейф

При использовании **/clr: Сейф** можно создать только ссылочный тип или перехватить его.

Дополнительные сведения см. в разделе [/CLR (компиляция среды CLR)](../../build/reference/clr-common-language-runtime-compilation.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2749:

```cpp
// C2749.cpp
// compile with: /clr:safe
ref struct MyStruct {
public:
   int i;
};

int main() {
   MyStruct ^x = gcnew MyStruct;

   // Delete the following 4 lines to resolve.
   try {
      throw (1);   // C2749
   }
   catch(int){}

   // OK
   try {
      throw (x);
   }
   catch(MyStruct ^){}
}
```
