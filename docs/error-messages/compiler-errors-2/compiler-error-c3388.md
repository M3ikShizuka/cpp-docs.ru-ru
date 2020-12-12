---
description: 'Дополнительные сведения о: Ошибка компилятора C3388'
title: Ошибка компилятора C3388
ms.date: 11/04/2016
f1_keywords:
- C3388
helpviewer_keywords:
- C3388
ms.assetid: 34336545-ed13-4d81-ab5f-f869799fe4c2
ms.openlocfilehash: 0acc4729b5b6de61476bc134b9ef7f79bb9e86e2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97285530"
---
# <a name="compiler-error-c3388"></a>Ошибка компилятора C3388

"тип": не допускается в качестве ограничения; предполагается, что "класс ref" продолжит синтаксический разбор

Ограничение для универсального типа указано неправильно. Дополнительные сведения см. [в разделе ограничения для параметров универсального типа (C++/CLI)](../../extensions/constraints-on-generic-type-parameters-cpp-cli.md) .

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3388:

```cpp
// C3388.cpp
// compile with: /clr /c
interface class AA {};

generic <class T>
where T : interface class   // C3388
ref class C {};

// OK
generic <class T>
where T : AA
ref class D {};
```
