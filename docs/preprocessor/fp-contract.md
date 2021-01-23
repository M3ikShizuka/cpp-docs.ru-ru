---
description: Дополнительные сведения об pragma директиве fp_contract в Microsoft C/C++
title: fp_contract pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.fp_contract
- fp_contract_CPP
helpviewer_keywords:
- pragma, fp_contract
- fp_contract pragma
no-loc:
- pragma
ms.openlocfilehash: 3263d1ec9675e0f8a9402ac7da78751b988e7bdf
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713653"
---
# <a name="fp_contract-no-locpragma"></a>`fp_contract` pragma

Определяет, выполняется ли контракт с плавающей точкой. Контракт с плавающей запятой — это инструкция, такая как FMA (предохранитель-умножение), которая объединяет две отдельные операции с плавающей точкой в одну инструкцию. Использование этих инструкций может повлиять на точность чисел с плавающей запятой, поскольку вместо округления после каждой операции процессор может округлять только один раз после обеих операций.

## <a name="syntax"></a>Синтаксис

> **`#pragma fp_contract (`** { **`on`** | **`off`** } **`)`**

## <a name="remarks"></a>Примечания

По умолчанию **`fp_contract`** имеет значение **`on`** . Это указывает компилятору использовать инструкции по контракту с плавающей запятой, где это возможно. Задайте для значение **`fp_contract`** **`off`** , чтобы сохранить отдельные инструкции с плавающей запятой.

Дополнительные сведения о поведении чисел с плавающей запятой см. в разделе [ `/fp` (определение поведения с плавающей запятой)](../build/reference/fp-specify-floating-point-behavior.md).

Другие директивы с плавающей запятой pragma включают:

- [`fenv_access`](../preprocessor/fenv-access.md)

- [`float_control`](../preprocessor/float-control.md)

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

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
