---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4286'
title: Предупреждение компилятора (уровень 1) C4286
ms.date: 11/04/2016
f1_keywords:
- C4286
helpviewer_keywords:
- C4286
ms.assetid: 93eadd6c-6f36-413b-ba91-c9aa2314685a
ms.openlocfilehash: 52a17f66c20efc52f3d12da3a9cfbd041e5f262d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97311777"
---
# <a name="compiler-warning-level-1-c4286"></a>Предупреждение компилятора (уровень 1) C4286

"тип1": перехватывается базовым классом ("тип2") в номере строки

Указанный тип исключения обрабатывается предыдущим обработчиком. Тип второго перехвата является производным от типа первого. Исключения для базового класса перехватывают исключения для производного класса.

## <a name="example"></a>Пример

```cpp
//C4286.cpp
// compile with: /W1
#include <eh.h>
class C {};
class D : public  C {};
int main()
{
    try
    {
        throw "ooops!";
    }
    catch( C ) {}
    catch( D ) {}  // warning C4286, D is derived from C
}
```
