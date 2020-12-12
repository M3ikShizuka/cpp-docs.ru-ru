---
description: 'Дополнительные сведения о: Ошибка компилятора C3073'
title: Ошибка компилятора C3073
ms.date: 11/04/2016
f1_keywords:
- C3073
helpviewer_keywords:
- C3073
ms.assetid: b24b9b8b-f9fb-4c3c-a1a0-97fad2081bfc
ms.openlocfilehash: e26938d6c708c364bb2447b793abf7d51adb5779
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320251"
---
# <a name="compiler-error-c3073"></a>Ошибка компилятора C3073

"тип": класс ссылки не имеет определяемого пользователем конструктора копии

В компиляции [/CLR (компиляция среды CLR)](../../build/reference/clr-common-language-runtime-compilation.md) компилятор не создает конструктор копии для ссылочного типа. При любой компиляции **/CLR** необходимо определить собственный конструктор копии для ссылочного типа, если предполагается копирование экземпляра типа.

Дополнительные сведения см. в разделе [Семантика стека C++ для ссылочных типов](../../dotnet/cpp-stack-semantics-for-reference-types.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3073.

```cpp
// C3073.cpp
// compile with: /clr
ref class R {
public:
   R(int) {}
};

ref class S {
public:
   S(int) {}
   S(const S %rhs) {}   // copy constructor
};

void f(R) {}
void f2(S) {}
void f3(R%){}

int main() {
   R r(1);
   f(r);   // C3073
   f3(r);   // OK

   S s(1);
   f2(s);   // OK
}
```
