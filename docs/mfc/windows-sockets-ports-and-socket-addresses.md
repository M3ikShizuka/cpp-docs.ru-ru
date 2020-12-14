---
description: 'Дополнительные сведения: сокеты Windows: порты и адреса сокетов'
title: Сокеты Windows. Порты и адреса сокета
ms.date: 11/04/2016
helpviewer_keywords:
- ports [MFC], definition
- Windows Sockets [MFC], ports
- Windows Sockets [MFC], addresses
- ports [MFC]
- addresses [MFC], socket
- sockets [MFC], addresses
- sockets [MFC], ports
ms.assetid: e050261a-9285-4f31-a1c5-6c8033af5b4a
ms.openlocfilehash: 354505796ff60cc8968b2e10a2aac98be2eb4666
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97263404"
---
# <a name="windows-sockets-ports-and-socket-addresses"></a>Сокеты Windows. Порты и адреса сокета

В этой статье объясняются термины "порт" и "адрес", используемые с сокетами Windows.

## <a name="port"></a><a name="_core_port"></a> Порту

Порт определяет уникальный процесс, для которого может быть предоставлена служба. В приведенном контексте порт связан с приложением, которое поддерживает сокеты Windows. Идея состоит в том, чтобы идентифицировать каждое приложение Windows Sockets уникальным образом, чтобы на одном компьютере одновременно выполнялось несколько приложений Windows Sockets.

Некоторые порты зарезервированы для общих служб, таких как FTP. Следует избегать использования этих портов, если вы не предоставляете такую службу. Сведения о зарезервированных портах приведены в спецификации Windows Sockets. Файл WINSOCK. H также перечисляет их.

Чтобы разрешить библиотеке DLL Windows sockets выбрать пригодный для использования порт, в качестве значения порта необходимо передать 0. MFC выбирает значение порта больше 1 024 десятичного числа. Вы можете получить значение порта, выбранное MFC, вызвав функцию члена [CAsyncSocket:: жетсоккнаме](../mfc/reference/casyncsocket-class.md#getsockname) .

## <a name="socket-address"></a><a name="_core_socket_address"></a> Адрес сокета

Каждый объект сокета связан с IP-адресом в сети. Как правило, адрес — это имя компьютера, например "ftp.microsoft.com", или разделенное число, например "128.56.22.8".

При попытке создания сокета обычно не требуется указывать собственный адрес.

> [!NOTE]
> Возможно, на компьютере имеется несколько сетевых карт (или ваше приложение может когда-нибудь на таком компьютере), каждое из которых представляет отдельную сеть. В этом случае может потребоваться указать адрес, указывающий, какой сетевой адаптер будет использоваться сокетом. Это может быть расширено и возможной проблемой переносимости.

Дополнительные сведения см. в разделе:

- [Сокеты Windows: использование класса CAsyncSocket](../mfc/windows-sockets-using-class-casyncsocket.md)

- [Сокеты Windows: Использование сокетов с архивами](../mfc/windows-sockets-using-sockets-with-archives.md)

- [Сокеты Windows: как работают сокеты с архивами](../mfc/windows-sockets-how-sockets-with-archives-work.md)

- [Сокеты Windows: сокеты потоков](../mfc/windows-sockets-stream-sockets.md)

- [Сокеты Windows: сокеты датаграммы](../mfc/windows-sockets-datagram-sockets.md)

## <a name="see-also"></a>См. также раздел

[Сокеты Windows в MFC](../mfc/windows-sockets-in-mfc.md)
