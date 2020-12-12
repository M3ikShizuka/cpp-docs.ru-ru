---
description: 'Дополнительные сведения о: Ошибка компилятора C3194'
title: Ошибка компилятора C3194
ms.date: 11/04/2016
f1_keywords:
- C3194
helpviewer_keywords:
- C3194
ms.assetid: 49d3ffc6-eff6-4b46-865b-18811692a8bb
ms.openlocfilehash: 7513b9d4964b6eb0024c3b51480f188243bf2637
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97174043"
---
# <a name="compiler-error-c3194"></a>Ошибка компилятора C3194

"член": тип значения не может иметь оператор присваивания

Специальные функции-члены, требующие автоматического вызова компилятором, такие как конструктор копий или оператор присваивания копий, не поддерживаются в классе значений.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3194.

```cpp
// C3194.cpp
// compile with: /clr /c
value struct MyStruct {
   MyStruct& operator= (const MyStruct& i) { return *this; }   // C3194
};

ref struct MyStruct2 {
   MyStruct2% operator= (const MyStruct2% i) { return *this; }   // OK
};
```
