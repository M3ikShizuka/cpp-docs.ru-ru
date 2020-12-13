---
description: 'Дополнительные сведения: сокеты Windows: наследование от классов сокетов'
title: Сокеты Windows. Наследование от классов сокета
ms.date: 11/04/2016
helpviewer_keywords:
- derived classes [MFC], from socket classes
- Windows Sockets [MFC], deriving from socket classes
- sockets [MFC], deriving from socket classes
ms.assetid: 3a26e67a-e323-433b-9b05-eca018799801
ms.openlocfilehash: ba3526ddde4d254ff044fa09588d7764b16fb719
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97132968"
---
# <a name="windows-sockets-deriving-from-socket-classes"></a>Сокеты Windows. Наследование от классов сокета

В этой статье описываются некоторые функции, которые можно получить, создав собственный класс на основе одного из классов сокетов.

Вы можете создать собственные классы сокетов из [CAsyncSocket](../mfc/reference/casyncsocket-class.md) или [CSocket](../mfc/reference/csocket-class.md) , чтобы добавить собственные функции. В частности, эти классы предоставляют ряд виртуальных функций-членов, которые можно переопределить. К этим функциям относятся [OnReceive](../mfc/reference/casyncsocket-class.md#onreceive), [OnReceive](../mfc/reference/casyncsocket-class.md#onsend), [OnReceive](../mfc/reference/casyncsocket-class.md#onaccept), [OnReceive](../mfc/reference/casyncsocket-class.md#onconnect)и [OnReceive](../mfc/reference/casyncsocket-class.md#onclose). Вы можете переопределить функции в производном классе сокета, чтобы воспользоваться преимуществами уведомлений, которые они предоставляют при возникновении сетевых событий. Платформа вызывает эти функции обратного вызова уведомлений, чтобы уведомлять вас о важных событиях сокета, например о получении данных, которые можно начать читать. Дополнительные сведения о функциях уведомления см. в разделе [сокеты Windows: уведомления сокетов](../mfc/windows-sockets-socket-notifications.md).

Кроме того, класс `CSocket` предоставляет функцию-член [онмессажепендинг](../mfc/reference/csocket-class.md#onmessagepending) (расширенную переопределяемую). MFC вызывает эту функцию, пока сокет перебирает сообщения на основе Windows. Можно переопределить `OnMessagePending` , чтобы искать определенные сообщения в Windows и реагировать на них.

Версия по умолчанию, `OnMessagePending` предоставляемая в классе, `CSocket` проверяет очередь сообщений на наличие WM_PAINT сообщений при ожидании завершения блокирующего вызова. Он отправляет сообщения рисования, чтобы улучшить качество отображения. Помимо выполнения каких-либо полезных действий, это иллюстрирует один из способов переопределения функции. В качестве другого примера рассмотрите возможность использования `OnMessagePending` для следующей задачи. Предположим, что при ожидании завершения сетевой транзакции отображается немодальное диалоговое окно. Диалоговое окно содержит кнопку Отмена, которую пользователь может использовать для отмены блокирующих транзакций, которые занимают слишком много времени. `OnMessagePending`Переопределение может передавать сообщения, связанные с этим немодальным диалоговым окном.

В `OnMessagePending` переопределении возвратите **значение true** или Return из вызова к версии базового класса `OnMessagePending` . Вызовите версию базового класса, если она выполняет работу, которую вы по-прежнему хотите выполнить.

Дополнительные сведения см. в разделе:

- [Сокеты Windows: Использование сокетов с архивами](../mfc/windows-sockets-using-sockets-with-archives.md)

- [Сокеты Windows: использование класса CAsyncSocket](../mfc/windows-sockets-using-class-casyncsocket.md)

- [Сокеты Windows. Блокировка](../mfc/windows-sockets-blocking.md)

- [Сокеты Windows: порядок байтов](../mfc/windows-sockets-byte-ordering.md)

- [Сокеты Windows: преобразование строк](../mfc/windows-sockets-converting-strings.md)

## <a name="see-also"></a>См. также раздел

[Сокеты Windows в MFC](../mfc/windows-sockets-in-mfc.md)
