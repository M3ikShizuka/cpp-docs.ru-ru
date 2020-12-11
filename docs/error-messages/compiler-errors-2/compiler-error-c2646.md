---
description: 'Дополнительные сведения о: Ошибка компилятора C2646'
title: Ошибка компилятора C2646
ms.date: 11/04/2016
f1_keywords:
- C2646
helpviewer_keywords:
- C2646
ms.assetid: 92ff1f02-5eaf-40a5-8b7a-a682f149e967
ms.openlocfilehash: 7aa378a0a2dbaeae78a63f97e83a84d94d861c72
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97160822"
---
# <a name="compiler-error-c2646"></a>Ошибка компилятора C2646

анонимную структуру или объединение в глобальной области видимости или области видимости пространства имен необходимо объявлять как статическое

Анонимная структура или объединение имеет область Global или Namespace, но не объявлена **`static`** .

В следующем примере показано возникновение ошибки C2646 и приводятся сведения по ее устранению.

```cpp
// C2646.cpp
// compile with: /c
union { int i; };   // C2646 not static

// OK
static union { int j; };
union U { int i; };
```
