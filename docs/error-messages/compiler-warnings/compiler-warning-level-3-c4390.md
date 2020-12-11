---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4390'
title: Предупреждение компилятора (уровень 3) C4390
ms.date: 11/04/2016
f1_keywords:
- C4390
helpviewer_keywords:
- C4390
ms.assetid: c95c2f1b-9bce-4b1f-a80c-565d4cde0b1e
ms.openlocfilehash: 8067d4beae44e098085122968a227f6ff8bc8b4b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97160445"
---
# <a name="compiler-warning-level-3-c4390"></a>Предупреждение компилятора (уровень 3) C4390

";": найден пустой контролируемый оператор; является ли это намерением?

Точка с запятой обнаружена после оператора управления, который не содержит инструкций.

При получении C4390 из-за макроса следует использовать прагма-директиву [warning](../../preprocessor/warning.md) , чтобы отключить C4390 в модуле, содержащем макрос.

Следующий пример приводит к возникновению ошибки C4390:

```cpp
// C4390.cpp
// compile with: /W3
int main() {
   int i = 0;
   if (i);   // C4390
      i++;
}
```
