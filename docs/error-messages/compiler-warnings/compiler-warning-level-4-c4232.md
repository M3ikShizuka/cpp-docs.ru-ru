---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4232'
title: Предупреждение компилятора (уровень 4) C4232
ms.date: 11/04/2016
f1_keywords:
- C4232
helpviewer_keywords:
- C4232
ms.assetid: f92028a5-4ddd-43c1-97f5-4f724e5e14af
ms.openlocfilehash: 272fdcbc856ef5e86a8ff043b5aeab98a36413a8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97291419"
---
# <a name="compiler-warning-level-4-c4232"></a>Предупреждение компилятора (уровень 4) C4232

использовано нестандартное расширение: "идентификатор": адрес dllimport "dllimport" не является статическим, удостоверение не гарантируется

В разделе расширения Майкрософт (/Ze) можно предоставить нестатическое значение в качестве адреса функции, объявленной с помощью **`dllimport`** модификатора. В режиме совместимости с ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)) это приводит к ошибке.

Следующий пример приводит к возникновению ошибки C4232:

```c
// C4232.c
// compile with: /W4 /Ze /c
int __declspec(dllimport) f();
int (*pfunc)() = &f;   // C4232
```
