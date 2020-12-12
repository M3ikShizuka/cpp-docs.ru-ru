---
description: 'Дополнительные сведения о: Ошибка компилятора C2008'
title: Ошибка компилятора C2008
ms.date: 11/04/2016
f1_keywords:
- C2008
helpviewer_keywords:
- C2008
ms.assetid: e748ccbe-ffd4-4008-aca7-e53c25225209
ms.openlocfilehash: 3fcde1885fd752a03a1285470a232f1daaa27df2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298530"
---
# <a name="compiler-error-c2008"></a>Ошибка компилятора C2008

"символ": не требуется в макроопределении

Символ отображается сразу после имени макроса. Чтобы устранить эту ошибку, после имени макроса должен быть пробел.

Следующий пример приводит к возникновению ошибки C2008:

```cpp
// C2008.cpp
#define TEST1"mytest1"    // C2008
```

Возможное решение:

```cpp
// C2008b.cpp
// compile with: /c
#define TEST2 "mytest2"
```
