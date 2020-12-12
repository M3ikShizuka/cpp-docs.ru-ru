---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4242'
title: Предупреждение компилятора (уровень 4) C4242
ms.date: 11/04/2016
f1_keywords:
- C4242
helpviewer_keywords:
- C4242
ms.assetid: 8df742e1-fbf1-42f3-8e93-c0e1c222dc7e
ms.openlocfilehash: 7eabb546e2dff11b52be20e1a791aa31e9373a69
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97334853"
---
# <a name="compiler-warning-level-4-c4242"></a>Предупреждение компилятора (уровень 4) C4242

"идентификатор": преобразование из "тип1" в "тип2", возможна утрата данных

Типы различаются. Преобразование типов может привести к утрате данных. Компилятор выполняет преобразование типов.

Это предупреждение отключено по умолчанию. Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

Дополнительные сведения о C4242 см. в разделе [Общие ошибки компилятора](/windows/win32/WinProg64/common-compiler-errors).

Следующий пример приводит к возникновению ошибки C4242:

```cpp
// C4242.cpp
// compile with: /W4
#pragma warning(4:4242)
int func() {
   return 0;
}

int main() {
   char a;
   a = func();   // C4242, return type and variable type do not match
}
```
