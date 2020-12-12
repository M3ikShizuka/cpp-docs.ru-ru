---
description: 'Дополнительные сведения о: Ошибка компилятора C2814'
title: Ошибка компилятора C2814
ms.date: 11/04/2016
f1_keywords:
- C2814
helpviewer_keywords:
- C2814
ms.assetid: 7d165136-a08b-4497-a76d-60a21bb19404
ms.openlocfilehash: 3da888c70356abee8ae18990d521d5589a5c5069
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97278393"
---
# <a name="compiler-error-c2814"></a>Ошибка компилятора C2814

member: неуправляемый тип не может быть вложенным в управляемом типе или типе WinRT "type"

## <a name="example"></a>Пример

Неуправляемый тип не может быть вложенным в типе CLR или WinRT. В следующем примере показано возникновение ошибки C2814 и приводятся сведения по ее устранению.

```cpp
// C2814.cpp
// compile with: /clr /c
ref class A {
   class B {};   // C2814
   ref class C {};   // OK
};
```
