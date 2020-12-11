---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4052'
title: Предупреждение компилятора (уровень 1) C4052
ms.date: 11/04/2016
f1_keywords:
- C4052
helpviewer_keywords:
- C4052
ms.assetid: f9955421-16ab-46e5-8f9d-bf1639a519ef
ms.openlocfilehash: 0da0823b3268e8f957a87d1c975fb82098fe2511
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97160562"
---
# <a name="compiler-warning-level-1-c4052"></a>Предупреждение компилятора (уровень 1) C4052

объявления функции отличаются; одно из них содержит переменные аргументы

Одно объявление функции не содержит переменных аргументов. Игнорируется.

В следующем примере возникает ошибка C4052.

```c
// C4052.c
// compile with: /W4 /c
int f();
int f(int i, ...);   // C4052
```
