---
description: 'Дополнительные сведения о: Ошибка компилятора C2449'
title: Ошибка компилятора C2449
ms.date: 11/04/2016
f1_keywords:
- C2449
helpviewer_keywords:
- C2449
ms.assetid: 544bf0b6-daa0-40e8-9f21-8e583d472a2d
ms.openlocfilehash: cea4218d71b01a5f93b4c9409175449f78e3211f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332448"
---
# <a name="compiler-error-c2449"></a>Ошибка компилятора C2449

обнаружено "{" в области файла (отсутствует заголовок функции?)

Открытая фигурная скобка возникает в области видимости файла.

Эта ошибка может быть вызвана точкой с запятой между заголовком функции и открывающей фигурной скобкой определения функции.

Следующий пример приводит к возникновению ошибки C2499:

```c
// C2449.c
// compile with: /c
void __stdcall func(void) {}   // OK
void __stdcall func(void);  // extra semicolon on this line
{                         // C2449 detected here
```
