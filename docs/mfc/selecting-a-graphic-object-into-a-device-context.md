---
description: 'Дополнительные сведения: Выбор графического объекта в контексте устройства'
title: Выбор графического объекта в контексте устройства
ms.date: 11/04/2016
helpviewer_keywords:
- graphic objects [MFC], selecting into device context
- SelectObject method [MFC]
- GDI objects [MFC], device contexts
- lifetime, graphic objects [MFC]
- device contexts, selecting graphic objects into
- device contexts, graphic objects [MFC]
ms.assetid: cf54a330-63ef-421f-83eb-90ec7bd82eef
ms.openlocfilehash: cc2aabbcb1614fc77e5eadf9e6fba13ba377a4c7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97217683"
---
# <a name="selecting-a-graphic-object-into-a-device-context"></a>Выбор графического объекта в контексте устройства

Этот раздел относится к использованию графических объектов в контексте устройства окна. После [создания объекта-рисунка](../mfc/one-stage-and-two-stage-construction-of-objects.md)необходимо выбрать его в контексте устройства вместо объекта по умолчанию, хранящегося там:

[!code-cpp[NVC_MFCDocViewSDI#7](../mfc/codesnippet/cpp/selecting-a-graphic-object-into-a-device-context_1.cpp)]

## <a name="lifetime-of-graphic-objects"></a>Время существования графических объектов

Графический объект, возвращаемый функцией [SelectObject](../mfc/reference/cdc-class.md#selectobject) , является временным. Это значит, что он будет удален функцией-членом [OnIdle](../mfc/reference/cwinapp-class.md#onidle) класса `CWinApp` в следующий раз, когда программа получит время простоя. Если вы используете объект, возвращаемый `SelectObject` в одной функции, без возврата управления в главный цикл обработки сообщений, проблема не возникает.

### <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Графические объекты](../mfc/graphic-objects.md)

- [Одноэтапное и двухэтапное создание графических объектов](../mfc/one-stage-and-two-stage-construction-of-objects.md)

- [Контексты устройств](../mfc/device-contexts.md)

- [Рисование в представлении](../mfc/drawing-in-a-view.md)

## <a name="see-also"></a>См. также раздел

[Графические объекты](../mfc/graphic-objects.md)
