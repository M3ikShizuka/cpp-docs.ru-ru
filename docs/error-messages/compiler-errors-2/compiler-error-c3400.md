---
description: 'Дополнительные сведения о: Ошибка компилятора C3400'
title: Ошибка компилятора C3400
ms.date: 11/04/2016
f1_keywords:
- C3400
helpviewer_keywords:
- C3400
ms.assetid: d44169a8-73b6-4766-b406-b3a6c93f2a4d
ms.openlocfilehash: d2ed88232f88c49f72c868e7b378aa0d6ef30ac3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321959"
---
# <a name="compiler-error-c3400"></a>Ошибка компилятора C3400

циклическая зависимость ограничения, включающая "ограничение_1" и "ограничение_2"

Компилятор обнаружил циклическую зависимость ограничений.

Дополнительные сведения см. в статье [Constraints on Generic Type Parameters (C++/CLI)](../../extensions/constraints-on-generic-type-parameters-cpp-cli.md) (Ограничения, применяемые к параметрам универсальных типов (C++/CLI)).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3400:

```cpp
// C3400.cpp
// compile with: /clr /c
generic<class T, class U>
where T : U
where U : T   // C3400
public ref struct R {};
```
