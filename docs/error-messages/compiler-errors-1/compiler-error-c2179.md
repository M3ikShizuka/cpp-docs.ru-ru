---
description: 'Дополнительные сведения о: Ошибка компилятора C2179'
title: Ошибка компилятора C2179
ms.date: 11/04/2016
f1_keywords:
- C2179
helpviewer_keywords:
- C2179
ms.assetid: f929bfc6-3964-4e54-87d6-7529b9b6c0b9
ms.openlocfilehash: 17ddc839161f36efc668bb52504e2434ec82f995
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335219"
---
# <a name="compiler-error-c2179"></a>Ошибка компилятора C2179

"тип": аргумент атрибута не может использовать параметры типа

Параметр универсального типа разрешается во время выполнения. Однако параметр атрибута должен быть разрешен во время компиляции. Поэтому нельзя использовать параметр универсального типа в качестве аргумента атрибута.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2179.

```cpp
// C2179.cpp
// compile with: /clr
using namespace System;

public ref struct Attr : Attribute {
   Attr(Type ^ a) {
      x = a;
   }

   Type ^ x;
};

ref struct G {};

generic<typename T>
public ref class Z {
public:
   Type ^ d;
   [Attr(T::typeid)]   // C2179
   // try the following line instead
   // [Attr(G::typeid)]
   T t;
};
```
