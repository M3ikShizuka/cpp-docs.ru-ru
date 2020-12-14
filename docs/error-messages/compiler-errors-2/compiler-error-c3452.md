---
description: 'Дополнительные сведения о: Ошибка компилятора C3452'
title: Ошибка компилятора C3452
ms.date: 11/04/2016
f1_keywords:
- C3452
helpviewer_keywords:
- C3452
ms.assetid: e5293dcf-cb70-4133-ae2a-0bb496950ba0
ms.openlocfilehash: 7153088ccd132112f47823cd1eb1147480615fc5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97315990"
---
# <a name="compiler-error-c3452"></a>Ошибка компилятора C3452

член аргумента списка не является константой

Аргумент передан в атрибут, ожидающий константу, значение которого можно вычислить во время компиляции.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3452:

```cpp
// C3452.cpp
// compile with: /c
int i;
[module( name="mod", type=dll, custom={i} ) ];   // C3452
// try the following line instead
// [module( name="mod", type=dll, custom={"a"} ) ];
```
