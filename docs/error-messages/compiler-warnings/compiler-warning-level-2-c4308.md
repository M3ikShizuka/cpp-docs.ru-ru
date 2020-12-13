---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 2) C4308'
title: Предупреждение компилятора (уровень 2) C4308
ms.date: 11/04/2016
f1_keywords:
- C4308
helpviewer_keywords:
- C4308
ms.assetid: d4e5c53c-71b2-4bbc-8a7c-3a2a3180d9d9
ms.openlocfilehash: 180372bef17180b74431ea3c317417f15a6a231d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97339192"
---
# <a name="compiler-warning-level-2-c4308"></a>Предупреждение компилятора (уровень 2) C4308

отрицательная целая константа преобразована в тип без знака

Выражение преобразует отрицательную целочисленную константу в тип без знака. Результат выражения, вероятно, не имеет смысла.

## <a name="example"></a>Пример

```cpp
// C4308.cpp
// compile with: /W2
unsigned int u = (-5 + 3U);   // C4308

int main()
{
}
```
