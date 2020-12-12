---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1306'
title: Ошибка средств компоновщика LNK1306
ms.date: 11/04/2016
f1_keywords:
- LNK1306
helpviewer_keywords:
- LNK1306
ms.assetid: fad1df6a-0bd9-412f-b0d1-7c9bc749c584
ms.openlocfilehash: aa6386da7c836eea8365d8a4ffde0bbd80d0fa81
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193660"
---
# <a name="linker-tools-error-lnk1306"></a>Ошибка средств компоновщика LNK1306

> Функция точки входа DLL не может быть управляемой; компилировать в машинный код

`DllMain` невозможно скомпилировать в MSIL; Он должен быть скомпилирован в машинный код.

Чтобы устранить эту проблему,

- Скомпилируйте файл, содержащий точку входа, без **/CLR**.

- Поместите точку входа в `#pragma unmanaged` раздел.

Дополнительные сведения см. в разделе:

- [/clr (компиляция среды выполнения)](../../build/reference/clr-common-language-runtime-compilation.md)

- [managed, unmanaged](../../preprocessor/managed-unmanaged.md)

- [Инициализация смешанных сборок](../../dotnet/initialization-of-mixed-assemblies.md)

- [Библиотеки DLL и поведение библиотеки времени выполнения Visual C++](../../build/run-time-library-behavior.md)

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки LNK1306.

```cpp
// LNK1306.cpp
// compile with: /clr /link /dll /entry:NewDllMain
// LNK1306 error expected
#include <windows.h>
int __stdcall NewDllMain( HINSTANCE h, ULONG ulReason, PVOID pvReserved ) {
   return 1;
}
```

Чтобы устранить эту проблему, не используйте параметр/CLR для компиляции этого файла или используйте `#pragma` директиву, чтобы разместить определение точки входа в неуправляемом разделе, как показано в следующем примере:

```cpp
// LNK1306fix.cpp
// compile with: /clr /link /dll /entry:NewDllMain
#include <windows.h>
#pragma managed(push, off)
int __stdcall NewDllMain( HINSTANCE h, ULONG ulReason, PVOID pvReserved ) {
   return 1;
}
#pragma managed(pop)
```
