---
description: 'Дополнительные сведения о: Ошибка компилятора C2505'
title: Ошибка компилятора C2505
ms.date: 11/04/2016
f1_keywords:
- C2505
helpviewer_keywords:
- C2505
ms.assetid: b19f5c53-399d-425e-90db-fe3ca9b40858
ms.openlocfilehash: 46054594731b8e39f4cb4b13e71559fcdbd2a55d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97213017"
---
# <a name="compiler-error-c2505"></a>Ошибка компилятора C2505

"символ": "__declspec (модификатор)" может применяться только к объявлениям или определениям глобальных объектов или статических данных-членов

**`__declspec`** В функции использовался модификатор, предназначенный для использования только в глобальной области.

Дополнительные сведения см. в разделах [appdomain](../../cpp/appdomain.md) и [process](../../cpp/process.md).

Следующий пример приводит к возникновению ошибки C2505:

```cpp
// C2505.cpp
// compile with: /clr

// OK
__declspec(process) int ii;
__declspec(appdomain) int jj;

int main() {
   __declspec(process) int i;   // C2505
   __declspec(appdomain) int j;   // C2505
}
```
