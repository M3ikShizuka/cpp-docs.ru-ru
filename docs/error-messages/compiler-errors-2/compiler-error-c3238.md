---
description: 'Дополнительные сведения о: Ошибка компилятора C3238'
title: Ошибка компилятора C3238
ms.date: 11/04/2016
f1_keywords:
- C3238
helpviewer_keywords:
- C3238
ms.assetid: 19942497-b3c5-4df0-9144-142ced92468b
ms.openlocfilehash: d2900d8c00badb19edb16bb726eaf2ea503d4ef4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97307383"
---
# <a name="compiler-error-c3238"></a>Ошибка компилятора C3238

"тип": тип с этим именем уже перенаправлен в сборку "сборка"

В клиентском приложении был определен тип, который также определен посредством синтаксиса перенаправления в связанной сборке. Нельзя определять оба типа в области приложения.

Дополнительные сведения см. в разделе [Пересылка типов (C++/CLI)](../../extensions/type-forwarding-cpp-cli.md) .

## <a name="examples"></a>Примеры

В следующем примере создается сборка, содержащая тип, перенаправленный из другой сборки.

```cpp
// C3238.cpp
// compile with: /clr /LD
public ref class R {};
```

В следующем примере создается сборка, которая используется для содержания определения типа, но содержит не только синтаксис перенаправления для типа.

```cpp
// C3238_b.cpp
// compile with: /clr /LD
#using "C3238.dll"
[ assembly:TypeForwardedTo(R::typeid) ];
```

Следующий пример приводит к возникновению ошибки C3238.

```cpp
// C3238_c.cpp
// compile with: /clr /c
// C3238 expected
// Delete the following line to resolve.
#using "C3238_b.dll"
public ref class R {};
```
