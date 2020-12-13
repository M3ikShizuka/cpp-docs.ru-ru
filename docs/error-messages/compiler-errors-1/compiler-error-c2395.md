---
description: 'Дополнительные сведения о: Ошибка компилятора C2395'
title: Ошибка компилятора C2395
ms.date: 11/04/2016
f1_keywords:
- C2395
helpviewer_keywords:
- C2395
ms.assetid: 2d9e3b28-8c2c-4f41-a57f-61ef88fc2af0
ms.openlocfilehash: 86b6123646ca91945a861e9b9822076877421ac8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97145474"
---
# <a name="compiler-error-c2395"></a>Ошибка компилятора C2395

'your_type::operator'op'' : недопустимый оператор CLR или WinRT. По крайней мере один параметр должен иметь следующие типы: 'T ', ' не% ', '& ', ' не ^ ', ' t ^% ', ' t ^& ', где T = ' your_type '

Оператор в управляемом типе или типе среды выполнения Windows не содержал по крайней мере один параметр, тип которого совпадает с типом значения, возвращаемого оператором.

В следующем примере показано возникновение ошибки C2395 и приводятся сведения по ее устранению.

```cpp
// C2395.cpp
// compile with: /clr /c
value struct V {
   static V operator *(int i, char c);   // C2395

   // OK
   static V operator *(V v, char c);
   // or
   static V operator *(int i, V& rv);
};
```
