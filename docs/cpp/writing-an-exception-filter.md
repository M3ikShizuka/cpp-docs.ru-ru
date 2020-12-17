---
description: Дополнительные сведения о написании структурированного фильтра исключений.
title: Написание фильтра исключений
ms.date: 12/16/2020
helpviewer_keywords:
- exception handling [C++], filters
ms.openlocfilehash: 8b6706c7dfe0e96e26f77f1f3a452db638141803
ms.sourcegitcommit: 387ce22a3b0137f99cbb856a772b5a910c9eba99
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "97645063"
---
# <a name="writing-an-exception-filter"></a>Написание фильтра исключений

Исключение можно обработать посредством перехода на уровень обработчика исключений или путем продолжения выполнения. Вместо того чтобы использовать код обработчика исключений для обработки исключения и перебора, можно использовать критерий *фильтра* , чтобы устранить проблему. Затем, возвращая `EXCEPTION_CONTINUE_EXECUTION` (-1), вы можете возобновить нормальную последовательность, не очистив стек.

> [!NOTE]
> После некоторых исключений возобновление невозможно. Если для такого исключения *Фильтр* принимает значение-1, система создает новое исключение. При вызове [`RaiseException`](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) определяется, будет ли продолжаться исключение.

Например, следующий код использует вызов функции в критерии *фильтра* : Эта функция обрабатывает проблему, а затем возвращает значение-1, чтобы возобновить нормальный поток управления:

```cpp
// exceptions_Writing_an_Exception_Filter.cpp
#include <windows.h>
int main() {
   int Eval_Exception( int );

   __try {}

   __except ( Eval_Exception( GetExceptionCode( ))) {
      ;
   }

}
void ResetVars( int ) {}
int Eval_Exception ( int n_except ) {
   if ( n_except != STATUS_INTEGER_OVERFLOW &&
      n_except != STATUS_FLOAT_OVERFLOW )   // Pass on most exceptions
   return EXCEPTION_CONTINUE_SEARCH;

   // Execute some code to clean up problem
   ResetVars( 0 );   // initializes data to 0
   return EXCEPTION_CONTINUE_EXECUTION;
}
```

Рекомендуется использовать вызов функции в выражении *фильтра* , когда *Фильтр* должен выполнить все сложнее. Вычисление выражения приводит к выполнению функции, в данном случае — `Eval_Exception`.

Обратите внимание на использование [`GetExceptionCode`](/windows/win32/Debug/getexceptioncode) для определения исключения. Эта функция должна вызываться внутри выражения фильтра **`__except`** инструкции. `Eval_Exception` не удается вызвать `GetExceptionCode` , но ему должен быть передан код исключения.

Если исключение не вызвано переполнением при операции с целыми числами или числами с плавающей запятой, этот обработчик передает управление другому обработчику. В этом случае обработчик вызывает функцию (`ResetVars` — это только пример, а не функция API), чтобы сбросить некоторые глобальные переменные. **`__except`** Блок операторов, который в этом примере пуст, не может быть выполнен, так как `Eval_Exception` никогда не возвращает `EXCEPTION_EXECUTE_HANDLER` (1).

Вызов функции — хороший способ работы со сложными выражениями фильтров. Удобны также две другие возможности языка C:

- условный оператор;

- оператор "запятая".

Условный оператор часто полезен здесь. Его можно использовать для проверки конкретного кода возврата и возврата одного из двух различных значений. Например, фильтр в следующем коде распознает исключение только в том случае, если исключение `STATUS_INTEGER_OVERFLOW` :

```cpp
__except( GetExceptionCode() == STATUS_INTEGER_OVERFLOW ? 1 : 0 ) {
```

Цель условного оператора в этом случае — в основном, обеспечить ясность, так как следующий код дает такие же результаты.

```cpp
__except( GetExceptionCode() == STATUS_INTEGER_OVERFLOW ) {
```

Условный оператор полезнее в ситуациях, когда может потребоваться, чтобы фильтр выдает значение-1, `EXCEPTION_CONTINUE_EXECUTION` .

Оператор "запятая" позволяет выполнять несколько выражений последовательно. Затем он возвращает значение последнего выражения. Например, в следующем коде код исключения сохраняется в переменной и затем проверяется.

```cpp
__except( nCode = GetExceptionCode(), nCode == STATUS_INTEGER_OVERFLOW )
```

## <a name="see-also"></a>См. также раздел

[Написание обработчика исключений](../cpp/writing-an-exception-handler.md)<br/>
[Structured Exception Handling (C/C++)](../cpp/structured-exception-handling-c-cpp.md)
