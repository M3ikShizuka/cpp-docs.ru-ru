---
description: 'Дополнительные сведения о: Ошибка компилятора C2937'
title: Ошибка компилятора C2937
ms.date: 11/04/2016
f1_keywords:
- C2937
helpviewer_keywords:
- C2937
ms.assetid: 95671ca3-79f7-4b56-a5f2-a92296da1629
ms.openlocfilehash: af73e4564293fdcd5b69cc2f1890cb3e5364c618
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323055"
---
# <a name="compiler-error-c2937"></a>Ошибка компилятора C2937

"класс": идентификатор класса типа переопределен как глобальное определение типа (typedef)

Универсальный шаблон или класс шаблона нельзя использовать в качестве глобального **`typedef`** .

Следующий пример приводит к возникновению ошибки C2937:

```cpp
// C2937.cpp
// compile with: /c
template<class T>
struct TC { };
typedef int TC<int>;   // C2937
typedef TC<int> c;   // OK
```

Ошибка C2937 также может возникнуть при использовании универсальных шаблонов.

```cpp
// C2937b.cpp
// compile with: /clr
generic<class T>
ref struct GC { };
typedef int GC<int>;   // C2937
typedef GC<int> xx;   // OK
```
