---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4628'
title: Предупреждение компилятора (уровень 1) C4628
ms.date: 11/04/2016
f1_keywords:
- C4628
helpviewer_keywords:
- C4628
ms.assetid: 20fdc6f8-5f6a-40cc-aff8-c7ccf3d8ec26
ms.openlocfilehash: b5dd017afb5b8bb0d882700cb047643d6d118685
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97112379"
---
# <a name="compiler-warning-level-1-c4628"></a>Предупреждение компилятора (уровень 1) C4628

диграфы не поддерживаются при наличии параметра -Ze. Последовательность знаков "digraph" не преобразована в альтернативный маркер для "char"

Раскрутки не поддерживаются при использовании параметра [/Ze](../../build/reference/za-ze-disable-language-extensions.md). После этого предупреждения будет выведено сообщение об ошибке.

Это предупреждение отключено по умолчанию. Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

Следующий пример приводит к возникновению ошибки C4628:

```cpp
// C4628.cpp
// compile with: /WX
#pragma warning(default : 4628)
int main()
<%   // C4628 <% digraph for {
}
```
