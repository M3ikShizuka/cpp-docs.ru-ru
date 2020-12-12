---
description: 'Дополнительные сведения о: Ошибка компилятора C2087'
title: Ошибка компилятора C2087
ms.date: 11/04/2016
f1_keywords:
- C2087
helpviewer_keywords:
- C2087
ms.assetid: 89761e83-415a-4468-a4c6-b6dedfd1dd6a
ms.openlocfilehash: 98e54a8df8f06230f1adca1cb6d2f23f80acff8e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97252042"
---
# <a name="compiler-error-c2087"></a>Ошибка компилятора C2087

"идентификатор": отсутствует индекс

В определении массива с несколькими индексами отсутствует значение подстрочного скрипта для измерения, превышающего единицу.

Следующий пример приводит к возникновению ошибки C2087:

```cpp
// C2087.cpp
int main() {
   char a[10][];   // C2087
}
```

Возможное решение:

```cpp
// C2087b.cpp
int main() {
   char b[4][5];
}
```
