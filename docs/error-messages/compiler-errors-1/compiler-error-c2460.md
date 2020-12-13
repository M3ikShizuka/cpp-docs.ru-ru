---
description: 'Дополнительные сведения о: Ошибка компилятора C2460'
title: Ошибка компилятора C2460
ms.date: 11/04/2016
f1_keywords:
- C2460
helpviewer_keywords:
- C2460
ms.assetid: d969fca9-3ac5-4e4e-88fc-df05510e2093
ms.openlocfilehash: 6a6b521b356d4005906e97b085271369f2624c46
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97341858"
---
# <a name="compiler-error-c2460"></a>Ошибка компилятора C2460

"идентификатор1": использует "идентификатор2", который определяется

Класс или структура ( `identifier2` ) объявляется как член самого себя ( `identifier1` ). Рекурсивные определения классов и структур не допускаются.

Следующий пример приводит к возникновению ошибки C2460:

```cpp
// C2460.cpp
class C {
   C aC;    // C2460
};
```

Вместо этого используйте ссылку на указатель в классе.

```cpp
// C2460.cpp
class C {
   C * aC;    // OK
};
```
