---
description: 'Дополнительные сведения о: Ошибка компилятора C3077'
title: Ошибка компилятора C3077
ms.date: 11/04/2016
f1_keywords:
- C3077
helpviewer_keywords:
- C3077
ms.assetid: d9f3c619-d1e2-4656-81a5-a35a9586a7d4
ms.openlocfilehash: a8e6a15f38427727939fbaabb0bfcf4d9e315d77
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320171"
---
# <a name="compiler-error-c3077"></a>Ошибка компилятора C3077

"метод_завершения": метод завершения может быть членом только ссылочного типа

Нельзя объявлять метод завершения с собственным типом или типом значения.

Дополнительные сведения см. [в разделе Деструкторы и методы завершения в статье инструкции: определение и использование классов и структур (C++/CLI)](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Destructors_and_finalizers).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3077.

```cpp
// C3077.cpp
// compile with: /clr /c
value struct vs {
   !vs(){}   // C3077
};

ref struct rs {
protected:
   !rs(){}   // OK
};
```
