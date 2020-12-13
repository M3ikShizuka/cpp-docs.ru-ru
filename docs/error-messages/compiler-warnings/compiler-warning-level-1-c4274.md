---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4274'
title: Предупреждение компилятора (уровень 1) C4274
ms.date: 11/04/2016
f1_keywords:
- C4274
helpviewer_keywords:
- C4274
ms.assetid: 5a948680-7ed1-469f-978d-ae99d154e161
ms.openlocfilehash: aa1f6d3b07c7d788d9e47955c4bb51930522b7a3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340103"
---
# <a name="compiler-warning-level-1-c4274"></a>Предупреждение компилятора (уровень 1) C4274

\#Ident игнорируется; #pragma комментарий (exestr, "String") см. в документации.

`#ident`Директива, которая вставляет указанную пользователем строку в объект или исполняемый файл, является устаревшей. Следовательно, компилятор игнорирует директиву.

> [!CAUTION]
> Предупреждение C4274 рекомендует использовать директиву [комментария #pragma (exestr, "String")](../../preprocessor/comment-c-cpp.md) . Однако этот Совет является устаревшим и будет пересмотрен в будущих выпусках компилятора. При использовании `#pragma` директивы средство компоновщика (LINK.exe) игнорирует запись комментария, созданную директивой, и выдает предупреждение [LNK4229](../../error-messages/tool-errors/linker-tools-warning-lnk4229.md). Вместо `#ident` директивы рекомендуется использовать в приложении строку ресурса версии файла.

## <a name="to-correct-this-error"></a>Исправление ошибки

- Удалите `#ident "`  `"` директиву строки.

## <a name="see-also"></a>См. также раздел

[comment (C/C++)](../../preprocessor/comment-c-cpp.md)<br/>
[Предупреждение средств компоновщика LNK4229](../../error-messages/tool-errors/linker-tools-warning-lnk4229.md)<br/>
[Работа с файлами ресурсов](../../windows/working-with-resource-files.md)
