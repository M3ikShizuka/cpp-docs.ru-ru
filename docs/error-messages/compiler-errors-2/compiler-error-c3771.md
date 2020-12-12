---
description: 'Дополнительные сведения о: Ошибка компилятора C3771'
title: Ошибка компилятора C3771
ms.date: 11/04/2016
f1_keywords:
- C3771
helpviewer_keywords:
- C3771
ms.assetid: 68c23b25-7f21-4eaa-8f7e-38fda1130a69
ms.openlocfilehash: f7d71952411632ded02bc5121c6f6668eddeabc0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97291666"
---
# <a name="compiler-error-c3771"></a>Ошибка компилятора C3771

"идентификатор": в ближайшей области пространства имен не удалось найти дружественное объявление

Объявление шаблона класса для указанного шаблона *идентификатор* не удалось найти в текущем пространстве имен.

### <a name="to-correct-this-error"></a>Исправление ошибки

- Убедитесь, что объявление шаблона класса для идентификатора шаблона задается в текущем пространстве имен или что идентификатор шаблона является полным именем.

## <a name="example"></a>Пример

Следующий пример кода объявляет шаблон класса и функцию в пространстве имен `NA`, но пытается объявить шаблон дружественной функции в пространстве имен `NB`.

```cpp
// C3771.cpp
// compile with: /c

namespace NA {
template<class T> class A {
    void aFunction(T t) {};
    };
}
// using namespace NA;
namespace NB {
    class X {
        template<class T> friend void A<T>::aFunction(T); // C3771
// try the following line instead
//      template<class T> friend void NA::A<T>::aFunction(T);
// or try "using namespace NA;" instead.
    };
}
```

## <a name="see-also"></a>См. также раздел

[Шаблоны](../../cpp/templates-cpp.md)
