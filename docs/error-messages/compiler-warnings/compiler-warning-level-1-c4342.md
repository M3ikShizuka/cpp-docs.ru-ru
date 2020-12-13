---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4342'
title: Предупреждение компилятора (уровень 1) C4342
ms.date: 11/04/2016
f1_keywords:
- C4342
helpviewer_keywords:
- C4342
ms.assetid: 47d4d5ab-069f-4cdc-98c3-10d649577a37
ms.openlocfilehash: f08cf24b0fe429e8b788a20fbcb05d2a8cd8b1d0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340024"
---
# <a name="compiler-warning-level-1-c4342"></a>Предупреждение компилятора (уровень 1) C4342

изменение поведения: вызвана *функция "Function*", но в предыдущих версиях был вызван оператор-член

В версиях Visual C++ до Visual Studio 2002 был вызван элемент, но это поведение было изменено, и компилятор теперь находит наилучшее соответствие в области пространства имен.

Если обнаружен оператор-член, компилятор ранее не рассматривал никаких операторов области пространства имен. Если в области видимости пространства имен есть лучшее совпадение, текущий компилятор правильно вызывает его, тогда как предыдущие компиляторы не рассчитают его.

Это предупреждение следует отключить после успешного переноса кода в текущую версию.  Компилятор может давать ложные срабатывания, создавая это предупреждение для кода, в котором нет изменений в поведении.

Это предупреждение отключено по умолчанию. Дополнительные сведения см. в разделе [Compiler Warnings That Are Off by Default](../../preprocessor/compiler-warnings-that-are-off-by-default.md).

Следующий пример приводит к возникновению ошибки C4342:

```cpp
// C4342.cpp
// compile with: /EHsc /W1
#include <fstream>
#pragma warning(default: 4342)
using namespace std;
struct X : public ofstream {
   X();
};

X::X() {
   open( "ofs_bug_ev.txt." );
   if ( is_open() ) {
      *this << "Text" << "<-should be text" << endl;   // C4342
      *this << ' ' << "<-should be space symbol" << endl;   // C4342
   }
}

int main() {
   X b;
   b << "Text" << "<-should be text" << endl;
   b << ' ' << "<-should be space symbol" << endl;
}
```
