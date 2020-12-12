---
description: 'Дополнительные сведения о: Ошибка компилятора C2006'
title: Ошибка компилятора C2006
ms.date: 11/04/2016
f1_keywords:
- C2006
helpviewer_keywords:
- C2006
ms.assetid: caaed6f7-ceb9-4742-8820-d66657c0b04d
ms.openlocfilehash: 5747f5417db60bd3c1f7bc1420c257552a9b42c7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298517"
---
# <a name="compiler-error-c2006"></a>Ошибка компилятора C2006

для "директивы" требуется имя файла, найдено "token"

Для директив, таких как [#include](../../preprocessor/hash-include-directive-c-cpp.md) или [#import](../../preprocessor/hash-import-directive-cpp.md) , требуется имя файла. Чтобы устранить эту ошибку, убедитесь, что *токен* является допустимым именем файла. Кроме того, заключите имя файла в двойные кавычки или угловые скобки.

Следующий пример приводит к возникновению ошибки C2006:

```cpp
// C2006.cpp
#include stdio.h   // C2006
```

Возможное решение:

```cpp
// C2006b.cpp
// compile with: /c
#include <stdio.h>
```
