---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4216'
title: Предупреждение компилятора (уровень 4) C4216
ms.date: 11/04/2016
f1_keywords:
- C4216
helpviewer_keywords:
- C4216
ms.assetid: 211079dc-59d0-42a7-801c-2ddab21d7232
ms.openlocfilehash: b570863653ea64d159cbb2f4a11138b2361ce149
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97266485"
---
# <a name="compiler-warning-level-1-c4216"></a>Предупреждение компилятора (уровень 4) C4216

использовано нестандартное расширение: float Long

Расширения Майкрософт по умолчанию (/Ze) обрабатывают значение **float Long** , равное **`double`** . ANSI Compatibility ([/Za](../../build/reference/za-ze-disable-language-extensions.md)) не поддерживает. Используйте **`double`** для обеспечения совместимости. Следующий пример приводит к возникновению ошибки C4216:

```cpp
// C4216.cpp
// compile with: /W1
float long a;   // C4216

// use the line below to resolve the warning
// double a;

int main() {
}
```
