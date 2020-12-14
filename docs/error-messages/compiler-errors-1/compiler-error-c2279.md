---
description: 'Дополнительные сведения о: Ошибка компилятора C2279'
title: Ошибка компилятора C2279
ms.date: 11/04/2016
f1_keywords:
- C2279
helpviewer_keywords:
- C2279
ms.assetid: 1b5c88ef-2336-49b8-9ddb-d61f97c73e14
ms.openlocfilehash: e0f8822c77bd243bc2ec6002027d8eadb2aaf8a0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97228980"
---
# <a name="compiler-error-c2279"></a>Ошибка компилятора C2279

спецификация исключения не может присутствовать в объявлении typedef

В параметре **/Za** [спецификации исключений](../../cpp/exception-specifications-throw-cpp.md) не допускаются в объявлении typedef.

Следующий пример приводит к возникновению ошибки C2279:

```cpp
// C2279.cpp
// compile with: /Za /c
typedef int (*xy)() throw(...);   // C2279
typedef int (*xyz)();   // OK
```
