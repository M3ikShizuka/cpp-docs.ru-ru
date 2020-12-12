---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4538'
title: Предупреждение компилятора (уровень 3) C4538
ms.date: 11/04/2016
f1_keywords:
- C4538
helpviewer_keywords:
- C4538
ms.assetid: 747e3d51-b6d0-41c1-a726-7af3253b59d7
ms.openlocfilehash: 4f5d6ee8b6144db4fad519f1484d00fe325591a2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257853"
---
# <a name="compiler-warning-level-3-c4538"></a>Предупреждение компилятора (уровень 3) C4538

"тип": квалификаторы Const или volatile для этого типа не поддерживаются

Неправильное применение ключевого слова квалификатора к массиву. Дополнительные сведения см. в описании [array](../../extensions/arrays-cpp-component-extensions.md).

Следующий пример приводит к возникновению ошибки C4538:

```cpp
// C4538.cpp
// compile with: /clr /W3 /LD
const array<int> ^f1();   // C4538
array<const int> ^f2();   // OK
```
