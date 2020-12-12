---
description: 'Дополнительные сведения о: Ошибка компилятора C3114'
title: Ошибка компилятора C3114
ms.date: 11/04/2016
f1_keywords:
- C3114
helpviewer_keywords:
- C3114
ms.assetid: b5d2df4f-87d0-4292-9981-25c6a6013c05
ms.openlocfilehash: 18d14ae01c0ae101ff0b66d837edd0699312af9c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97115954"
---
# <a name="compiler-error-c3114"></a>Ошибка компилятора C3114

"аргумент": недопустимый именованный аргумент атрибута

Чтобы член данных класса атрибута был допустимым именованным аргументом, он не должен быть помечен как **`static`** , **`const`** или **`literal`** . Если свойство, свойство не должно быть **`static`** и должно иметь методы доступа get и Set.

Дополнительные сведения см. в разделе [Свойства](../../extensions/property-cpp-component-extensions.md) и [определяемые пользователем атрибуты](../../extensions/user-defined-attributes-cpp-component-extensions.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3114.

```cpp
// C3114.cpp
// compile with: /clr /c
public ref class A : System::Attribute {
public:
   static property int StaticProp {
      int get();
   }

   property int Prop2 {
      int get();
      void set(int i);
   }
};

[A(StaticProp=123)]   // C3114
public ref class R {};

[A(Prop2=123)]   // OK
public ref class S {};
```
