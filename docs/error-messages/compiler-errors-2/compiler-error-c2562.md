---
description: 'Дополнительные сведения о: Ошибка компилятора C2562'
title: Ошибка компилятора C2562
ms.date: 11/04/2016
f1_keywords:
- C2562
helpviewer_keywords:
- C2562
ms.assetid: 2c41e511-9952-4b98-9976-6b1523613e1b
ms.openlocfilehash: 9e9da8a7463b450073f4b537ec36512242995760
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338705"
---
# <a name="compiler-error-c2562"></a>Ошибка компилятора C2562

"идентификатор": функция "void", возвращающая значение

Функция объявлена как, **`void`** но возвращает значение.

Эта ошибка может быть вызвана неправильным прототипом функции.

Эту ошибку можно исправить, если указать тип возвращаемого значения в объявлении функции.

Следующий пример приводит к возникновению ошибки C2562:

```cpp
// C2562.cpp
// compile with: /c
void testfunc() {
   int i;
   return i;   // C2562 delete the return to resolve
}
```
