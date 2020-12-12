---
description: 'Дополнительные сведения о: Ошибка компилятора C2563'
title: Ошибка компилятора C2563
ms.date: 11/04/2016
f1_keywords:
- C2563
helpviewer_keywords:
- C2563
ms.assetid: 54abba68-6458-4ca5-894d-3babdb7b3552
ms.openlocfilehash: 2243e0820b2e69d6bc05351fdba4600188a3ac08
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209156"
---
# <a name="compiler-error-c2563"></a>Ошибка компилятора C2563

несоответствие в списке формальных параметров

Список формальных параметров функции (или указателя на функцию) не соответствует другим функциям (или указателю на функцию-член). В результате назначение функций или указателей не может быть выполнено.

Следующий пример приводит к возникновению ошибки C2563:

```cpp
// C2563.cpp
void func( int );
void func( int, int );
int main() {
   void *fp();
   fp = func;   // C2563
}
```
