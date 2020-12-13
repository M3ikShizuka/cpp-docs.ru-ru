---
description: 'Дополнительные сведения о: Ошибка компилятора C2490'
title: Ошибка компилятора C2490
ms.date: 11/04/2016
f1_keywords:
- C2490
helpviewer_keywords:
- C2490
ms.assetid: 9de6bddd-b2e2-4ce6-b33b-201a8c2c8c54
ms.openlocfilehash: 9638b65eb453fcc957ac2e9a947138ba1f7ac745
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339349"
---
# <a name="compiler-error-c2490"></a>Ошибка компилятора C2490

"ключевое слово" не допускается в функции с атрибутом "naked"

Функция, определенная как [naked](../../cpp/naked-cpp.md) , не может использовать структурированную обработку исключений.

Следующий пример приводит к возникновению ошибки C2490:

```cpp
// C2490.cpp
// processor: x86
__declspec( naked ) int func() {
   __try{}   // C2490, structured exception handling
}
```
