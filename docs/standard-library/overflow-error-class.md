---
description: 'Дополнительные сведения о: overflow_error классе'
title: Класс overflow_error
ms.date: 11/04/2016
f1_keywords:
- stdexcept/std::overflow_error
helpviewer_keywords:
- overflow_error class
ms.assetid: bae7128d-e36b-4a45-84f1-2f89da441d20
ms.openlocfilehash: 48d30974152089d941e9ba7c36deb2d8db3a2501
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340883"
---
# <a name="overflow_error-class"></a>Класс overflow_error

Этот класс служит базовым для всех исключений, создаваемых для сообщения об арифметическом переполнении.

## <a name="syntax"></a>Синтаксис

```cpp
class overflow_error : public runtime_error {
public:
    explicit overflow_error(const string& message);

    explicit overflow_error(const char *message);

};
```

## <a name="remarks"></a>Remarks

Значение, возвращаемое, `what()` является копией `message.data()` . Дополнительные сведения см. в разделах [`what`](../standard-library/exception-class.md) и [`data`](../standard-library/basic-string-class.md#data).

## <a name="example"></a>Пример

```cpp
// overflow_error.cpp
// compile with: /EHsc /GR
#include <bitset>
#include <iostream>

using namespace std;

int main( )
{
   try
   {
      bitset< 33 > bitset;
      bitset[32] = 1;
      bitset[0] = 1;
      unsigned long x = bitset.to_ulong( );
   }
   catch ( exception &e )
   {
      cerr << "Caught " << e.what( ) << endl;
      cerr << "Type " << typeid( e ).name( ) << endl;
   };
}
/* Output:
Caught bitset<N> overflow
Type class std::overflow_error
*/
```

## <a name="requirements"></a>Требования

**Заголовок:**\<stdexcept>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Класс runtime_error](../standard-library/runtime-error-class.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
