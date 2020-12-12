---
description: 'Дополнительные сведения: правила Batch-Mode'
title: Правила пакетного режима
ms.date: 11/04/2016
helpviewer_keywords:
- inference rules in NMAKE
- NMAKE program, inference rules
- batch-mode inference rules in NMAKE
ms.assetid: 0650b547-ef19-4455-9bba-fa567dcf88f2
ms.openlocfilehash: 73439082b4e2ad8e33b104329d861ddd1919ec63
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97182740"
---
# <a name="batch-mode-rules"></a>Правила пакетного режима

```
{frompath}.fromext{topath}.toext::
   commands
```

Правила вывода пакетного режима предоставляют только один вызов правила вывода, когда N команд проходят через это правило вывода. Без правил вывода в пакетном режиме для вызова требуется N команд. N — число зависимых объектов, которые активируют правило вывода.

Файлы Makefile, содержащие правила вывода в пакетном режиме, должны использовать NMAKE версии 1,62 или более поздней. Чтобы проверить версию NMAKE, запустите макрос _NMAKE_VER, доступный в NMAKE версии 1,62 или более поздней. Этот макрос возвращает строку, представляющую Visual C++ версию продукта.

Единственное синтаксическое отличие от стандартного правила вывода заключается в том, что правило вывода в пакетном режиме завершается двойным двоеточием (::).

> [!NOTE]
> Вызываемое средство должно иметь возможность обрабатывать несколько файлов. Правило вывода пакетного режима должно использовать в `$<` качестве макроса для доступа к зависимым файлам.

Правила вывода пакетного режима могут ускорить процесс сборки. Быстрее предоставлять файлы компилятору в пакетном режиме, так как драйвер компилятора вызывается только один раз. Например, компилятор C и C++ работает лучше при обработке набора файлов, так как он может оставаться резидентным во время процесса.

В следующем примере показано, как использовать правила вывода в пакетном режиме.

```
#
# sample makefile to illustrate batch-mode inference rules
#
O = .
S = .
Objs = $O/foo1.obj $O/foo2.obj $O/foo2.obj $O/foo3.obj $O/foo4.obj
CFLAGS = -nologo

all : $(Objs)

!ifdef NOBatch
{$S}.cpp{$O}.obj:
!else
{$S}.cpp{$O}.obj::
!endif
   $(CC) $(CFLAGS) -Fd$O\ -c $<

$(Objs) :

#end of makefile
```

NMAKE выдает следующие выходные данные без правил вывода в пакетном режиме:

```
E:\tmp> nmake -f test.mak -a NOBatch=1

Microsoft (R) Program Maintenance Utility   Version 7.00.0000
Copyright (C) Microsoft Corp 1988-2001. All rights reserved.
        cl -nologo -Fd.\ -c .\foo1.cpp
foo1.cpp
        cl -nologo -Fd.\ -c .\foo2.cpp
foo2.cpp
        cl -nologo -Fd.\ -c .\foo3.cpp
foo3.cpp
        cl -nologo -Fd.\ -c .\foo4.cpp
foo4.cpp
```

NMAKE создает следующий результат с правилами вывода в пакетном режиме:

```
E:\tmp> nmake -f test.mak -a

Microsoft (R) Program Maintenance Utility   Version 7.00.0000
Copyright (C) Microsoft Corp 1988-2001. All rights reserved.

        cl -nologo -Fd.\ -c .\foo1.cpp .\foo2.cpp .\foo3.cpp .\foo4.cpp
foo1.cpp
foo2.cpp
foo3.cpp
foo4.cpp
Generating Code...
```

## <a name="see-also"></a>См. также раздел

[Правила вывода](inference-rules.md)
