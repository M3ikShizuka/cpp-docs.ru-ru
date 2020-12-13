---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4629'
title: Предупреждение компилятора (уровень 4) C4629
ms.date: 11/04/2016
f1_keywords:
- C4629
helpviewer_keywords:
- C4629
ms.assetid: 158cde12-bae5-4d43-b575-b52b35aaa0b9
ms.openlocfilehash: b357b72ca95682c33d3f4019d4663593c5c5ee8d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97134177"
---
# <a name="compiler-warning-level-4-c4629"></a>Предупреждение компилятора (уровень 4) C4629

использован диграф, последовательность знаков digraph интерпретирована как токен char (если требуется другой результат, добавьте пробел между двумя знаками)

При использовании параметра [/Za](../../build/reference/za-ze-disable-language-extensions.md)компилятор выдает предупреждение, когда обнаруживает диграф.

В следующем примере возникает ошибка C4629.

```cpp
// C4629.cpp
// compile with: /Za /W4
int main()
<%   // C4629 <% digraph for {
}
```
