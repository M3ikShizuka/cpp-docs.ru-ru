---
description: Дополнительные сведения о двоичных выходных файлах
title: Двоичные выходные файлы
ms.date: 11/04/2016
helpviewer_keywords:
- I/O [C++], binary output files
- files [C++], binary output files
- binary data, binary output files
ms.assetid: 180954af-8cd6-444b-9a76-2f630a3389d8
ms.openlocfilehash: acbefe8eb7f091bf3d323f25ff00464068d9b1f3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97325522"
---
# <a name="binary-output-files"></a>Двоичные выходные файлы

Потоки изначально были разработаны для текста, поэтому по умолчанию установлен режим вывода текста. В текстовом режиме символ перевода строки разворачивается в пару символов возврата каретки и перевода строки. Расширение может вызвать проблемы, как показано ниже:

```cpp
// binary_output_files.cpp
// compile with: /EHsc
#include <fstream>
using namespace std;
int iarray[2] = { 99, 10 };
int main( )
{
    ofstream os( "test.dat" );
    os.write( (char *) iarray, sizeof( iarray ) );
}
```

Можно предположить, что эта программа будет выводить байтовую последовательность {99, 0, 10, 0}; вместо этого она выводит {99, 0, 13, 10, 0}, что приводит к проблемам в программе, ожидающей ввод двоичных данных. Если требуется истинный двоичный вывод, в котором символы записываются без преобразования, можно указать двоичный выход с помощью [](../standard-library/basic-ofstream-class.md#basic_ofstream) `openmode` аргумента конструктора ofstream:

```cpp
// binary_output_files2.cpp
// compile with: /EHsc
#include <fstream>
using namespace std;
int iarray[2] = { 99, 10 };

int main()
{
   ofstream ofs ( "test.dat", ios_base::binary );

   // Exactly 8 bytes written
   ofs.write( (char*)&iarray[0], sizeof(int)*2 );
}
```

## <a name="see-also"></a>См. также раздел

[Выходные потоки](../standard-library/output-streams.md)
