---
description: 'Дополнительные сведения: командный файл BSCMAKE (файл ответов)'
title: Командный файл BSCMAKE (файл отклика)
ms.date: 11/04/2016
helpviewer_keywords:
- BSCMAKE, response file
- BSCMAKE, command file
- response files, BSCMAKE
- command files, BSCMAKE
- response files
- command files
ms.assetid: abdffeea-35c7-4f2d-8c17-7d0d80bac314
ms.openlocfilehash: 4bb321cd7aa705d7e33d0f539ab3e0aa2e3cb8bf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97187160"
---
# <a name="bscmake-command-file-response-file"></a>Командный файл BSCMAKE (файл отклика)

> [!WARNING]
> Хотя средство BSCMAKE по-прежнему устанавливается вместе с Visual Studio, оно больше не используется в интегрированной среде разработки. Начиная с Visual Studio 2008 информация об исходном коде и символах автоматически сохраняется в SDF-файле SQL Server в папке решения.

Можно указать часть или все входные данные командной строки в командном файле. Укажите командный файл, используя следующий синтаксис:

```
BSCMAKE @filename
```

Допускается только один командный файл. Можно указать путь с *именем файла*. Перед *именем файла* введите знак ( **\@** ). BSCMAKE не предполагает расширение. После *имени файла* можно указать дополнительные *сбрфилес* в командной строке. Командный файл — это текстовый файл, содержащий входные данные для BSCMAKE в том же порядке, в котором они указываются в командной строке. Разделяйте аргументы командной строки одним или несколькими пробелами, знаками табуляции или символами новой строки.

Следующая команда вызывает BSCMAKE с помощью командного файла:

```
BSCMAKE @prog1.txt
```

Ниже приведен пример командного файла.

```
/n /v /o main.bsc /El
/S (
toolbox.h
verdate.h c:\src\inc\screen.h
)
file1.sbr file2.sbr file3.sbr file4.sbr
```

## <a name="see-also"></a>См. также раздел

[Справочник по BSCMAKE](bscmake-reference.md)
