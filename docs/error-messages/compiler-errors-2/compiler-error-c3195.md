---
description: 'Дополнительные сведения о: Ошибка компилятора C3195'
title: Ошибка компилятора C3195
ms.date: 11/04/2016
f1_keywords:
- C3195
helpviewer_keywords:
- C3195
ms.assetid: 97e4f681-812b-49e8-ba57-24b7817e3cd8
ms.openlocfilehash: 691aa50fcb091f240253363a23671ac4db70894f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97203800"
---
# <a name="compiler-error-c3195"></a>Ошибка компилятора C3195

operator: зарезервирован и не может использоваться как элемент ссылочного класса или типа значения. Операторы среды CLR или WinRT должны быть определены с помощью ключевого слова operator

Компилятор обнаружил определение оператора с использованием синтаксиса управляемых расширений для C++. Для операторов необходимо использовать синтаксис C++.

В следующем примере показано возникновение ошибки C3195 и приводятся сведения по ее устранению.

```cpp
// C3195.cpp
// compile with: /clr /LD
#using <mscorlib.dll>
value struct V {
   static V op_Addition(V v, int i);   // C3195
   static V operator +(V v, char c);   // OK for new C++ syntax
};
```
