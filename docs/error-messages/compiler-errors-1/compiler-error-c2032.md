---
description: 'Дополнительные сведения о: Ошибка компилятора C2032'
title: Ошибка компилятора C2032
ms.date: 11/04/2016
f1_keywords:
- C2032
helpviewer_keywords:
- C2032
ms.assetid: 625d7c83-70b6-42c2-a558-81fbc0026324
ms.openlocfilehash: cb39a539dc1e360f70cc2b217d50f3a1eabcf0f6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175460"
---
# <a name="compiler-error-c2032"></a>Ошибка компилятора C2032

"идентификатор": функция не может быть членом структуры или объединения "структорунион"

Структура или объединение имеет функцию-член, которая разрешена в C++, но не в C. Чтобы устранить эту ошибку, либо скомпилируйте ее как программу C++, либо удалите функцию-член.

Следующий пример приводит к возникновению ошибки C2032:

```c
// C2032.c
struct z {
   int i;
   void func();   // C2032
};
```

Возможное решение:

```c
// C2032b.c
// compile with: /c
struct z {
   int i;
};
```
