---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4684'
title: Предупреждение компилятора (уровень 1) C4684
ms.date: 11/04/2016
f1_keywords:
- C4684
helpviewer_keywords:
- C4684
ms.assetid: e95f1a83-2784-4b05-ae94-12148e056e26
ms.openlocfilehash: 036548912c55b2f21d9d62b00a06e49c0af252ba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97285218"
---
# <a name="compiler-warning-level-1-c4684"></a>Предупреждение компилятора (уровень 1) C4684

"атрибут": предупреждение!! атрибут может вызвать недопустимое создание кода: используйте с осторожностью

Вы использовали атрибут, который обычно не должен использоваться.

Следующий пример приводит к возникновению ошибки C4684:

```cpp
// C4684.cpp
// compile with: /W1 /LD
[module(name="xx")]; // C4684 expected
[no_injected_text];
```
