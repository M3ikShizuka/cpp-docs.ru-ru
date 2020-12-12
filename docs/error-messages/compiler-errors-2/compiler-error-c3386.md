---
description: 'Дополнительные сведения о: Ошибка компилятора C3386'
title: Ошибка компилятора C3386
ms.date: 11/04/2016
f1_keywords:
- C3386
helpviewer_keywords:
- C3386
ms.assetid: 93fa8c33-0f10-402b-8eec-b0a217a1f8dc
ms.openlocfilehash: 5bc80abe7c43e30c4114d0f3ffd7733c8ea3e9d1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97115902"
---
# <a name="compiler-error-c3386"></a>Ошибка компилятора C3386

> "*Type-Name*": `__declspec(dllexport)` / `__declspec(dllimport)` не может применяться к типу управляемого или WinRT

[`dllimport`](../../cpp/dllexport-dllimport.md) [`dllexport`](../../cpp/dllexport-dllimport.md) **`__declspec`** Модификаторы и не являются допустимыми для управляемого или среда выполнения Windowsого типа.

В следующем примере показано возникновение ошибки C3386 и приводятся сведения по ее устранению.

```cpp
// C3386.cpp
// compile with: /clr /c
ref class __declspec(dllimport) X1 {   // C3386
// try the following line instead
// ref class X1 {
};
```
