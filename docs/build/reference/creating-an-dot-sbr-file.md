---
description: 'Дополнительные сведения: создание. SBR, файл'
title: Создание SBR-файла
ms.date: 11/04/2016
helpviewer_keywords:
- SBR files
- BSCMAKE, input files
- .sbr files
- source browser files
- local symbols in browse information
- symbols
ms.assetid: bdb4b93c-a88a-441a-84fd-01087d03be25
ms.openlocfilehash: 7f3e056418fe1716dc0130330b09c369e9bdceff
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97196923"
---
# <a name="creating-an-sbr-file"></a>Создание SBR-файла

> [!WARNING]
> Хотя средство BSCMAKE по-прежнему устанавливается вместе с Visual Studio, оно больше не используется в интегрированной среде разработки. Начиная с Visual Studio 2008 информация об исходном коде и символах автоматически сохраняется в SDF-файле SQL Server в папке решения.

Входными файлами для BSCMAKE являются SBRs. Компилятор создает SBR-файл для каждого файла объекта (obj), который он компилирует. При сборке или обновлении файла сведений о просмотре все SBR файлы проекта должны быть доступны на диске.

Чтобы создать SBR файла со всеми возможными сведениями, укажите [/fr](fr-fr-create-dot-sbr-file.md).

Чтобы создать SBR файл, который не содержит локальных символов, укажите [/fr](fr-fr-create-dot-sbr-file.md). Если SBR-файлы содержат локальные символы, их можно опустить в файле BSC с помощью [параметра BSCMAKE/ел](bscmake-options.md)`.`

Можно создать SBR-файл без выполнения полной компиляции. Например, можно задать параметр/ZS для компилятора, чтобы выполнить проверку синтаксиса и все еще создать SBR-файл, если задано/FR или/фр.

Процесс сборки может быть более эффективным, если SBR файлы сначала упаковываются для удаления определений без ссылок. Компилятор автоматически упаковывает sbrные файлы.

## <a name="see-also"></a>См. также раздел

[Сборка. BSC файл](building-a-dot-bsc-file.md)
