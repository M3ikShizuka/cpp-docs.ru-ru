---
title: Завершение программы C++
description: Узнайте о стандартных способах выхода из программы на языке C++.
ms.date: 12/07/2020
helpviewer_keywords:
- terminating execution
- quitting applications
- exiting applications
- programs [C++], terminating
ms.openlocfilehash: 15d31d8d454f6ac90e012d35ef14e6d6e0a9e29a
ms.sourcegitcommit: 754df5278f795f661d4eeb0d4cacc908aa630159
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2020
ms.locfileid: "96933213"
---
# <a name="c-program-termination"></a>Завершение программы C++

В C++ можно выйти из программы следующими способами:

- Вызовите [`exit`](../c-runtime-library/reference/exit-exit-exit.md) функцию.
- Вызовите [`abort`](../c-runtime-library/reference/abort.md) функцию.
- Выполните [`return`](return-statement-cpp.md) инструкцию из `main` .

## <a name="exit-function"></a>Функция `exit`

[`exit`](../c-runtime-library/reference/exit-exit-exit.md)Функция, объявленная в \<stdlib.h> , завершает программу на C++. Значение, передаваемое в качестве аргумента, `exit` возвращается операционной системе в качестве кода возврата программы или кода выхода. Принято, чтобы нулевым кодом возврата обозначалось, что программа завершена успешно. Константы `EXIT_FAILURE` и `EXIT_SUCCESS` , также определенные в, можно использовать \<stdlib.h> для обозначения успеха или неудачи программы.

Выдача **`return`** инструкции из `main` функции эквивалентна вызову `exit` функции с возвращаемым значением в качестве аргумента.

## <a name="abort-function"></a>Функция `abort`

[`abort`](../c-runtime-library/reference/abort.md)Функция, также объявленная в стандартном включаемом файле \<stdlib.h> , завершает программу на C++. Разница между `exit` и заключается в том `abort` , что `exit` позволяет выполнять обработку завершения при завершении выполнения C++ (вызываются деструкторы глобальных объектов), но `abort` немедленно завершает программу. `abort`Функция обходит обычный процесс уничтожения инициализированных глобальных статических объектов. Он также обходит любую специальную обработку, указанную с помощью [`atexit`](../c-runtime-library/reference/atexit.md) функции.

## <a name="atexit-function"></a>Функция `atexit`

Используйте [`atexit`](../c-runtime-library/reference/atexit.md) функцию, чтобы указать действия, которые выполняются до завершения программы. Глобальные статические объекты, инициализированные до уничтожения вызова `atexit` , не будут уничтожены до выполнения функции выхода.

## <a name="return-statement-in-main"></a>`return` в `main`

Выдача [`return`](return-statement-cpp.md) инструкции из `main` функционально эквивалентна вызову `exit` функции. Рассмотрим следующий пример.

```cpp
// return_statement.cpp
#include <stdlib.h>
int main()
{
    exit( 3 );
    return 3;
}
```

`exit`Операторы и **`return`** в предыдущем примере функционально идентичны. Как правило, для C++ требуются функции, которые возвращают типы, отличные от **`void`** возвращаемых значений. `main`Функция является исключением; она может завершаться без **`return`** оператора. В этом случае он возвращает зависящее от реализации значение для вызывающего процесса. **`return`** Оператор позволяет указать возвращаемое значение из `main` .

## <a name="destruction-of-static-objects"></a>Уничтожение статических объектов

При вызове `exit` или выполнении **`return`** инструкции из `main` статические объекты уничтожаются в обратном порядке их инициализации (после вызова метода, `atexit` если он существует). В следующем примере показано выполнение такого процесса инициализации и удаления.

### <a name="example"></a>Пример

В следующем примере статические объекты `sd1` и `sd2` создаются и инициализируются перед записью в `main` . После завершения выполнения этой программы с помощью **`return`** инструкции сначала `sd2` уничтожается, а затем `sd1` . Деструктор класса `ShowData` закрывает файлы, связанные с этими статическими объектами.

```cpp
// using_exit_or_return1.cpp
#include <stdio.h>
class ShowData {
public:
   // Constructor opens a file.
   ShowData( const char *szDev ) {
   errno_t err;
      err = fopen_s(&OutputDev, szDev, "w" );
   }

   // Destructor closes the file.
   ~ShowData() { fclose( OutputDev ); }

   // Disp function shows a string on the output device.
   void Disp( char *szData ) {
      fputs( szData, OutputDev );
   }
private:
   FILE *OutputDev;
};

//  Define a static object of type ShowData. The output device
//   selected is "CON" -- the standard output device.
ShowData sd1 = "CON";

//  Define another static object of type ShowData. The output
//   is directed to a file called "HELLO.DAT"
ShowData sd2 = "hello.dat";

int main() {
   sd1.Disp( "hello to default device\n" );
   sd2.Disp( "hello to file hello.dat\n" );
}
```

Другой способ записать этот код — объявить объекты `ShowData` с областью видимости блока, в результате чего они будут удаляться при выходе из области.

```cpp
int main() {
   ShowData sd1( "CON" ), sd2( "hello.dat" );

   sd1.Disp( "hello to default device\n" );
   sd2.Disp( "hello to file hello.dat\n" );
}
```

## <a name="see-also"></a>См. также раздел

[`main` аргументы функции и командной строки](main-function-command-line-args.md)
