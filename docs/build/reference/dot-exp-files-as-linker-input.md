---
description: Дополнительные сведения:. Файлы exp в качестве входных файлов компоновщика
title: EXP-файлы в качестве входных файлов компоновщика
ms.date: 11/04/2016
helpviewer_keywords:
- exporting functions
- import libraries, linker files
- linking [C++], exports
- exporting functions, information about exported functions
- exporting data, export (.exp) files
- functions [C++], exporting
- .exp files [C++]
- EXP files
ms.assetid: 399f5636-0a4d-462e-b500-5f5b9ae5ad22
ms.openlocfilehash: 03104d6b4265484e54373484b6c9bbdabf0e1afc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192815"
---
# <a name="exp-files-as-linker-input"></a>EXP-файлы в качестве входных файлов компоновщика

Файлы экспорта (exp) содержат сведения о экспортированных функциях и элементах данных. Когда LIB создает библиотеку импорта, она также создает EXP файл. EXP-файл используется при связывании программы, которая экспортирует и импортирует из другой программы, либо прямо, либо косвенно. При компоновке с EXP-файлом ссылка не создает библиотеку импорта, так как предполагается, что библиотека уже создана. Дополнительные сведения о файлах EXP и библиотеках импорта см. в разделе [Работа с библиотеками импорта и экспорт файлов](working-with-import-libraries-and-export-files.md).

## <a name="see-also"></a>См. также раздел

[Входные файлы ссылок](link-input-files.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
