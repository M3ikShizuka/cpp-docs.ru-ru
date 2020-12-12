---
description: 'Дополнительные сведения о: Ошибка компилятора C2133'
title: Ошибка компилятора C2133
ms.date: 11/04/2016
f1_keywords:
- C2133
helpviewer_keywords:
- C2133
ms.assetid: 8942f9e8-9818-468f-97db-09dbd124fcae
ms.openlocfilehash: d98cb3bd8df5543ecf0426a146157300f67dd91b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323133"
---
# <a name="compiler-error-c2133"></a>Ошибка компилятора C2133

"идентификатор": неизвестный размер

Неразмерный массив объявляется как член класса, структуры, объединения или перечисления. Параметр/Za (ANSI C) не допускает неразмерных массивов элементов.

Следующий пример приводит к возникновению ошибки C2133:

```cpp
// C2133.cpp
// compile with: /Za
struct X {
   int a[0];   // C2133 unsized array
};
```

Возможное решение:

```cpp
// C2133b.cpp
// compile with: /c
struct X {
   int a[0];   // no /Za
};
```
