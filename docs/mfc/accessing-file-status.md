---
description: 'Дополнительные сведения: доступ к состоянию файла'
title: Доступ к состоянию файла
ms.date: 11/04/2016
helpviewer_keywords:
- files [MFC], status information
- examples [MFC], file status
- files [MFC], accessing
- file status [MFC]
- status of files [MFC]
ms.assetid: 1b8891d6-eb0f-4037-a837-4928fe595222
ms.openlocfilehash: defff16ddfb8cb5321def898cad451f1e12f1f8c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97169532"
---
# <a name="accessing-file-status"></a>Доступ к состоянию файла

`CFile` также поддерживает получение сведений о состоянии файла, включая наличие файла, дату и время создания и изменения, логический размер и путь.

### <a name="to-get-file-status"></a>Получение состояния файла

1. Используйте класс [кфиле](reference/cfile-class.md) для получения и задания сведений о файле. Одним из полезных приложений является использование `CFile` статической функции-члена с **состоянием** "очень", чтобы определить, существует ли файл. Функция **OnStatus** возвращает 0, если указанный файл не существует.

Таким образом, можно использовать результат с параметром- **Status** , чтобы определить, следует ли использовать флаг **Кфиле:: модекреате** при открытии файла, как показано в следующем примере:

[!code-cpp[NVC_MFCFiles#3](../atl-mfc-shared/reference/codesnippet/cpp/accessing-file-status_1.cpp)]

Связанные сведения см. в разделе [сериализация](serialization-in-mfc.md).

## <a name="see-also"></a>См. также раздел

[Файлы](files-in-mfc.md)
