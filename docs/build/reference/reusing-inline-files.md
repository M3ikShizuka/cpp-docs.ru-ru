---
description: 'Дополнительные сведения: повторное использование встроенных файлов'
title: Повторное использование подставляемого файла
ms.date: 11/04/2016
helpviewer_keywords:
- inline files, reusing NMAKE
- revising inline files
- NMAKE program, inline files
ms.assetid: d42dbffb-2cef-4ccb-9a1f-20b8ef81481c
ms.openlocfilehash: b95cbd9e85626e1fee7c03dfd5e9b6b5bd0045c5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225015"
---
# <a name="reusing-inline-files"></a>Повторное использование подставляемого файла

Чтобы повторно использовать встроенный файл, укажите <<*имя* файла, в котором он определен и использовался первым, а затем повторно используйте *имя файла* без << позже в той же или другой команде. Команда для создания подставляемого файла должна выполняться перед всеми командами, которые используют этот файл.

## <a name="see-also"></a>См. также раздел

[Встроенные файлы в файле Makefile](inline-files-in-a-makefile.md)
