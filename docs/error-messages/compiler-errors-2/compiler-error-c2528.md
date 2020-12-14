---
description: 'Дополнительные сведения о: Ошибка компилятора C2528'
title: Ошибка компилятора C2528
ms.date: 11/04/2016
f1_keywords:
- C2528
helpviewer_keywords:
- C2528
ms.assetid: 2ea9d583-67a8-4b16-b35f-a50eeffc03c4
ms.openlocfilehash: de07867f48843be76ff5b8d74dda9725b50a2560
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97302183"
---
# <a name="compiler-error-c2528"></a>Ошибка компилятора C2528

"имя": недопустимый указатель на ссылку

Нельзя объявить указатель на ссылку. Разыменование переменной перед объявлением указателя на нее.

Следующий пример приводит к возникновению ошибки C2528:

```cpp
// C2528.cpp
int i;
int &ir = i;
int & (*irptr) = ir;    // C2528
```
