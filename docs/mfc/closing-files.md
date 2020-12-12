---
description: 'Дополнительные сведения: закрытие файлов'
title: Закрытие файлов
ms.date: 11/04/2016
helpviewer_keywords:
- MFC, file operations
- files [MFC], closing
ms.assetid: 8415a3a8-3c75-45b0-ac2a-d5385f49bdb3
ms.openlocfilehash: e8d2f0792aeb889c40cb516af259fc2a40890a1a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338384"
---
# <a name="closing-files"></a>Закрытие файлов

Как обычно в операциях ввода-вывода, после завершения работы с файлом его необходимо закрыть.

#### <a name="to-close-a-file"></a>Закрытие файла

1. Используйте функцию элемента **Close** . Эта функция закрывает файл файловой системы и очищает буфер при необходимости.

Если объект [кфиле](reference/cfile-class.md) был выделен в кадре (как показано в примере [открытия файлов](opening-files.md)), объект будет автоматически закрыт, а затем уничтожен при выходе из области действия. Обратите внимание, что удаление `CFile` объекта не приводит к удалению физического файла в файловой системе.

## <a name="see-also"></a>См. также раздел

[Файлы](files-in-mfc.md)
