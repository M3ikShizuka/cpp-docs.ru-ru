---
description: 'Дополнительные сведения о: Ошибка компилятора C2007'
title: Ошибка компилятора C2007
ms.date: 11/04/2016
f1_keywords:
- C2007
helpviewer_keywords:
- C2007
ms.assetid: ecd09d99-5036-408b-9e46-bc15488f049e
ms.openlocfilehash: fa2ad780269079ef081f22d2c222e106443200e1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298491"
---
# <a name="compiler-error-c2007"></a>Ошибка компилятора C2007

\#определение синтаксиса

Идентификатор не отображается после a `#define` . Чтобы устранить эту ошибку, используйте идентификатор.

Следующий пример приводит к возникновению ошибки C2007:

```cpp
// C2007.cpp
#define   // C2007
```

Возможное решение:

```cpp
// C2007b.cpp
// compile with: /c
#define true 1
```
