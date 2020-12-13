---
description: 'Дополнительные сведения о: Ошибка компилятора C3298'
title: Ошибка компилятора C3298
ms.date: 11/04/2016
f1_keywords:
- C3298
helpviewer_keywords:
- C3298
ms.assetid: 458c2680-95bb-4d5e-895f-ce4115844193
ms.openlocfilehash: 25b0abc98d5498e59b97f83f47bc0ba12704a328
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97144577"
---
# <a name="compiler-error-c3298"></a>Ошибка компилятора C3298

"ограничение_1": невозможно использовать "ограничение_2" как ограничение, поскольку "ограничение_2" имеет ограничение ссылки, а "ограничение_1" имеет ограничение значения

Нельзя указывать взаимно исключающие характеристики для ограничения. Например, параметр универсального типа не может быть ограничен одновременно типом значения и ссылочным типом.

Дополнительные сведения см. в статье [Constraints on Generic Type Parameters (C++/CLI)](../../extensions/constraints-on-generic-type-parameters-cpp-cli.md) (Ограничения, применяемые к параметрам универсальных типов (C++/CLI)).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3298.

```cpp
// C3298.cpp
// compile with: /clr /c
generic<class T, class U>
where T : ref class
where U : T, value class   // C3298
public ref struct R {};
```
