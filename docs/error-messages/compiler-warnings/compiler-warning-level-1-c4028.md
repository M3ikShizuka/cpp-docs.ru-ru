---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4028'
title: Предупреждение компилятора (уровень 1) C4028
ms.date: 11/04/2016
f1_keywords:
- C4028
helpviewer_keywords:
- C4028
ms.assetid: c3e8b70b-e870-416c-a285-bba5f71dbfc6
ms.openlocfilehash: ac6f4ba05d7acfa0772429372128d32c27fc909c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97241421"
---
# <a name="compiler-warning-level-1-c4028"></a>Предупреждение компилятора (уровень 1) C4028

формальный параметр "число" отличается от объявления

Тип формального параметра не согласуется с соответствующим параметром в объявлении. Используется тип в исходном объявлении.

Это предупреждение допустимо только для исходного кода на языке C.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4028.

```c
// C4028.c
// compile with: /W1 /Za
void f(int , ...);
void f(int i, int j) {}   // C4028

void g(int , int);
void g(int i, int j) {}   // OK

int main() {}
```
