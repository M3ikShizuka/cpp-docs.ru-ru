---
description: 'Дополнительные сведения о: Ошибка компилятора C2142'
title: Ошибка компилятора C2142
ms.date: 11/04/2016
f1_keywords:
- C2142
helpviewer_keywords:
- C2142
ms.assetid: d0dbe10e-0952-49a4-8b33-e82fb7558b19
ms.openlocfilehash: 65bd189fe99bb54549e458b093b72d8e47b840a3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97235532"
---
# <a name="compiler-error-c2142"></a>Ошибка компилятора C2142

различаются объявления функций, параметры переменных задаются только в одном из них

Одно объявление функции содержит переменный список параметров. Другое объявление не имеет. Только ANSI C ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).

Следующий пример приводит к возникновению ошибки C2142:

```c
// C2142.c
// compile with: /Za /c
void func();
void func( int, ... );   // C2142
void func2( int, ... );   // OK
```
