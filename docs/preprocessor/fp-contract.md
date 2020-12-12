---
description: 'Дополнительные сведения о: fp_contract pragma'
title: Прагма fp_contract
ms.date: 08/29/2019
f1_keywords:
- vc-pragma.fp_contract
- fp_contract_CPP
helpviewer_keywords:
- pragmas, fp_contract
- fp_contract pragma
ms.assetid: 15b97338-6680-4287-ba2a-2dccc5b2ccf5
ms.openlocfilehash: cefcf0519f08b3fd68a0f8b464938ea7cdbda6d0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97261181"
---
# <a name="fp_contract-pragma"></a>Прагма fp_contract

Определяет, выполняется ли контракт с плавающей точкой. Контракт с плавающей запятой — это инструкция, такая как FMA (предохранитель-умножение), которая объединяет две отдельные операции с плавающей точкой в одну инструкцию. Использование этих инструкций может повлиять на точность чисел с плавающей запятой, поскольку вместо округления после каждой операции процессор может округлять только один раз после обеих операций.

## <a name="syntax"></a>Синтаксис

> **fp_contract #pragma (** { **On**  |  **Off** } **)**

## <a name="remarks"></a>Комментарии

По умолчанию **fp_contract** имеет значение **On**. Это указывает компилятору использовать инструкции по контракту с плавающей запятой, где это возможно. Задайте для параметра **fp_contract** значение **Off** , чтобы сохранить отдельные инструкции с плавающей запятой.

Дополнительные сведения о поведении чисел с плавающей запятой см. в разделе [/FP (определение поведения Floating-Point)](../build/reference/fp-specify-floating-point-behavior.md).

Другие типы директив pragma для значений с плавающей запятой:

- [fenv_access](../preprocessor/fenv-access.md)

- [float_control](../preprocessor/float-control.md)

## <a name="example"></a>Пример

Код, созданный в этом примере, не использует инструкцию-умножение с предохранителем, даже если она доступна на целевом процессоре. Если вы закомментируем комментарий `#pragma fp_contract (off)` , в созданном коде может использоваться инструкция с предохранителем-умножение, если она доступна.

```cpp
// pragma_directive_fp_contract.cpp
// on x86 and x64 compile with: /O2 /fp:fast /arch:AVX2
// other platforms compile with: /O2

#include <stdio.h>

// remove the following line to enable FP contractions
#pragma fp_contract (off)

int main() {
   double z, b, t;

   for (int i = 0; i < 10; i++) {
      b = i * 5.5;
      t = i * 56.025;

      z = t * i + b;
      printf("out = %.15e\n", z);
   }
}
```

```Output
out = 0.000000000000000e+00
out = 6.152500000000000e+01
out = 2.351000000000000e+02
out = 5.207249999999999e+02
out = 9.184000000000000e+02
out = 1.428125000000000e+03
out = 2.049900000000000e+03
out = 2.783725000000000e+03
out = 3.629600000000000e+03
out = 4.587525000000000e+03
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и ключевое слово __pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)
