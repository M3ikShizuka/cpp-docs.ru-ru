---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4212'
title: Предупреждение компилятора (уровень 4) C4212
ms.date: 11/04/2016
f1_keywords:
- C4212
helpviewer_keywords:
- C4212
ms.assetid: df781ea1-182d-4f9f-9a31-55b6ce80c711
ms.openlocfilehash: 3c557e5fa11e2a6fb1f15e5389901ede537755af
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97297360"
---
# <a name="compiler-warning-level-4-c4212"></a>Предупреждение компилятора (уровень 4) C4212

использовано нестандартное расширение: в объявлении функции используется многоточие

Прототип функции имеет переменное число аргументов. Определение функции не имеет значение.

Следующий пример приводит к возникновению ошибки C4212:

```c
// C4212.c
// compile with: /W4 /Ze /c
void f(int , ...);
void f(int i, int j) {}
```
