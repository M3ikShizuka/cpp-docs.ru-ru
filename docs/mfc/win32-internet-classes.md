---
description: 'Дополнительные сведения: Интернет – классы Win32'
title: Классы Win32 для работы в Интернете
ms.date: 09/12/2018
f1_keywords:
- vc.classes.win32
helpviewer_keywords:
- Internet classes [MFC]
- WinInet classes [MFC], classes
- Win32 [MFC], Internet classes
- Windows API [MFC], Internet classes
ms.assetid: b49601d5-3025-4068-9408-316b54ee4375
ms.openlocfilehash: 8b6acad5f867444c33ed86cb7e70f4f1eec42df0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97197482"
---
# <a name="win32-internet-classes"></a>Классы Win32 для работы в Интернете

MFC создает оболочку для Интернета (WinInet) и технологии ActiveX, чтобы упростить Интернет-программирование.

>[!IMPORTANT]
> ActiveX — это устаревшая технология, которую не следует использовать для новой разработки. Дополнительные сведения о современных технологиях, которые заменяют ActiveX, см. в разделе [элементы управления ActiveX](activex-controls.md).

[CInternetSession](../mfc/reference/cinternetsession-class.md)<br/>
Создает и инициализирует один сеанс Интернета или несколько одновременных сеансов Интернета и, при необходимости, описывает подключение к прокси-серверу.

[CInternetConnection](../mfc/reference/cinternetconnection-class.md)<br/>
Управление подключением к интернет-серверу.

[CInternetFile](../mfc/reference/cinternetfile-class.md)<br/>
Этот класс и его производные классы разрешают доступ к файлам в удаленных системах, использующих протоколы Интернета.

[CHttpConnection](../mfc/reference/chttpconnection-class.md)<br/>
Управление подключением к HTTP-серверу.

[CHttpFile](../mfc/reference/chttpfile-class.md)<br/>
Предоставляет функциональные возможности для поиска и чтения файлов на HTTP-сервере.

[CGopherFile](../mfc/reference/cgopherfile-class.md)<br/>
Обеспечивает возможность поиска и чтения файлов на сервере gopher.

[CFtpConnection](../mfc/reference/cftpconnection-class.md)<br/>
Управляет подключением к FTP-серверу.

[CGopherConnection](../mfc/reference/cgopherconnection-class.md)<br/>
Управляет подключением к серверу Gopher.

[CFileFind](../mfc/reference/cfilefind-class.md)<br/>
Выполняет локальный поиск файлов и в Интернете.

[CFtpFileFind](../mfc/reference/cftpfilefind-class.md)<br/>
Помогает в поиске файлов Интернета на FTP-серверах.

[CGopherFileFind](../mfc/reference/cgopherfilefind-class.md)<br/>
Помогает в поиске файлов Интернета на серверах gopher.

[CGopherLocator](../mfc/reference/cgopherlocator-class.md)<br/>
Получает средство поиска gopher с сервера gopher, определяет тип средства поиска и предоставляет средство поиска `CGopherFileFind`.

[CInternetConnection](../mfc/reference/cinternetexception-class.md)<br/>
Представляет условие исключения, касающееся интернет-операции.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../mfc/class-library-overview.md)
