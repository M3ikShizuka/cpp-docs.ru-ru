---
description: 'Дополнительные сведения: оператор do-while (C++)'
title: Выражение do-while (C++)
ms.date: 11/04/2016
f1_keywords:
- do_cpp
helpviewer_keywords:
- do keyword [C++], do-while
- do-while keyword [C++]
- do keyword [C++]
- while keyword [C++], do-while
ms.assetid: e01e6f7c-7da1-4591-87f9-c26ff848e7b0
ms.openlocfilehash: fed7dc3300651dd35326c1eb28e3078538db1301
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97195493"
---
# <a name="do-while-statement-c"></a>Выражение do-while (C++)

Выполняет *инструкцию* повторно, пока указанное условие завершения ( *выражение*) не примет значение 0.

## <a name="syntax"></a>Синтаксис

```
do
   statement
while ( expression ) ;
```

## <a name="remarks"></a>Remarks

Проверка условия завершения выполняется после каждого выполнения цикла. Таким образом, цикл **do-while** выполняется один или несколько раз в зависимости от значения выражения завершения. Выполнение оператора **do-while** также может прерваться, если в теле оператора выполняется оператор [break](../cpp/break-statement-cpp.md), [goto](../cpp/goto-statement-cpp.md) или [return](../cpp/return-statement-cpp.md).

Выражение *expression* должно иметь арифметический тип или тип указателя. Выполнение происходит следующим образом:

1. Выполняется тело оператора.

1. Затем вычисляется значение *expression*. Если выражение *expression* имеет значение false, выполнение оператора **do-while** завершается и управление передается следующему оператору программы. Если *expression* имеет значение true (то есть не равно нулю), процесс повторяется с шага 1.

## <a name="example"></a>Пример

В следующем примере показан оператор **do-while** :

```cpp
// do_while_statement.cpp
#include <stdio.h>
int main()
{
    int i = 0;
    do
    {
        printf_s("\n%d",i++);
    } while (i < 3);
}
```

## <a name="see-also"></a>См. также раздел

[Операторы итерации](../cpp/iteration-statements-cpp.md)<br/>
[Ключевые слова](../cpp/keywords-cpp.md)<br/>
[Оператор while (C++)](../cpp/while-statement-cpp.md)<br/>
[Оператор for (C++)](../cpp/for-statement-cpp.md)<br/>
[Основанное на диапазоне выражение for (C++)](../cpp/range-based-for-statement-cpp.md)
