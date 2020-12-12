---
description: 'Дополнительные сведения о: Ошибка компилятора C2013'
title: Ошибка компилятора C2013
ms.date: 11/04/2016
f1_keywords:
- C2013
helpviewer_keywords:
- C2013
ms.assetid: 6b5c955c-53da-48ee-8533-64ef5b905173
ms.openlocfilehash: 2f883c24be5e02c58553ca6f7abe4f588ae8a2da
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97220972"
---
# <a name="compiler-error-c2013"></a>Ошибка компилятора C2013

отсутствует ">"

В директиве `#include` отсутствует закрывающая угловая скобка. Чтобы устранить эту ошибку, добавьте закрывающую скобку.

Следующий пример приводит к возникновению ошибки C2013:

```cpp
// C2013.cpp
#include <stdio.h    // C2013
```

Возможное решение:

```cpp
// C2013b.cpp
// compile with: /c
#include <stdio.h>
```
