---
description: 'Дополнительные сведения: OLE-и Передача данных классы перетаскивания'
title: Классы перетаскивания и передачи данных OLE
ms.date: 11/04/2016
helpviewer_keywords:
- ActiveX classes [MFC]
- OLE drag and drop [MFC], and data transfer classes
- drag and drop [MFC], classes
- data transfer [MFC], OLE
- data transfer classes [MFC]
ms.assetid: c8ab2825-ed69-4b88-8ae6-f368b94726b8
ms.openlocfilehash: ea19efd05fe4b85a5c0e2ff57412f7eb1d05fcfe
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97244112"
---
# <a name="ole-drag-and-drop-and-data-transfer-classes"></a>Классы перетаскивания и передачи данных OLE

Эти классы используются при передаче данных OLE. Они позволяют передавать данные между приложениями с помощью буфера обмена или перетаскиванием.

[COleDropSource](reference/coledropsource-class.md)<br/>
Управляет операцией перетаскивания от начала до конца. Этот класс определяет, когда начинается операция перетаскивания и когда она завершается. В нем также отображается обратная связь курсора во время операции перетаскивания.

[COleDataSource](reference/coledatasource-class.md)<br/>
Используется, когда приложение предоставляет данные для обмена данными. `COleDataSource` можно просмотреть как объектно-ориентированный объект буфера обмена.

[COleDropTarget](reference/coledroptarget-class.md)<br/>
Представляет целевой объект операции перетаскивания. `COleDropTarget`Объект соответствует окну на экране. Он определяет, следует ли принимать любые данные, переброшенные в него, и реализует фактическую операцию удаления.

[COleDataObject](reference/coledataobject-class.md)<br/>
Используется как получатель на стороне `COleDataSource` . `COleDataObject` объекты предоставляют доступ к данным, хранящимся в `COleDataSource` объекте.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](class-library-overview.md)
