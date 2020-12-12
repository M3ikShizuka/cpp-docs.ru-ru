---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4114'
title: Предупреждение компилятора (уровень 1) C4114
ms.date: 11/04/2016
f1_keywords:
- C4114
helpviewer_keywords:
- C4114
ms.assetid: 3983e1c6-e8bb-46dc-8894-e1827db48797
ms.openlocfilehash: 7d1d7696fabdf8e5114ba733f7bf6de53353bcb4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97267447"
---
# <a name="compiler-warning-level-1-c4114"></a>Предупреждение компилятора (уровень 1) C4114

Множественное использование одного и того же квалификатора типа

В объявлении типа или определении используется квалификатор типа ( **`const`** , **`volatile`** , **`signed`** или **`unsigned`** ) более одного раза. Это вызывает предупреждение с расширениями Майкрософт (/Ze) и ошибкой в режиме совместимости с ANSI (/ZA).

Следующий пример приводит к возникновению ошибки C4114:

```cpp
// C4114.cpp
// compile with: /W1 /c
volatile volatile int i;   // C4114
```

Следующий пример приводит к возникновению ошибки C4114:

```cpp
// C4114_b.cpp
// compile with: /W1 /c
static const int const * ii;   // C4114
static const int * const iii;   // OK
```
