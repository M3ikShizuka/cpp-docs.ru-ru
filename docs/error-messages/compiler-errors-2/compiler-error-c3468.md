---
description: 'Дополнительные сведения о: Ошибка компилятора C3468'
title: Ошибка компилятора C3468
ms.date: 11/04/2016
f1_keywords:
- C3468
helpviewer_keywords:
- C3468
ms.assetid: cfd320db-2f6e-4e0d-ba02-e79ece87e1e0
ms.openlocfilehash: 7e6d58e012baa0163f33867069e7250da61177b2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97315742"
---
# <a name="compiler-error-c3468"></a>Ошибка компилятора C3468

"тип": тип можно передать только в сборку:

"`file`" не является сборкой

Перенаправлять типы можно только в сборке.

Дополнительные сведения см. в разделе [Пересылка типов (C++/CLI)](../../extensions/type-forwarding-cpp-cli.md).

## <a name="examples"></a>Примеры

В приведенном ниже примере создается модуль.

```cpp
// C3468.cpp
// compile with: /LN /clr
public ref class R {};
```

Следующий пример приводит к возникновению ошибки C3468:

```cpp
// C3468_b.cpp
// compile with: /clr /c
#using "C3468.netmodule"
[ assembly:TypeForwardedTo(R::typeid) ];   // C3468
```
