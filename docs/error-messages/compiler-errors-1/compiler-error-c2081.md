---
description: 'Дополнительные сведения о: Ошибка компилятора C2081'
title: Ошибка компилятора C2081
ms.date: 11/04/2016
f1_keywords:
- C2081
helpviewer_keywords:
- C2081
ms.assetid: 7db9892d-364d-4178-a49d-f8398ece09a0
ms.openlocfilehash: e6f75d6d478d9523d36a9671457cf2a5618e4f21
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97151181"
---
# <a name="compiler-error-c2081"></a>Ошибка компилятора C2081

"идентификатор": недопустимое имя в списке формальных параметров

Идентификатор привел к синтаксической ошибке.

Эта ошибка может быть вызвана использованием старого стиля для списка формальных параметров. В списке формальных параметров необходимо указать тип формальных параметров.

Следующий пример приводит к возникновению ошибки C2081:

```c
// C2081.c
void func( int i, j ) {}  // C2081, no type specified for j
```

Возможное решение:

```c
// C2081b.c
// compile with: /c
void func( int i, int j ) {}
```
