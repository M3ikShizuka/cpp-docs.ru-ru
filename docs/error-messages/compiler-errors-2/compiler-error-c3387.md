---
description: 'Дополнительные сведения о: Ошибка компилятора C3387'
title: Ошибка компилятора C3387
ms.date: 11/04/2016
f1_keywords:
- C3387
helpviewer_keywords:
- C3387
ms.assetid: c54d9925-ed14-4976-b8db-e8d4dc84e536
ms.openlocfilehash: febd47004026a7e22ca576c153ee8cf1506c3e1d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97285556"
---
# <a name="compiler-error-c3387"></a>Ошибка компилятора C3387

"член": __declspec (dllexport)/ \_ _declspec (dllimport) не может применяться к члену типа Managed или WinRT

`dllimport` [](../../cpp/dllexport-dllimport.md) **`__declspec`** Модификаторы и не являются допустимыми для членов управляемого или среда выполнения Windowsого типа.

В следующем примере показано возникновение ошибки C3387 и приводятся сведения по ее устранению.

```cpp
// C3387a.cpp
// compile with: /clr /c
ref class X2 {
   void __declspec(dllexport) mf() {   // C3387
   // try the following line instead
   // void mf() {
   }
};
```
