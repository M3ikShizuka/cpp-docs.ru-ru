---
description: 'Дополнительные сведения о: Неустранимая ошибка C1020'
title: Неустранимая ошибка C1020
ms.date: 11/04/2016
f1_keywords:
- C1020
helpviewer_keywords:
- C1020
ms.assetid: 42f429e2-5e3b-4086-a10d-b99e032e51c5
ms.openlocfilehash: 444da85bddf65533eb5ae37278085664efeae7ee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97316366"
---
# <a name="fatal-error-c1020"></a>Неустранимая ошибка C1020

непредвиденный #endif

Директива `#endif` не имеет соответствующей директивы `#if`, `#ifdef`или `#ifndef` . Убедитесь, что каждая директива `#endif` имеет соответствующую директиву.

В следующем примере возникает ошибка C1020:

```cpp
// C1020.cpp
#endif     // C1020
```

Возможное решение:

```cpp
// C1020b.cpp
// compile with: /c
#if 1
#endif
```
