---
description: 'Дополнительные сведения: bad_typeid Exception'
title: Исключение bad_typeid
ms.date: 10/04/2019
f1_keywords:
- bad_typeid
- bad_typeid_cpp
helpviewer_keywords:
- bad_typeid exception
- exceptions [C++], bad_typeid
ms.assetid: 5963ed58-4ede-4597-957d-f7bbd06299c2
ms.openlocfilehash: cdc582e2becba35b851bc3b6c2d68c877110068c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97146267"
---
# <a name="bad_typeid-exception"></a>Исключение bad_typeid

**Bad_typeid** исключение вызывается [оператором typeid](../cpp/typeid-operator.md) , если операнд для **`typeid`** является пустым указателем.

## <a name="syntax"></a>Синтаксис

```
catch (bad_typeid)
   statement
```

## <a name="remarks"></a>Remarks

Интерфейс для **bad_typeid** :

```cpp
class bad_typeid : public exception
{
public:
   bad_typeid();
   bad_typeid(const char * _Message = "bad typeid");
   bad_typeid(const bad_typeid &);
   virtual ~bad_typeid();

   bad_typeid& operator=(const bad_typeid&);
   const char* what() const;
};
```

В следующем примере показано, **`typeid`** как оператор создает исключение **bad_typeid** .

```cpp
// expre_bad_typeid.cpp
// compile with: /EHsc /GR
#include <typeinfo>
#include <iostream>

class A{
public:
   // object for class needs vtable
   // for RTTI
   virtual ~A();
};

using namespace std;
int main() {
A* a = NULL;

try {
   cout << typeid(*a).name() << endl;  // Error condition
   }
catch (bad_typeid){
   cout << "Object is NULL" << endl;
   }
}
```

## <a name="output"></a>Вывод

```Output
Object is NULL
```

## <a name="see-also"></a>См. также

[Сведения о типах времени выполнения](../cpp/run-time-type-information.md)\
[Ключевые слова](../cpp/keywords-cpp.md)
