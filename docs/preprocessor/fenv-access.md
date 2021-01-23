---
title: fenv_access pragma
description: Описывает использование и эффекты pragma директивы fenv_access. Директива fenv_access управляет доступом к среде с плавающей запятой во время выполнения.
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.fenv_access
- fenv_access_CPP
helpviewer_keywords:
- pragma, fenv_access
- fenv_access pragma
no-loc:
- pragma
ms.openlocfilehash: be33bbf9de381850ec78ece204d117ebc537152b
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713666"
---
# <a name="fenv_access-no-locpragma"></a>`fenv_access` pragma

Отключает ( **`on`** ) или включает ( **`off`** ) оптимизацию, которая может изменить проверки флагов среды с плавающей точкой и изменения режима.

## <a name="syntax"></a>Синтаксис

> **`#pragma fenv_access (`** { **`on`** | **`off`** } **`)`**

## <a name="remarks"></a>Примечания

По умолчанию **`fenv_access`** имеет значение **`off`** . Компилятор предполагает, что ваш код не обращается к среде с плавающей запятой или не управляет ею. Если доступ к среде не требуется, компилятор может повысить эффективность кода с плавающей точкой.

Включить **`fenv_access`** , если ваш код проверяет флаги состояния с плавающей точкой, исключения или задает флаги режима управления. Компилятор отключает оптимизацию операций с плавающей запятой, поэтому код может постоянно обращаться к среде с плавающей запятой.

Параметр командной строки [/FP: Option] включается автоматически **`fenv_access`** . Дополнительные сведения об этом и других воздействиех с плавающей запятой см. в разделе [/FP (определение поведения Floating-Point)](../build/reference/fp-specify-floating-point-behavior.md).

Существуют ограничения на способы использования **`fenv_access`** pragma в сочетании с другими параметрами с плавающей запятой.

- Невозможно включить, **`fenv_access`** если не включена точная семантика. Точная семантика может быть включена либо параметром [`float_control`](float-control.md) pragma , либо с помощью [`/fp:precise`](../build/reference/fp-specify-floating-point-behavior.md) [`/fp:strict`](../build/reference/fp-specify-floating-point-behavior.md) параметров компилятора или. Компилятор по умолчанию принимает значение, **`/fp:precise`** если не указан другой параметр командной строки с плавающей запятой.

- Нельзя использовать **`float_control`** для отключения точной семантики, если **`fenv_access(on)`** задан параметр.

**`fenv_access`** Существуют следующие виды оптимизации:

- Глобальное исключение общей части выражения

- Перемещение кода

- Свертывание констант

Другие директивы с плавающей запятой pragma включают:

- [float_control](../preprocessor/float-control.md)

- [fp_contract](../preprocessor/fp-contract.md)

## <a name="examples"></a>Примеры

В этом примере задается значение для **`fenv_access`** **`on`** задания контрольного регистра с плавающей запятой для 24-разрядной точности:

```cpp
// pragma_directive_fenv_access_x86.cpp
// compile with: /O2 /arch:IA32
// processor: x86
#include <stdio.h>
#include <float.h>
#include <errno.h>
#pragma fenv_access (on)

int main() {
   double z, b = 0.1, t = 0.1;
   unsigned int currentControl;
   errno_t err;

   err = _controlfp_s(&currentControl, _PC_24, _MCW_PC);
   if (err != 0) {
      printf_s("The function _controlfp_s failed!\n");
      return -1;
   }
   z = b * t;
   printf_s ("out=%.15e\n",z);
}
```

```Output
out=9.999999776482582e-03
```

Если закомментировать `#pragma fenv_access (on)` предыдущий пример, выходные данные будут отличаться. Это обусловлено тем, что компилятор выполняет вычисление во время компиляции, которое не использует режим управления.

```cpp
// pragma_directive_fenv_access_2.cpp
// compile with: /O2 /arch:IA32
#include <stdio.h>
#include <float.h>

int main() {
   double z, b = 0.1, t = 0.1;
   unsigned int currentControl;
   errno_t err;

   err = _controlfp_s(&currentControl, _PC_24, _MCW_PC);
   if (err != 0) {
      printf_s("The function _controlfp_s failed!\n");
      return -1;
   }
   z = b * t;
   printf_s ("out=%.15e\n",z);
}
```

```Output
out=1.000000000000000e-02
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
