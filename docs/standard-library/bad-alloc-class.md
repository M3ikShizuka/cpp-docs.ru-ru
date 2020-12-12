---
description: 'Дополнительные сведения о: bad_alloc классе'
title: Класс bad_alloc
ms.date: 11/04/2016
f1_keywords:
- new/std::bad_alloc
helpviewer_keywords:
- bad_alloc class
ms.assetid: 6429a8e6-5a49-4907-8d56-f4a4ec8131d0
ms.openlocfilehash: 1096157e5c69633ee8d4e1c34d98c65775391aca
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321657"
---
# <a name="bad_alloc-class"></a>Класс bad_alloc

Данный класс описывает исключение, возникновение которого указывает на то, что запрос на выделение памяти не выполнен.

## <a name="syntax"></a>Синтаксис

```cpp
class bad_alloc : public exception {
    bad_alloc();
    virtual ~bad_alloc();
    bad_alloc(const bad_alloc&);
    bad_alloc& operator=(const bad_alloc&);
    const char* what() const override;
};
```

## <a name="remarks"></a>Remarks

Значение, возвращаемое, `what` является строкой C, определяемой реализацией. Ни одна из функций-членов не создает исключение.

## <a name="example"></a>Пример

```cpp
// bad_alloc.cpp
// compile with: /EHsc
#include<new>
#include<iostream>
using namespace std;

int main() {
   char* ptr;
   try {
      ptr = new char[(~unsigned int((int)0)/2) - 1];
      delete[] ptr;
   }
   catch( bad_alloc &ba) {
      cout << ba.what( ) << endl;
   }
}
```

```Output
bad allocation
```
