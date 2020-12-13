---
description: 'Дополнительные сведения о: Ошибка компилятора C2860'
title: Ошибка компилятора C2860
ms.date: 11/04/2016
f1_keywords:
- C2860
helpviewer_keywords:
- C2860
ms.assetid: ccc83553-90ed-4e94-b5e9-38b58ae38e31
ms.openlocfilehash: 27474577e31cdc046769f9fc26686d3aaa7f3e64
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97341169"
---
# <a name="compiler-error-c2860"></a>Ошибка компилятора C2860

"void" не может быть типом аргумента, за исключением "(void)"

Тип **`void`** не может использоваться в качестве типа аргумента с другими аргументами.

Следующий пример приводит к возникновению ошибки C2860:

```cpp
// C2860.cpp
// compile with: /c
void profunc1(void, int i);   // C2860
void func10(void);   // OK
```
