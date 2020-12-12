---
description: 'Дополнительные сведения о: Ошибка компилятора C2346'
title: Ошибка компилятора C2346
ms.date: 11/04/2016
f1_keywords:
- C2346
helpviewer_keywords:
- C2346
ms.assetid: 246145be-5645-4cd6-867c-e3bc39e33dca
ms.openlocfilehash: eb2bbda6c7f7e0c9213b35a794b915967d03321f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298374"
---
# <a name="compiler-error-c2346"></a>Ошибка компилятора C2346

"функция" не может быть скомпилирована как собственная: причина

Компилятору не удалось скомпилировать функцию в MSIL.

Дополнительные сведения см. в разделе [управляемые, неуправляемые](../../preprocessor/managed-unmanaged.md) и [/CLR (компиляция общеязыковой среды выполнения)](../../build/reference/clr-common-language-runtime-compilation.md).

### <a name="to-correct-this-error"></a>Исправление ошибки

1. Удалите код в функции, которая не может быть скомпилирована в MSIL.

1. Либо не компилируйте модуль с помощью **параметра/clr**, либо пометьте функцию как неуправляемую с помощью неуправляемой директивы pragma.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2346.

```cpp
// C2346.cpp
// processor: x86
// compile with: /clr
// C2346 expected
struct S
{
   S()
   {
      { __asm { nop } }
   }
   virtual __clrcall ~S() { }
};

int main()
{
   S s;
}
```
