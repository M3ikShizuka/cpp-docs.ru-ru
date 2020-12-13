---
description: 'Дополнительные сведения о: Ошибка компилятора C2191'
title: Ошибка компилятора C2191
ms.date: 11/04/2016
f1_keywords:
- C2191
helpviewer_keywords:
- C2191
ms.assetid: 051b8350-e5de-4f51-ab6e-96d32366bcef
ms.openlocfilehash: b3b2133e70eeae566a972b0e5db11105b316d6f7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337669"
---
# <a name="compiler-error-c2191"></a>Ошибка компилятора C2191

второй список параметров длиннее первого

Функция C была объявлена второй раз с более длинным списком параметров. C не поддерживает перегруженные функции.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2191:

```c
// C2191.c
// compile with: /Za /c
void func( int );
void func( int, float );   // C2191 different parameter list
void func2( int, float );   // OK
```
