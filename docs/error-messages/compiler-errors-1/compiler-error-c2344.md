---
description: 'Дополнительные сведения о: Ошибка компилятора C2344'
title: Ошибка компилятора C2344
ms.date: 11/04/2016
f1_keywords:
- C2344
helpviewer_keywords:
- C2344
ms.assetid: a84c7b37-c84e-4345-8691-c23abb2dc193
ms.openlocfilehash: 1ad4f1808f407a9f654f5bbf3a022c2dc7b0b3ff
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97234765"
---
# <a name="compiler-error-c2344"></a>Ошибка компилятора C2344

align(#): выравнивание должно быть степенью двух

При использовании ключевого слова [align](../../cpp/align-cpp.md) передаваемое значение должно быть степенью двух.

Например, приведенный ниже код вызывает ошибку C2344, так как число 3 не является степенью двух.

```cpp
// C2344.cpp
// compile with: /c
__declspec(align(3)) int a;   // C2344
__declspec(align(4)) int b;   // OK
```
