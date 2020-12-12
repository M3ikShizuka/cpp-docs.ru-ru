---
description: 'Дополнительные сведения о: Ошибка компилятора C3126'
title: Ошибка компилятора C3126
ms.date: 11/04/2016
f1_keywords:
- C3126
helpviewer_keywords:
- C3126
ms.assetid: e72658a3-5d85-4a31-89a4-dbc3d475973d
ms.openlocfilehash: 7084359ae0be412ccb36e9a634cc72848f1c8daa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97345463"
---
# <a name="compiler-error-c3126"></a>Ошибка компилятора C3126

невозможно определить объединение "Union" внутри управляемого типа "тип"

Объединение не может быть определено внутри управляемого типа.

Следующий пример приводит к возникновению ошибки C3126:

```cpp
// C3126_2.cpp
// compile with: /clr /c
ref class Test
{
   union x
   {   // C3126
      int a;
      int b;
   };
};
```
