---
description: 'Дополнительные сведения: предоставление активации Flicker-Free'
title: Предоставление активации без мерцания
ms.date: 11/04/2016
helpviewer_keywords:
- MFC ActiveX controls [MFC], flicker-free
- flicker, MFC ActiveX controls
- activation [MFC], flicker-free
ms.assetid: bcb24b77-31d8-44a0-8c58-2ea6213b4c43
ms.openlocfilehash: c0af1ccdd4795f55296ff38e0e74bc6492f79eb1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97248831"
---
# <a name="providing-flicker-free-activation"></a>Предоставление активации без мерцания

Если элемент управления сам рисуется в неактивном и активном состояниях (и не использует активацию без окон), можно исключить операции рисования и сопутствующую визуальную мерцание, которая обычно возникает при переходе между неактивным и активным состояниями. Для этого включите флаг **нофликкерактивате** в набор флагов, возвращаемых [COleControl:: жетконтролфлагс](../mfc/reference/colecontrol-class.md#getcontrolflags). Пример:

[!code-cpp[NVC_MFC_AxOpt#5](../mfc/codesnippet/cpp/providing-flicker-free-activation_1.cpp)]
[!code-cpp[NVC_MFC_AxOpt#13](../mfc/codesnippet/cpp/providing-flicker-free-activation_2.cpp)]
[!code-cpp[NVC_MFC_AxOpt#7](../mfc/codesnippet/cpp/providing-flicker-free-activation_3.cpp)]

Код для включения этого флага создается автоматически, если на странице " [Параметры управления](../mfc/reference/control-settings-mfc-activex-control-wizard.md) " при создании элемента управления с помощью мастера элементов управления MFC ActiveX выбран параметр **активации без мерцания** .

Если вы используете безоконную активацию, эта оптимизация не действует.

## <a name="see-also"></a>См. также раздел

[Элементы ActiveX в MFC. Оптимизация](../mfc/mfc-activex-controls-optimization.md)
