---
description: 'Дополнительные сведения о: Ошибка компилятора C3163'
title: Ошибка компилятора C3163
ms.date: 11/04/2016
f1_keywords:
- C3163
helpviewer_keywords:
- C3163
ms.assetid: 17dcafa3-f416-4e04-a232-f9569218ba75
ms.openlocfilehash: 53d0135e3083de7727b2a6c7f51a3f75e7314405
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97203956"
---
# <a name="compiler-error-c3163"></a>Ошибка компилятора C3163

> "*конструкция*": атрибуты несовместимы с предыдущим объявлением

Атрибуты, применяемые к определению, конфликтуют с атрибутами, применяемыми к объявлению.

Одним из способов разрешения C3163 является удаление атрибутов в прямом объявлении. Все атрибуты в прямом объявлении должны быть меньше атрибутов в определении или, как правило, равно им.

Возможной причиной ошибки C3163 является язык аннотирования исходного кода Microsoft (SAL). Макросы SAL не расширяются, если проект не компилируется с помощью **`/analyze`** флага. Программа, которая компилируется чисто без **`/analyze`** возможности создания C3163, если попытается перекомпилировать ее с **`/analyze`** параметром. Дополнительные сведения о SAL см. в разделе [аннотации SAL](../../c-runtime-library/sal-annotations.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3163.

```cpp
// C3163.cpp
// compile with: /clr /c
using namespace System;

[CLSCompliant(true)] void f();
[CLSCompliant(false)] void f() {}   // C3163
// try the following line instead
// [CLSCompliant(true)] void f() {}
```

## <a name="see-also"></a>См. также раздел

[Аннотации SAL](../../c-runtime-library/sal-annotations.md)
