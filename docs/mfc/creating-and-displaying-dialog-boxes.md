---
description: 'Дополнительные сведения: создание и отображение диалоговых окон'
title: Создание и отображение диалоговых окон
ms.date: 11/04/2016
helpviewer_keywords:
- modal dialog boxes [MFC], creating
- opening dialog boxes
- modeless dialog boxes [MFC], creating
- MFC dialog boxes [MFC], creating
- MFC dialog boxes [MFC], displaying
ms.assetid: 1c5219ee-8b46-44bc-9708-83705d4f248b
ms.openlocfilehash: 9865e43392021cc7ba1349a73bffb8e47f4cca9d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97309829"
---
# <a name="creating-and-displaying-dialog-boxes"></a>Создание и отображение диалоговых окон

Создание объекта диалогового окна является двухфазной операцией. Сначала создайте объект диалогового окна, а затем — диалоговое окно. Модальные и немодальные диалоговые окна немного отличаются в процессе, который используется для их создания и вывода. В следующей таблице показано, как обычно создаются и отображаются модальные и немодальные диалоговые окна.

### <a name="dialog-creation"></a>Создание диалогового окна

|Тип диалога|Создание|
|-----------------|----------------------|
|[Modeless](creating-modeless-dialog-boxes.md)|Создайте `CDialog` , а затем вызовите `Create` функцию члена.|
|[Модальный режим](creating-modal-dialog-boxes.md)|Создайте `CDialog` , а затем вызовите `DoModal` функцию члена.|

При необходимости можно создать диалоговое окно из созданного [шаблона диалогового окна в памяти](using-a-dialog-template-in-memory.md) , а не из ресурса шаблона диалогового окна. Однако это дополнительная тема.

## <a name="see-also"></a>См. также раздел

[Работа с диалоговыми окнами в MFC](life-cycle-of-a-dialog-box.md)
