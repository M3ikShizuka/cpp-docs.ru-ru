---
description: Дополнительные сведения см. в статье классы Windows Sockets.
title: Классы сокетов Windows
ms.date: 11/04/2016
helpviewer_keywords:
- sockets classes [MFC]
- Windows Sockets [MFC], classes
ms.assetid: 58b9ab8d-9e44-4db3-8265-e04e713d2e9a
ms.openlocfilehash: 03d8ddae0bb511e52b0ea7ed2b3754184ed6ebc8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97118645"
---
# <a name="windows-sockets-classes"></a>Классы сокетов Windows

Сокеты Windows обеспечивают независимый от сетевого протокола способ связи между двумя компьютерами. Эти сокеты могут быть синхронными (программа ожидает, пока связь не будет выполнена) или асинхронной (программа продолжит выполнение во время обмена данными).

[CAsyncSocket](../mfc/reference/casyncsocket-class.md)<br/>
Инкапсулирует API сокетов Windows в тонкой оболочке.

[CSocket](../mfc/reference/csocket-class.md)<br/>
Абстракция более высокого уровня, производная от `CAsyncSocket` . Он работает синхронно.

[CSocketFile](../mfc/reference/csocketfile-class.md)<br/>
Предоставляет `CFile` интерфейс для сокета Windows.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../mfc/class-library-overview.md)
