---
description: 'Дополнительные сведения: сокеты Windows: преобразование строк'
title: Сокеты Windows. Преобразование строк
ms.date: 11/04/2016
helpviewer_keywords:
- Windows Sockets [MFC], multibyte character string conversion
- sockets [MFC], multibyte character string conversion issues
- string conversion, multibyte character strings
ms.assetid: 9df522b5-6b23-41e0-bb96-e4e623baf141
ms.openlocfilehash: fe8607647192fadc7f0d5d32d7716c222ff9206f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97118632"
---
# <a name="windows-sockets-converting-strings"></a>Сокеты Windows. Преобразование строк

В этой статье и двух сопутствующих статьях объясняются некоторые проблемы, связанные с программированием Windows Sockets. В этой статье рассматривается преобразование строк. Другие проблемы описаны в разделе [сокеты Windows: Блокировка](../mfc/windows-sockets-blocking.md) и [сокеты Windows: упорядочение байтов](../mfc/windows-sockets-byte-ordering.md).

Если вы используете или наследуете от класса [CAsyncSocket](../mfc/reference/casyncsocket-class.md), вам придется самостоятельно управлять этими проблемами. Если вы используете или наследуете от класса [CSocket](../mfc/reference/csocket-class.md), MFC управляет ими.

## <a name="converting-strings"></a>Преобразование строк

При обмене данными между приложениями, которые используют строки, хранящиеся в разных форматах расширенных символов, таких как Юникод или многобайтовые кодировки (MBCS), или между одним из них и приложением, использующими строки символов ANSI, необходимо самостоятельно управлять преобразованиями в `CAsyncSocket` . `CArchive`Объект, используемый с `CSocket` объектом, управляет этим преобразованием с помощью возможностей класса [CString](../atl-mfc-shared/reference/cstringt-class.md). Дополнительные сведения см. в описании спецификации сокетов Windows, расположенной в Windows SDK.

Дополнительные сведения см. в разделе:

- [Сокеты Windows: использование класса CAsyncSocket](../mfc/windows-sockets-using-class-casyncsocket.md)

- [Сокеты Windows: Использование сокетов с архивами](../mfc/windows-sockets-using-sockets-with-archives.md)

- [Сокеты Windows. Фон](../mfc/windows-sockets-background.md)

- [Сокеты Windows: сокеты потоков](../mfc/windows-sockets-stream-sockets.md)

- [Сокеты Windows: сокеты датаграммы](../mfc/windows-sockets-datagram-sockets.md)

## <a name="see-also"></a>См. также раздел

[Сокеты Windows в MFC](../mfc/windows-sockets-in-mfc.md)
