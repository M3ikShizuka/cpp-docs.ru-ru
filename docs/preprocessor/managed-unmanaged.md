---
description: Дополнительные сведения об управляемых и неуправляемых pragma директивах в Microsoft C++
title: управляемый и неуправляемый pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.unmanaged
- managed_CPP
- unmanaged_CPP
- vc-pragma.managed
helpviewer_keywords:
- managed pragma
- pragma, unmanaged
- pragma, managed
- unmanaged pragma
no-loc:
- pragma
ms.openlocfilehash: a106e9a1370daeedb94bbf5e4d092ae85457a3d2
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713510"
---
# <a name="managed-and-unmanaged-no-locpragma"></a>`managed` и `unmanaged` pragma

Включите управление на уровне функций для компиляции функций как управляемых или неуправляемых.

## <a name="syntax"></a>Синтаксис

> **`#pragma managed`**\
> **`#pragma unmanaged`**\
> **`#pragma managed(`** [ **`push,`** ] { **`on`** | **`off`** } **`)`**\
> **`#pragma managed(pop)`**

## <a name="remarks"></a>Примечания

[`/clr`](../build/reference/clr-common-language-runtime-compilation.md)Параметр компилятора обеспечивает управление на уровне модуля для компиляции функций как управляемых, так и неуправляемых.

Неуправляемая функция компилируется для собственной платформы. Выполнение этой части программы будет передано в собственную платформу средой CLR.

Функции компилируются как управляемые по умолчанию при **`/clr`** использовании.

При применении **`managed`** или **`unmanaged`** pragma :

- Добавьте pragma предшествующую функцию, но не внутри тела функции.

- Добавьте pragma Операторы after `#include` . Не используйте его перед любыми `#include` инструкциями.

Компилятор игнорирует **`managed`** и, **`unmanaged`** pragma Если **`/clr`** не используется при компиляции.

При создании экземпляра функции-шаблона pragma состояние, когда определяется шаблон, определяет, является ли он управляемым или неуправляемым.

Дополнительные сведения см. в разделе [Инициализация смешанных сборок](../dotnet/initialization-of-mixed-assemblies.md).

## <a name="example"></a>Пример

```cpp
// pragma_directives_managed_unmanaged.cpp
// compile with: /clr
#include <stdio.h>

// func1 is managed
void func1() {
   System::Console::WriteLine("In managed function.");
}

// #pragma unmanaged
// push managed state on to stack and set unmanaged state
#pragma managed(push, off)

// func2 is unmanaged
void func2() {
   printf("In unmanaged function.\n");
}

// #pragma managed
#pragma managed(pop)

// main is managed
int main() {
   func1();
   func2();
}
```

```Output
In managed function.
In unmanaged function.
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
