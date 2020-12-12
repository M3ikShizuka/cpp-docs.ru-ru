---
description: 'Дополнительные сведения о: domain_error классе'
title: Класс domain_error
ms.date: 11/04/2016
f1_keywords:
- stdexcept/std::domain_error
helpviewer_keywords:
- domain_error class
ms.assetid: a1d8245d-61c2-4d1e-973f-073bd5dd5fa3
ms.openlocfilehash: 337df7c7c8e2327a4e5b88a45a736c697e6cb1bc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324492"
---
# <a name="domain_error-class"></a>Класс domain_error

Этот класс служит базовым классом для всех исключений, создаваемых для сообщения об ошибке в домене.

## <a name="syntax"></a>Синтаксис

```cpp
class domain_error : public logic_error {
public:
    explicit domain_error(const string& message);

    explicit domain_error(const char *message);

};
```

## <a name="remarks"></a>Remarks

Значение, возвращаемое, `what()` является копией `message.data()` . Дополнительные сведения см. в разделах [`what`](../standard-library/exception-class.md) и [`data`](../standard-library/basic-string-class.md#data).

## <a name="example"></a>Пример

```cpp
// domain_error.cpp
// compile with: /EHsc /GR
#include <iostream>

using namespace std;

int main( )
{
   try
   {
      throw domain_error( "Your domain is in error!" );
   }
   catch (exception &e)
   {
      cerr << "Caught: " << e.what( ) << endl;
      cerr << "Type: " << typeid(e).name( ) << endl;
   };
}
/* Output:
Caught: Your domain is in error!
Type: class std::domain_error
*/
```

## <a name="requirements"></a>Требования

**Заголовок:**\<stdexcept>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Класс logic_error](../standard-library/logic-error-class.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
