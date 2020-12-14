---
description: 'Дополнительные сведения: предупреждение компилятора (уровни 1 и 4) C4112'
title: Предупреждение компилятора (уровни 1 и 4) C4112
ms.date: 11/04/2016
f1_keywords:
- C4112
helpviewer_keywords:
- C4112
ms.assetid: aff64897-bb79-4a67-9b6f-902c6d44f3dc
ms.openlocfilehash: a4958cbd4537ab9c1f5686383f27414ae366e72b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97234557"
---
# <a name="compiler-warning-levels-1-and-4-c4112"></a>Предупреждение компилятора (уровни 1 и 4) C4112

\#для строки требуется целое число от 1 до Number

Директива [#Line](../../preprocessor/hash-line-directive-c-cpp.md) указывает целочисленный параметр, который не входит в допустимый диапазон.

Если указанный параметр имеет значение меньше 1, счетчик строк сбрасывается до 1. Если указанный параметр больше, чем *номер*, представляющий определенный компилятором предел, то счетчик строк не изменяется. Это предупреждение уровня 1 в режиме совместимости с ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)) и предупреждение уровня 4 в расширениях Майкрософт ([/Ze](../../build/reference/za-ze-disable-language-extensions.md)).

Следующий пример приводит к возникновению ошибки C4112:

```cpp
// C4112.cpp
// compile with: /W4
#line 0   // C4112, value must be between 1 and number

int main() {
}
```
