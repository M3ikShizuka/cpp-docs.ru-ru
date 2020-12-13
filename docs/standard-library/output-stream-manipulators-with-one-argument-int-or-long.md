---
description: 'Дополнительные сведения: выходные потоковые манипуляторы с одним аргументом (int или long)'
title: Манипуляторы потока вывода с одним аргументом (int или long)
ms.date: 11/04/2016
helpviewer_keywords:
- output streams, int or long argument manipulators
ms.assetid: 338f3164-b5e2-4c5a-a605-7d9dc3629ca1
ms.openlocfilehash: e04486f7d207731d9fbf7ba8083ffcb02a82ba8a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340896"
---
# <a name="output-stream-manipulators-with-one-argument-int-or-long"></a>Манипуляторы потока вывода с одним аргументом (int или long)

Библиотека классов iostream предоставляет набор макросов для создания параметризованных манипуляторов. **`int`** **`long`** Особым случаем являются манипуляторы с одним аргументом или. Чтобы создать манипулятор потока вывода, принимающий один **`int`** **`long`** аргумент или (например `setw` ,), необходимо использовать макрос _Smanip, который определен в \<iomanip> . В этом примере определяется манипулятор `fillblank`, который вставляет в поток заданное число пробелов.

## <a name="example"></a>Пример

```cpp
// output_stream_manip.cpp
// compile with: /GR /EHsc
#include <iostream>
#include <iomanip>
using namespace std;

void fb( ios_base& os, int l )
{
   ostream *pos = dynamic_cast<ostream*>(&os);
   if (pos)
   {
      for( int i=0; i < l; i++ )
      (*pos) << ' ';
   };
}

_Smanip<int>
   __cdecl fillblank(int no)
   {
   return (_Smanip<int>(&fb, no));
   }

int main( )
{
   cout << "10 blanks follow" << fillblank( 10 ) << ".\n";
}
```

## <a name="see-also"></a>См. также раздел

[Пользовательские манипуляторы с аргументами](../standard-library/custom-manipulators-with-arguments.md)
