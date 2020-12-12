---
description: 'Дополнительные сведения о: Ошибка компилятора C3920'
title: Ошибка компилятора C3920
ms.date: 11/04/2016
f1_keywords:
- C3920
helpviewer_keywords:
- C3920
ms.assetid: 66e91f28-ed82-4ce2-bf22-c0c74905b1ed
ms.openlocfilehash: b4cb793744126ee7bc91d18692d25439880fc672
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326577"
---
# <a name="compiler-error-c3920"></a>Ошибка компилятора C3920

"оператор": не удается определить постфиксный оператор инкремента или уменьшения, вызывающий постфиксный оператор WinRT или CLR будет вызывать соответствующий оператор prefix WinRT или CLR (op_Increment/op_Decrement), но с постфиксной семантикой

Среда выполнения Windows и среда CLR не поддерживают постфиксный оператор, а пользовательские постфиксные операторы не разрешены.  Можно определить префиксный оператор, который будет использоваться для операций до и после приращения.

В следующем примере показано возникновение ошибки C3920 и приводятся сведения по ее устранению.

```cpp
// C3920.cpp
// compile with: /clr /LD
public value struct V {
   static V operator ++(V me, int)
   // try the following line instead
   // static V operator ++(V me)
   {   // C3920
      me.m_i++;
      return me;
   }

   int m_i;
};
```
