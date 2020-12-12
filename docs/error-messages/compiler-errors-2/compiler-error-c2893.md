---
description: 'Дополнительные сведения о: Ошибка компилятора C2893'
title: Ошибка компилятора C2893
ms.date: 11/04/2016
f1_keywords:
- C2893
helpviewer_keywords:
- C2893
ms.assetid: ec0cbe43-005d-45da-8742-aaeb9b81d28e
ms.openlocfilehash: 42e31327096a539feeb691c698b52f57ecb615a5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97278263"
---
# <a name="compiler-error-c2893"></a>Ошибка компилятора C2893

Не удалось выполнить специализацию шаблона функции "имя шаблона"

Компилятору не удалось специализацию шаблона функции. Эта ошибка может быть вызвана многими причинами.

Как правило, для устранения ошибки C2893 необходимо проверить сигнатуру функции и убедиться, что вы можете создать экземпляр каждого типа.

## <a name="example"></a>Пример

C2893 происходит потому `f` , что параметр шаблона был `T` выведен как `std::map<int,int>` , но не `std::map<int,int>` имеет элемента `data_type` ( `T::data_type` экземпляр не может быть создан с помощью `T = std::map<int,int>` .) Следующий пример приводит к возникновению ошибки C2893.

```cpp
// C2893.cpp
// compile with: /c /EHsc
#include<map>
using namespace std;
class MyClass {};

template<class T>
inline typename T::data_type
// try the following line instead
// inline typename  T::mapped_type
f(T const& p1, MyClass const& p2);

template<class T>
void bar(T const& p1) {
    MyClass r;
    f(p1,r);   // C2893
}

int main() {
   map<int,int> m;
   bar(m);
}
```
