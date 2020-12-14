---
description: 'Дополнительные сведения: OLE-Related классы'
title: Классы, связанные с OLE
ms.date: 11/04/2016
helpviewer_keywords:
- ActiveX classes [MFC]
- OLE classes [MFC]
- OLE [MFC], classes
ms.assetid: 2135cf54-1d9d-4e0e-91b4-943b3440effa
ms.openlocfilehash: c54ebbedabc2e44095d06b0e842f7c73d5dbb43e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97244034"
---
# <a name="ole-related-classes"></a>Классы, связанные с OLE

Эти классы предоставляют ряд различных служб, от исключений до входных и выходных файлов.

[COleObjectFactory](reference/coleobjectfactory-class.md)<br/>
Используется для создания элементов по запросу из других контейнеров. Этот класс выступает в качестве базового класса для более конкретных типов фабрик, включая `COleTemplateServer` .

[COleMessageFilter](reference/colemessagefilter-class.md)<br/>
Используется для управления параллелизмом с помощью вызовов OLE-облегченного удаленного вызова процедур (ЛРПК).

[COleStreamFile](reference/colestreamfile-class.md)<br/>
Использует интерфейс COM `IStream` для предоставления `CFile` доступа к составным файлам. Этот класс (производный от `CFile` ) позволяет СЕРИАЛИЗАЦИИ MFC использовать структурированное хранилище OLE.

[CRectTracker](reference/crecttracker-class.md)<br/>
Используется для разрешения перемещения, изменения размера и ориентации элементов на месте.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](class-library-overview.md)
