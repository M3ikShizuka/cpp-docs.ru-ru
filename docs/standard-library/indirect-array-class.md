---
description: 'Дополнительные сведения о: indirect_array классе'
title: Класс indirect_array
ms.date: 11/04/2016
f1_keywords:
- valarray/std::indirect_array
helpviewer_keywords:
- indirect_array class
ms.assetid: 10e1eaea-ba5a-405c-a25e-7bdd3eee7fc7
ms.openlocfilehash: 47c9a0e604fd9873d7705f70624e67d9b3a22a7a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324045"
---
# <a name="indirect_array-class"></a>Класс indirect_array

Внутренний, вспомогательный шаблон класса, который поддерживает объекты, являющиеся подмножествами объектов valarray, предоставляя операции между массивами подмножества, определенными путем указания подмножества индексов родительского valarray.

## <a name="syntax"></a>Синтаксис

## <a name="remarks"></a>Remarks

Класс описывает объект, хранящий ссылку на объект `va` класса [valarray](../standard-library/valarray-class.md) **\<Type>** , а также объект `xa` класса `valarray<size_t>` , который описывает последовательность элементов для выбора из `valarray<Type>` объекта.

`indirect_array<Type>`Объект создается только путем написания выражения формы `va[xa]` . Функции-члены класса indirect_array ведут себя как соответствующие сигнатуры функций, определенные для `valarray<Type>` , за исключением того, что затрагивается только последовательность выбранных элементов.

Последовательность состоит из **XA.** [Размер](../standard-library/valarray-class.md#size) элементов, элемент Where `I` преобразуется в индекс **XA**[ `I` ] в `va` .

## <a name="example"></a>Пример

```cpp
// indirect_array.cpp
// compile with: /EHsc
#include <valarray>
#include <iostream>

int main( )
{
   using namespace std;
   int i;

   valarray<int> va ( 10 );
   for ( i = 0 ; i < 10 ; i += 2 )
      va [ i ] =  i;
   for ( i = 1 ; i < 10 ; i += 2 )
      va [ i ] =  -1;

   cout << "The initial operand valarray is:  ( ";
      for ( i = 0 ; i < 10 ; i++ )
         cout << va [ i ] << " ";
   cout << ")." << endl;

   // Select 2nd, 4th & 6th elements
   // and assign a value of 10 to them
   valarray<size_t> indx ( 3 );
   indx [0] = 2;
   indx [1] = 4;
   indx [2] = 6;
   va[indx] = 10;

   cout << "The modified operand valarray is:  ( ";
      for (i = 0 ; i < 10 ; i++ )
         cout << va [ i ] << " ";
   cout << ")." << endl;
}
```

### <a name="output"></a>Выходные данные

```cpp
The initial operand valarray is:  (0 -1 2 -1 4 -1 6 -1 8 -1).
The modified operand valarray is:  (0 -1 10 -1 10 -1 10 -1 8 -1).
```

## <a name="requirements"></a>Требования

**Заголовок:**\<valarray>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
