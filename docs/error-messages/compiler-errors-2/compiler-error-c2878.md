---
description: 'Дополнительные сведения о: Ошибка компилятора C2878'
title: Ошибка компилятора C2878
ms.date: 11/04/2016
f1_keywords:
- C2878
helpviewer_keywords:
- C2878
ms.assetid: 83ee3de1-f554-49e8-a840-1f550cee7f69
ms.openlocfilehash: df79869572117eed851c5edd63f94234555cb990
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320477"
---
# <a name="compiler-error-c2878"></a>Ошибка компилятора C2878

"имя": пространство имен или класс с таким именем не существует

Вы внесли ссылки на пространство имен или класс, который не определен.

Следующий пример приводит к возникновению ошибки C2878:

```cpp
// C2878.cpp
// compile with: /c
namespace A {}
namespace B = C;   // C2878 namespace C doesn't exist
namespace B = A;
```
