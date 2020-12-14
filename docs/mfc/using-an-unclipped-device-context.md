---
description: Дополнительные сведения см. в статье Использование необрезанного контекста устройства.
title: Использование необрезанного контекста устройства
ms.date: 11/04/2016
helpviewer_keywords:
- MFC ActiveX controls [MFC], unclipped device context
ms.assetid: 9c020063-73da-4803-bf7b-2e1fd950c9ed
ms.openlocfilehash: 76131d35b108b04caf0b07be8c46e250120f9f62
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202643"
---
# <a name="using-an-unclipped-device-context"></a>Использование необрезанного контекста устройства

Если вы совершенно уверены, что элемент управления не рисуется за пределами клиентского прямоугольника, можно реализовать небольшое, но легко обнаруживаемое увеличение скорости, отключив вызов `IntersectClipRect` , сделанный `COleControl` . Для этого удалите флаг *клиппаинтдк* из набора флагов, возвращаемых [COleControl:: жетконтролфлагс](../mfc/reference/colecontrol-class.md#getcontrolflags). Пример:

[!code-cpp[NVC_MFC_AxOpt#5](../mfc/codesnippet/cpp/using-an-unclipped-device-context_1.cpp)]
[!code-cpp[NVC_MFC_AxOpt#14](../mfc/codesnippet/cpp/using-an-unclipped-device-context_2.cpp)]
[!code-cpp[NVC_MFC_AxOpt#7](../mfc/codesnippet/cpp/using-an-unclipped-device-context_3.cpp)]

Код для удаления этого флага создается автоматически при выборе параметра **контекст необрезанного устройства** на странице [Параметры управления](../mfc/reference/control-settings-mfc-activex-control-wizard.md) при создании элемента управления с помощью мастера элементов управления MFC ActiveX.

Если вы используете безоконную активацию, эта оптимизация не действует.

## <a name="see-also"></a>См. также раздел

[Элементы ActiveX в MFC. Оптимизация](../mfc/mfc-activex-controls-optimization.md)
