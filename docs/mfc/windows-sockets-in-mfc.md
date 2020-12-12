---
description: 'Дополнительные сведения: сокеты Windows в MFC'
title: Сокеты Windows в MFC
ms.date: 11/04/2016
helpviewer_keywords:
- WINSOCK.DLL
- sockets [MFC], programming models
- MFC, Windows Sockets
- Windows Sockets [MFC], MFC support
- Windows Sockets [MFC], programming models
- WSOCK32.DLL
- sockets [MFC], MFC
ms.assetid: 1f3c476a-9c68-49fe-9a25-d22971a334d0
ms.openlocfilehash: 9724613fe20abbd53b8f7de6a57723510d37b7f5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97263430"
---
# <a name="windows-sockets-in-mfc"></a>Сокеты Windows в MFC

> [!NOTE]
> MFC поддерживает сокеты Windows 1, но не поддерживает [сокеты Windows 2](/windows/win32/WinSock/windows-sockets-start-page-2). Windows Sockets 2 впервые поставляется с Windows 98 и является версией, входящей в состав Windows 2000.

MFC предоставляет две модели для написания программ сетевого взаимодействия с помощью сокетов Windows, которые в двух классах MFC. В этой статье описываются эти модели и дополнительные сведения о поддержке сокетов MFC. "Socket" — это конечная точка взаимодействия: объект, с помощью которого приложение взаимодействует с другими приложениями Windows Sockets по сети.

Сведения о сокетах Windows, включая описание концепции сокета, см. в разделе [Windows Sockets: Background](../mfc/windows-sockets-background.md).

## <a name="sockets-programming-models"></a><a name="_core_sockets_programming_models"></a> Модели программирования для сокетов

Следующие классы поддерживают две модели программирования сокетов MFC для Windows:

- `CAsyncSocket`

   Этот класс инкапсулирует API-интерфейс сокетов Windows. [CAsyncSocket](../mfc/reference/casyncsocket-class.md) предназначен для программистов, которые узнают о сетевом программировании и хотят обеспечить гибкость программирования непосредственно в API-интерфейсе сокетов, но также хотят, чтобы было удобнее использовать функции обратного вызова для уведомления о сетевых событиях. Кроме упаковки сокетов в объектно-ориентированной форме для использования в C++, единственным дополнительным абстракцией, предоставляемой этим классом, является преобразование определенных сообщений Windows, связанных с сокетом, в обратные вызовы. Дополнительные сведения см. в разделе [сокеты Windows: уведомления сокетов](../mfc/windows-sockets-socket-notifications.md).

- `CSocket`

   Этот класс, производный от `CAsyncSocket` , предоставляет абстракцию более высокого уровня для работы с сокетами через объект MFC [CArchive](../mfc/reference/carchive-class.md) . Использование сокета с архивом очень напоминает использование протокола сериализации файлов MFC. Это упрощает использование, чем `CAsyncSocket` модель. [CSocket](../mfc/reference/csocket-class.md) наследует многие функции-члены `CAsyncSocket` , которые инкапсулируют API-интерфейсы сокетов Windows. вам придется использовать некоторые из этих функций и разбираться в обычном программировании для сокетов. Но `CSocket` управляет многими аспектами взаимодействия, которые нужно было бы сделать с помощью необработанного API или класса `CAsyncSocket` . Что важнее всего, `CSocket` предоставляет блокировку (с фоновой обработкой сообщений Windows), которая важна для синхронной работы `CArchive` .

Создание и использование `CSocket` `CAsyncSocket` объектов и описывается в разделе [сокеты Windows: Использование сокетов с архивами](../mfc/windows-sockets-using-sockets-with-archives.md) и [сокетами Windows: использование класса CAsyncSocket](../mfc/windows-sockets-using-class-casyncsocket.md).

## <a name="windows-sockets-dlls"></a><a name="_core_mfc_socket_samples_and_windows_sockets_dlls"></a> DLL-библиотеки сокетов Windows

Операционные системы Microsoft Windows предоставляют библиотеки динамической компоновки Windows Sockets (DLL). Visual C++ предоставляет соответствующие файлы заголовков и библиотеки, а также спецификацию сокетов Windows.

Дополнительные сведения о сокетах Windows см. в следующих статьях:

- [Сокеты Windows: сокеты потоков](../mfc/windows-sockets-stream-sockets.md)

- [Сокеты Windows: сокеты датаграммы](../mfc/windows-sockets-datagram-sockets.md)

- [Сокеты Windows: Использование сокетов с архивами](../mfc/windows-sockets-using-sockets-with-archives.md)

- [Сокеты Windows: последовательность операций](../mfc/windows-sockets-sequence-of-operations.md)

- [Сокеты Windows. пример сокетов с использованием архивов](../mfc/windows-sockets-example-of-sockets-using-archives.md)

- [Сокеты Windows: как работают сокеты с архивами](../mfc/windows-sockets-how-sockets-with-archives-work.md)

- [Сокеты Windows: использование класса CAsyncSocket](../mfc/windows-sockets-using-class-casyncsocket.md)

- [Сокеты Windows: производные от классов сокетов](../mfc/windows-sockets-deriving-from-socket-classes.md)

- [Сокеты Windows: уведомления сокета](../mfc/windows-sockets-socket-notifications.md)

- [Сокеты Windows. Блокировка](../mfc/windows-sockets-blocking.md)

- [Сокеты Windows: порядок байтов](../mfc/windows-sockets-byte-ordering.md)

- [Сокеты Windows: преобразование строк](../mfc/windows-sockets-converting-strings.md)

- [Сокеты Windows: порты и адреса сокетов](../mfc/windows-sockets-ports-and-socket-addresses.md)

## <a name="see-also"></a>См. также раздел

[Сокеты Windows](../mfc/windows-sockets.md)
