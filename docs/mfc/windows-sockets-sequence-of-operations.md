---
description: 'Дополнительные сведения: сокеты Windows: последовательность операций'
title: Сокеты Windows. Последовательность операций
ms.date: 11/04/2016
helpviewer_keywords:
- Windows Sockets [MFC], operations
- Windows Sockets [MFC], stream sockets
- sockets [MFC], stream sockets
- sockets [MFC], operations
- stream sockets [MFC]
ms.assetid: 43ce76f5-aad3-4247-b8a6-16cc7d012796
ms.openlocfilehash: 89870de642abcc8e0584c2c5dc93860eda9785e8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97263378"
---
# <a name="windows-sockets-sequence-of-operations"></a>Сокеты Windows. Последовательность операций

В этой статье показана параллельная последовательность операций для сокета сервера и сокета клиента. Так как сокеты используют `CArchive` объекты, они обязательно являются [потоковыми сокетами](../mfc/windows-sockets-stream-sockets.md).

## <a name="sequence-of-operations-for-a-stream-socket-communication"></a>Последовательность операций для связи сокета потока

До точки конструирования `CSocketFile` объекта следующая последовательность является точной (с различными различиями параметров) для `CAsyncSocket` и `CSocket` . С этого момента последовательность будет строгой `CSocket` . В следующей таблице показана последовательность операций по настройке связи между клиентом и сервером.

### <a name="setting-up-communication-between-a-server-and-a-client"></a>Настройка обмена данными между сервером и клиентом

|Сервер|клиент|
|------------|------------|
|`// construct a socket`<br /><br /> `CSocket sockSrvr;`|`// construct a socket`<br /><br /> `CSocket sockClient;`|
|`// create the SOCKET`<br /><br /> `sockSrvr.Create(nPort);`1,2|`// create the SOCKET`<br /><br /> `sockClient.Create( );`2|
|`// start listening`<br /><br /> `sockSrvr.Listen( );`||
||`// seek a connection`<br /><br /> `sockClient.Connect(strAddr, nPort);`3,4|
|`// construct a new, empty socket`<br /><br /> `CSocket sockRecv;`<br /><br /> `// accept connection`<br /><br /> `sockSrvr.Accept( sockRecv );` 5.0||
|`// construct file object`<br /><br /> `CSocketFile file(&sockRecv);`|`// construct file object`<br /><br /> `CSocketFile file(&sockClient);`|
|`// construct an archive`<br /><br /> `CArchive arIn(&file, CArchive::load);`<br /><br /> -или-<br /><br /> `CArchive arOut(&file, CArchive::store);`<br /><br /> -или Both-|`// construct an archive`<br /><br /> `CArchive arIn(&file, CArchive::load);`<br /><br /> -или-<br /><br /> `CArchive arOut(&file, CArchive::store);`<br /><br /> -или Both-|
|`// use the archive to pass data:`<br /><br /> `arIn >> dwValue;`<br /><br /> -или-<br /><br /> `arOut << dwValue;`6|`// use the archive to pass data:`<br /><br /> `arIn >> dwValue;`<br /><br /> -или-<br /><br /> `arOut << dwValue;`6|

1. Где *nпорт* — номер порта. Дополнительные сведения о портах см. в разделе [сокеты Windows: порты и адреса сокетов](../mfc/windows-sockets-ports-and-socket-addresses.md) .

2. Сервер должен всегда указывать порт, чтобы клиенты могли подключаться. В `Create` вызове иногда также указывается адрес. На стороне клиента используйте параметры по умолчанию, которые запрашивают MFC для использования любого доступного порта.

3. Где *nпорт* — номер порта, а *страддр* — адрес компьютера или IP-адрес.

4. Адреса компьютеров могут иметь несколько форм: "ftp.microsoft.com", "microsoft.com". В IP-адресах используется форма "127.54.67.32" с точками. `Connect`Функция проверяет, является ли адрес цифрой с точками (хотя не проверяет, что это число является допустимой машиной в сети). В противном случае `Connect` принимает имя компьютера одной из других форм.

5. При вызове `Accept` на стороне сервера вы передаете ссылку на новый объект Socket. Сначала необходимо создать этот объект, но не вызывайте `Create` его. Помните, что если объект сокета выходит за пределы области действия, соединение закрывается. MFC подключает новый объект к обработчику **сокета** . Можно создать сокет в стеке, как показано, или в куче.

6. Архив и файл сокета закрываются, когда выходят за пределы области действия. Деструктор объекта сокета также вызывает функцию [Close](../mfc/reference/casyncsocket-class.md#close) -Member для объекта Socket, когда объект выходит из области или удаляется.

## <a name="additional-notes-about-the-sequence"></a>Дополнительные примечания о последовательности

Последовательность вызовов, показанная в предыдущей таблице, предназначена для сокета потока. Сокеты датаграммы, которые не подключены, не нуждаются в вызовах [CAsyncSocket:: Connect](../mfc/reference/casyncsocket-class.md#connect), [Listen](../mfc/reference/casyncsocket-class.md#listen)и [Accept](../mfc/reference/casyncsocket-class.md#accept) (хотя при необходимости можно использовать `Connect` ). Вместо этого, если используется класс `CAsyncSocket` , сокеты датаграммы используют `CAsyncSocket::SendTo` функции и `ReceiveFrom` . (При использовании `Connect` с сокетом датаграмм используются `Send` и `Receive` .) Поскольку не `CArchive` работает с датаграммами, не используйте `CSocket` с архивом, если сокет является датаграммой.

[CSocketFile](../mfc/reference/csocketfile-class.md) не поддерживает все `CFile` функции. `CFile` такие члены `Seek` , как, которые не имеют смысла в связи с сокетами, недоступны. По этой причине некоторые функции MFC по умолчанию `Serialize` несовместимы с `CSocketFile` . Это особенно справедливо для `CEditView` класса. Не пытайтесь сериализовать `CEditView` данные через `CArchive` объект, присоединенный к `CSocketFile` объекту с помощью `CEditView::SerializeRaw` ; Используйте `CEditView::Serialize` вместо него (не задокументировано). Функция [сериализерав](../mfc/reference/ceditview-class.md#serializeraw) ждет, что объект File имеет функции, такие как `Seek` , которые `CSocketFile` не поддерживают.

Дополнительные сведения см. в разделе:

- [Сокеты Windows: Использование сокетов с архивами](../mfc/windows-sockets-using-sockets-with-archives.md)

- [Сокеты Windows: использование класса CAsyncSocket](../mfc/windows-sockets-using-class-casyncsocket.md)

- [Сокеты Windows: порты и адреса сокетов](../mfc/windows-sockets-ports-and-socket-addresses.md)

- [Сокеты Windows: сокеты потоков](../mfc/windows-sockets-stream-sockets.md)

- [Сокеты Windows: сокеты датаграммы](../mfc/windows-sockets-datagram-sockets.md)

## <a name="see-also"></a>См. также раздел

[Сокеты Windows в MFC](../mfc/windows-sockets-in-mfc.md)<br/>
[Класс CSocket](../mfc/reference/csocket-class.md)<br/>
[CAsyncSocket::Create](../mfc/reference/casyncsocket-class.md#create)<br/>
[CAsyncSocket:: Close](../mfc/reference/casyncsocket-class.md#close)
