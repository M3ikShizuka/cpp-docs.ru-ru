---
description: 'Дополнительные сведения о: Ошибка компилятора C2628'
title: Ошибка компилятора C2628
ms.date: 11/04/2016
f1_keywords:
- C2628
helpviewer_keywords:
- C2628
ms.assetid: 19a25e77-d5be-4107-88d5-0745b6281f98
ms.openlocfilehash: 876e96bfb406262c150807e4e95f14dd5b7177d5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97123569"
---
# <a name="compiler-error-c2628"></a>Ошибка компилятора C2628

"тип1", за которым следует "тип2", недопустим (возможно, вы забыли ";"?)

Возможно, отсутствует точка с запятой.

Следующий пример приводит к возникновению ошибки C2628:

```cpp
// C2628.cpp
class CMyClass {}
int main(){}   // C2628 error
```

Возможное решение:

```cpp
// C2628b.cpp
class CMyClass {};
int main(){}
```
