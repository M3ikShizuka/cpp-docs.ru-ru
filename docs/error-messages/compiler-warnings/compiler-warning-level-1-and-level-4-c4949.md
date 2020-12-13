---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1 и уровень 4) C4949'
title: Предупреждение компилятора (уровень 1 и 4) C4949
ms.date: 11/04/2016
f1_keywords:
- C4949
helpviewer_keywords:
- C4949
ms.assetid: 34f45a05-c115-49cb-9f67-0bd4f0735d9b
ms.openlocfilehash: 2330843c34207edbe99607208baff634836044cc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336013"
---
# <a name="compiler-warning-level-1-and-level-4-c4949"></a>Предупреждение компилятора (уровень 1 и 4) C4949

директивы pragma "Managed" и "unmanaged" имеют смысл только при компиляции с параметром "/CLR [: Option]"

Компилятор игнорирует [управляемые](../../preprocessor/managed-unmanaged.md) и неуправляемые прагмы, если исходный код не компилируется с [параметром/CLR](../../build/reference/clr-common-language-runtime-compilation.md). Это предупреждение носит информационный характер.

Следующий пример приводит к возникновению ошибки C4949:

```cpp
// C4949.cpp
// compile with: /LD /W1
#pragma managed   // C4949
```

При использовании **неуправляемого #pragma** без **/CLR**, C4949 представляет собой предупреждение уровня 4.

Следующий пример приводит к возникновению ошибки C4949:

```cpp
// C4949b.cpp
// compile with: /LD /W4
#pragma unmanaged   // C4949
```
