---
description: 'Дополнительные сведения о: runtime_error классе'
title: Класс runtime_error
ms.date: 11/04/2016
f1_keywords:
- stdexcept/std::runtime_error
helpviewer_keywords:
- runtime_error class
ms.assetid: 4d0227bf-847b-45a2-a320-2351ebf98368
ms.openlocfilehash: 6fd4bb843502d72e61afc5617d6a9c160f5cc434
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97148906"
---
# <a name="runtime_error-class"></a>Класс runtime_error

Этот класс служит базовым для всех исключений, создаваемых для сообщения об ошибках, которые можно обнаружить только при выполнении программы.

## <a name="syntax"></a>Синтаксис

```cpp
class runtime_error : public exception {
public:
    explicit runtime_error(const string& message);

    explicit runtime_error(const char *message);

};
```

## <a name="remarks"></a>Remarks

Значение, возвращаемое, `what()` является копией `message.data()` . Дополнительные сведения см. в разделах [`what`](../standard-library/exception-class.md) и [`data`](../standard-library/basic-string-class.md#data).

## <a name="example"></a>Пример

```cpp
// runtime_error.cpp
// compile with: /EHsc /GR
#include <iostream>

using namespace std;

int main( )
{
// runtime_error
   try
   {
      locale loc( "test" );
   }
   catch ( exception &e )
   {
      cerr << "Caught " << e.what( ) << endl;
      cerr << "Type " << typeid( e ).name( ) << endl;
   };
}
/* Output:
Caught bad locale name
Type class std::runtime_error
*/
```

## <a name="requirements"></a>Требования

**Заголовок:**\<stdexcept>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Класс Exception](../standard-library/exception-class.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
