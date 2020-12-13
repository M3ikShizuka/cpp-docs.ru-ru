---
description: Дополнительные сведения о приведениях в стиле C с помощью/CLR (C++/CLI)
title: Приведение в стиле C с использованием параметра -clr (C++/CLI)
ms.date: 10/12/2018
ms.topic: reference
helpviewer_keywords:
- C-style casts and /clr
ms.assetid: d2a4401a-156a-4da9-8d12-923743e26913
ms.openlocfilehash: aedd794ca0f305f0cc292fb9048bd8dcceace7d0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97176994"
---
# <a name="c-style-casts-with-clr-ccli"></a>Приведение в стиле C с использованием параметра /clr (C++/CLI)

Следующий раздел относится только к среде CLR.

При использовании типов CLR компилятор пытается сопоставить приведение в стиле C с одним из указанных ниже приведений в следующем порядке:

1. const_cast

2. safe_cast

3. safe_cast, а также const_cast

4. static_cast

5. static_cast, а также const_cast

Если ни одно из указанных выше приведений не является допустимым и если тип выражения и целевой тип являются ссылочными типами CLR, приведение в стиле C отображается на проверку во время выполнения (инструкция castclass MSIL). В противном случае приведение в стиле C считается недействительным, и компилятор выдает ошибку.

## <a name="remarks"></a>Комментарии

Приведение в стиле C не рекомендуется. При компиляции с помощью параметра [/CLR (компиляция CLR)](../build/reference/clr-common-language-runtime-compilation.md) необходимо использовать [safe_cast](safe-cast-cpp-component-extensions.md).

В следующем примере показана приведение в стиле C, сопоставленное с **`const_cast`** .

```cpp
// cstyle_casts_1.cpp
// compile with: /clr
using namespace System;

ref struct R {};
int main() {
   const R^ constrefR = gcnew R();
   R^ nonconstR = (R^)(constrefR);
}
```

В следующем примере показано сопоставление приведения типов в стиле C с **safe_cast**.

```cpp
// cstyle_casts_2.cpp
// compile with: /clr
using namespace System;
int main() {
   Object ^ o = "hello";
   String ^ s = (String^)o;
}
```

В следующем примере показана приведение в стиле C, сопоставленное с **safe_cast** и **`const_cast`** .

```cpp
// cstyle_casts_3.cpp
// compile with: /clr
using namespace System;

ref struct R {};
ref struct R2 : public R {};

int main() {
   const R^ constR2 = gcnew R2();
   try {
   R2^ b2DR = (R2^)(constR2);
   }
   catch(InvalidCastException^ e) {
      System::Console::WriteLine("Invalid Exception");
   }
}
```

В следующем примере показана приведение в стиле C, сопоставленное с **`static_cast`** .

```cpp
// cstyle_casts_4.cpp
// compile with: /clr
using namespace System;

struct N1 {};
struct N2 {
   operator N1() {
      return N1();
   }
};

int main() {
   N2 n2;
   N1 n1 ;
   n1 = (N1)n2;
}
```

В следующем примере показана приведение в стиле C, сопоставленное с **`static_cast`** плюсом **`const_cast`** .

```cpp
// cstyle_casts_5.cpp
// compile with: /clr
using namespace System;
struct N1 {};

struct N2 {
   operator const N1*() {
      static const N1 n1;
      return &n1;
   }
};

int main() {
   N2 n2;
   N1* n1 = (N1*)(const N1*)n2;   // const_cast + static_cast
}
```

В следующем примере показано сопоставление приведения типов в стиле C со временем выполнения.

```cpp
// cstyle_casts_6.cpp
// compile with: /clr
using namespace System;

ref class R1 {};
ref class R2 {};

int main() {
   R1^ r  = gcnew R1();
   try {
      R2^ rr = ( R2^)(r);
   }
   catch(System::InvalidCastException^ e) {
      Console::WriteLine("Caught expected exception");
   }
}
```

В следующем примере показано недопустимое приведение типов в стиле C, которое заставляет компилятор выдавать ошибку.

```cpp
// cstyle_casts_7.cpp
// compile with: /clr
using namespace System;
int main() {
   String^s = S"hello";
   int i = (int)s;   // C2440
}
```

## <a name="requirements"></a>Требования

Параметр компилятора: `/clr`

## <a name="see-also"></a>См. также раздел

[Расширения компонентов для .NET и UWP](component-extensions-for-runtime-platforms.md)
