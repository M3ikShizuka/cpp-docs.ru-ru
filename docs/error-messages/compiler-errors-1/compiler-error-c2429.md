---
description: 'Дополнительные сведения о: Ошибка компилятора C2429'
title: Ошибка компилятора C2429
ms.date: 11/16/2017
f1_keywords:
- C2429
helpviewer_keywords:
- C2429
ms.assetid: 57ff6df9-5cf1-49f3-8bd8-4e550dfd65a0
ms.openlocfilehash: 3c16a2a430e8050103c3903cf1355de089252ed5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190137"
---
# <a name="compiler-error-c2429"></a>Ошибка компилятора C2429

> "*компонент языка*" требует флаг компилятора "*параметр компилятора*"

Функция языка требует наличия определенного параметра компилятора для поддержки.

Ошибка **C2429: функция языка "Nested-Namespace-Definition" требует наличия флага компилятора "/std: c++ 17"** при попытке определить *составное пространство* имен, которое содержит одно или несколько имен вложенных пространств имен, начиная с Visual Studio 2015 с обновлением 5. (В Visual Studio 2017 версии 15,3 требуется параметр **/std: c + + Latest** .) Определения составных пространств имен не допускаются в C++ до C++ 17. Компилятор поддерживает определения составных пространств имен, если указан параметр компилятора [/std: c++ 17](../../build/reference/std-specify-language-standard-version.md) :

```cpp
// C2429a.cpp
namespace a::b { int i; } // C2429 starting in Visual Studio 2015 Update 3.
                          // Use /std:c++17 to fix, or do this:
// namespace a { namespace b { int i; }}

int main() {
   a::b::i = 2;
}
```
