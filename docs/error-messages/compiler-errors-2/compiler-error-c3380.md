---
description: 'Дополнительные сведения о: Ошибка компилятора C3380'
title: Ошибка компилятора C3380
ms.date: 11/04/2016
f1_keywords:
- C3380
helpviewer_keywords:
- C3380
ms.assetid: 86f1f4ec-4ad8-4a1a-9b6c-2d9b6129df6b
ms.openlocfilehash: bb633d75d08fdbb902f086b3a4cd6a8a6db1fc69
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334987"
---
# <a name="compiler-error-c3380"></a>Ошибка компилятора C3380

"класс": недопустимый спецификатор уровня доступа сборки — разрешены только "public" или "private"

Ключевые слова [public](../../cpp/public-cpp.md) и [private](../../cpp/private-cpp.md) , применяемые к управляемым классам или структурам, определяют возможность предоставления класса посредством метаданных сборки. К классам программы, компилируемой с использованием параметра `public` /clr `private` , могут применяться только ключевые слова [и](../../build/reference/clr-common-language-runtime-compilation.md).

`ref` `value` Ключевые слова и при использовании с [параметром/CLR](../../build/reference/clr-common-language-runtime-compilation.md)указывают на то, что класс является управляемым (см. раздел [классы и структуры](../../extensions/classes-and-structs-cpp-component-extensions.md)).

Следующий пример приводит к возникновению ошибки C3380:

```cpp
// C3380_2.cpp
// compile with: /clr
protected ref class A {   // C3380
// try the following line instead
// ref class A {
public:
   static int i = 9;
};

int main() {
   A^ myA = gcnew A;
   System::Console::WriteLine(myA->i);
}
```
