---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4659'
title: Предупреждение компилятора (уровень 1) C4659
ms.date: 11/04/2016
f1_keywords:
- C4659
helpviewer_keywords:
- C4659
ms.assetid: e29ba8db-7917-43f6-8e34-868b752279ae
ms.openlocfilehash: 05ec1e088e00b184ba083b6b197afc6041707449
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318820"
---
# <a name="compiler-warning-level-1-c4659"></a>Предупреждение компилятора (уровень 1) C4659

\#pragma "pragma": использование зарезервированного сегмента "сегмент" имеет неопределенное поведение, используйте #pragma комментарий (компоновщик,...)

Параметр. drectve использовался для передачи параметра компоновщику. Вместо этого используйте [Комментарий](../../preprocessor/comment-c-cpp.md) директивы pragma для передачи параметра компоновщика.

```cpp
// C4659.cpp
// compile with: /W1 /LD
#pragma code_seg(".drectve")   // C4659
```
