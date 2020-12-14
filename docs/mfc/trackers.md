---
description: 'Дополнительные сведения: средства мониторинга'
title: Средства отслеживания
ms.date: 11/04/2016
helpviewer_keywords:
- trackers [MFC]
- OLE applications [MFC], trackers
- applications [OLE], trackers
- tracking OLE items [MFC]
- OLE containers [MFC], trackers
- CDC class [MFC], trackers
- CRectTracker class [MFC], implementing trackers
- OLE server applications [MFC], trackers
ms.assetid: dcd09399-6637-4621-80e5-d12670429787
ms.openlocfilehash: e82766ecfabf2b5ebb0147b9f2c462f3b4460869
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97264251"
---
# <a name="trackers"></a>Средства отслеживания

Класс [кректтраккер](../mfc/reference/crecttracker-class.md) предоставляет пользовательский интерфейс между прямоугольными элементами приложения и пользователем, предоставляя разнообразные стили вывода. К этим стилям относятся сплошные, штриховые или пунктирные границы; заштрихованный шаблон, охватывающий элемент; и размер маркеров, которые могут располагаться снаружи или внутри границы. Инспекторы часто используются вместе с элементами OLE, то есть объектами, производными от `COleClientItem` . Прямоугольники инспектора предоставляют визуальные подсказки о текущем состоянии элемента.

Пример приложения MFC OLE в образце [OCLIENT](../overview/visual-cpp-samples.md) демонстрирует общий интерфейс, использующий средства мониторинга и элементы клиента OLE из точки зрения в приложении-контейнере. Демонстрацию различных стилей и возможностей объекта Tracker см. в разделе [средство регистрации](../overview/visual-cpp-samples.md)общего примера MFC.

Дополнительные сведения о реализации инспекторов в приложении OLE см. в статье средства мониторинга [: реализация инспекторов в приложении OLE](../mfc/trackers-implementing-trackers-in-your-ole-application.md)

## <a name="see-also"></a>См. также раздел

[OLE](../mfc/ole-in-mfc.md)<br/>
[Класс COleClientItem](../mfc/reference/coleclientitem-class.md)
