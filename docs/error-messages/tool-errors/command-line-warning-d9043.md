---
description: 'Дополнительные сведения о: Command-Line Warning D9043'
title: Предупреждение командной строки D9043
ms.date: 11/04/2016
f1_keywords:
- D9043
helpviewer_keywords:
- D9043
ms.assetid: 9263e28d-217b-414c-bfb6-86efd3c27a77
ms.openlocfilehash: ac61626f21465056ea96efe784e19405481f1b0f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97119753"
---
# <a name="command-line-warning-d9043"></a>Предупреждение командной строки D9043

Недопустимое значение "warning_level" для "compiler_option"; предполагается "4999"; Предупреждения анализа кода не связаны с уровнями предупреждений

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C9043.

```cpp
// D9043.cpp
// compile with: /analyze /w16001
// D9043 warning expected
int main() {}
```
