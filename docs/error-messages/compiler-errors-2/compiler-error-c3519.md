---
description: 'Дополнительные сведения о: Ошибка компилятора C3519'
title: Ошибка компилятора C3519
ms.date: 11/04/2016
f1_keywords:
- C3519
helpviewer_keywords:
- C3519
ms.assetid: ca24b2bc-7e90-4448-ae84-3fedddf9bca7
ms.openlocfilehash: f8eb90620894627beab450275c6725d665d837e4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97113095"
---
# <a name="compiler-error-c3519"></a>Ошибка компилятора C3519

"invalid_param": недопустимый параметр для embedded_idl атрибута

Параметр был передан `embedded_idl` атрибуту [#import](../../preprocessor/hash-import-directive-cpp.md), но компилятор не распознал параметр.

Единственными допустимыми параметрами для `embedded_idl` являются `emitidl` и `no_emitidl` .

Следующий пример приводит к возникновению ошибки C3519:

```cpp
// C3519.cpp
// compile with: /LD
[module(name="MyLib2")];
#import "C:\testdir\bin\importlib.tlb" embedded_idl("no_emitidcl")
// C3519
#import "C:\testdir\bin\importlib.tlb" embedded_idl("no_emitidl")
// OK
```
