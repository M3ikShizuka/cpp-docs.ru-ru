---
description: Дополнительные сведения о:/SYMBOLS
title: /SYMBOLS
ms.date: 09/05/2018
f1_keywords:
- /symbols
helpviewer_keywords:
- symbols, dumping
- public symbols
- symbols, displaying COFF symbol table
- symbol tables
- SYMBOLS dumpbin option
- /SYMBOLS dumpbin option
- -SYMBOLS dumpbin option
ms.assetid: 34bcae90-4561-4c77-a80c-065508dec39a
ms.openlocfilehash: f0cc213a8b37f99e0cb80f6df88967e4eb5204b0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230150"
---
# <a name="symbols"></a>/SYMBOLS

```
/SYMBOLS
```

Этот параметр отображает таблицу символов COFF. Таблицы символов существуют во всех объектных файлах. Таблица символов COFF отображается в файле изображения только в том случае, если она связана с/DEBUG.

Ниже приведено описание выходных данных для/СИМБОЛС.. Дополнительные сведения о значении выходных данных/SYMBOLS можно найти в статье Winnt. h (IMAGE_SYMBOL и IMAGE_AUX_SYMBOL) или в документации по COFF.

При наличии следующего образца дампа:

```
Dump of file main.obj
File Type: COFF OBJECT

COFF SYMBOL TABLE
000 00000000 DEBUG    notype       Filename     | .file
    main.cpp
002 000B1FDB ABS      notype       Static       | @comp.id
003 00000000 SECT1    notype       Static       | .drectve
    Section length     26, #relocs    0, #linenums    0, checksum 722C964F
005 00000000 SECT2    notype       Static       | .text
    Section length     23, #relocs    1, #linenums    0, checksum 459FF65F, selection    1 (pick no duplicates)
007 00000000 SECT2    notype ()    External     | _main
008 00000000 UNDEF    notype ()    External     | ?MyDump@@YAXXZ (void __cdecl MyDump(void))

String Table Size = 0x10 bytes

  Summary

         26 .drectve
         23 .text
```

## <a name="remarks"></a>Комментарии

Следующее описание для строк, начинающихся с номера символа, описывает столбцы, имеющие информацию, относящуюся к пользователям:

- Первое число, состоящих из трех цифр, является индексом или номером символа.

- Если третий столбец содержит сект *x*, символ определяется в этом разделе объектного файла. Но если присутствует UNDEF, он не определен в этом объекте и должен быть разрешен в других местах.

- Пятый столбец (статический, внешний) сообщает, является ли символ видимым только в пределах этого объекта, или является ли он открытым (видимым извне). Статический символ, _sym, не будет связан с открытым символом _sym; Это два разных экземпляра функций с именем _sym.

Последним столбцом в нумерованной строке является имя символа, декорированного и недекорированного.

С файлами, созданными с использованием параметра компилятора [/GL](gl-whole-program-optimization.md), можно использовать только параметр DUMPBIN [/HEADERS](headers.md).

## <a name="see-also"></a>См. также раздел

[Параметры DUMPBIN](dumpbin-options.md)
