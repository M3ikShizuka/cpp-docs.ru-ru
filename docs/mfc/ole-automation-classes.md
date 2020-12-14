---
description: 'Дополнительные сведения: классы OLE Automation'
title: Классы автоматизации OLE
ms.date: 11/04/2016
helpviewer_keywords:
- Automation, classes
- Automation classes [MFC], OLE classes
- OLE Automation [MFC], classes
- Automation classes [MFC]
- OLE Automation [MFC]
ms.assetid: 96e5372b-ff8a-4da1-933b-4d9bbf4dceb3
ms.openlocfilehash: 588c684d17eb358183097cd4ed62432f334e3f0f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97275572"
---
# <a name="ole-automation-classes"></a>Классы автоматизации OLE

Эти классы поддерживают клиентов автоматизации (приложений, управляющих другими приложениями). Серверы автоматизации (приложения, которые могут управляться другими приложениями) поддерживаются с помощью [карт диспетчеризации](reference/dispatch-maps.md).

[COleDispatchDriver](reference/coledispatchdriver-class.md)<br/>
Используется для вызова серверов автоматизации из клиента автоматизации. При добавлении класса этот класс используется для создания строго типизированных классов для серверов автоматизации, предоставляющих библиотеку типов.

[COleDispatchException](reference/coledispatchexception-class.md)<br/>
Исключение, полученное в результате ошибки при OLE Automation. Исключения автоматизации генерируются серверами службы автоматизации и перехватываются клиентами автоматизации.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](class-library-overview.md)
