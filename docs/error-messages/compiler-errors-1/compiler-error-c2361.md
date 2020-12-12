---
description: 'Дополнительные сведения о: Ошибка компилятора C2361'
title: Ошибка компилятора C2361
ms.date: 11/04/2016
f1_keywords:
- C2361
helpviewer_keywords:
- C2361
ms.assetid: efbdaeb9-891c-4f7d-97da-89088a8413f3
ms.openlocfilehash: 53ca69daf347d23bb27e214556a74c70c1e53725
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97328315"
---
# <a name="compiler-error-c2361"></a>Ошибка компилятора C2361

Инициализация "идентификатор" пропускается меткой "default"

Инициализацию `identifier` можно пропустить в **`switch`** операторе. Нельзя перейти к предшествующему объявлению с инициализатором, если объявление не заключено в блок. (Если только он не объявлен в блоке, переменная находится в пределах области до конца **`switch`** оператора.)

Следующий пример приводит к возникновению ошибки C2361:

```cpp
// C2361.cpp
void func( void ) {
   int x;
   switch (x) {
   case 0 :
      int i = 1;
      { int j = 1; }
   default :   // C2361 error
      int k = 1;
   }
}
```

Возможное решение:

```cpp
// C2361b.cpp
// compile with: /c
void func( void ) {
   int x = 0;
   switch (x) {
   case 0 :
      { int j = 1; int i = 1;}
   default :
      int k = 1;
   }
}
```
