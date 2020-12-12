---
description: 'Дополнительные сведения о: Ошибка компилятора C2085'
title: Ошибка компилятора C2085
ms.date: 11/04/2016
f1_keywords:
- C2085
helpviewer_keywords:
- C2085
ms.assetid: 0a86785c-8e6f-481b-8c7b-412220c1950d
ms.openlocfilehash: 2cd828c9a18c06c5794bef01ba861f702af2e096
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97252120"
---
# <a name="compiler-error-c2085"></a>Ошибка компилятора C2085

"идентификатор": отсутствует в списке формальных параметров

Идентификатор был объявлен в определении функции, но отсутствует в списке формальных параметров. (Только ANSI C)

Следующий пример приводит к возникновению ошибки C2085:

```c
// C2085.c
void func1( void )
int main( void ) {}   // C2085
```

Возможное решение:

```c
// C2085b.c
void func1( void );
int main( void ) {}
```

Если точка с запятой отсутствует, то `func1()` она выглядит как определение функции, а не прототип, так что `main` определяется в `func1()` , создавая ошибку C2085 для идентификатора `main` .
