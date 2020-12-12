---
description: 'Дополнительные сведения о: Ошибка компилятора C3227'
title: Ошибка компилятора C3227
ms.date: 11/04/2016
f1_keywords:
- C3227
helpviewer_keywords:
- C3227
ms.assetid: 7939c23a-96c8-43c2-89e9-f217d132d155
ms.openlocfilehash: 26d66bf3e0c3bc3a6f391d66608f3e6790b2d11d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97304146"
---
# <a name="compiler-error-c3227"></a>Ошибка компилятора C3227

"параметр": нельзя использовать "ключевое слово" для выделения универсального типа

Чтобы создать экземпляр типа, требуется соответствующий конструктор. Однако компилятор не может гарантировать доступность соответствующего конструктора.

Для устранения этой ошибки можно использовать шаблоны вместо универсальных шаблонов. также можно использовать один из нескольких методов для создания экземпляра типа.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3227.

```cpp
// C3227.cpp
// compile with: /clr /c
generic<class T> interface class ICreate {
   static T Create();
};

generic <class T>
where T : ICreate<T>
ref class C {
   void f() {
      T t = new T;   // C3227

      // OK
      T t2 = ICreate<T>::Create();
      T t3 = safe_cast<T>( System::Activator::CreateInstance(T::typeid) );
   }
};
```
