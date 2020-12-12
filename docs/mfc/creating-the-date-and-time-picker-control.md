---
description: Дополнительные сведения о создании элемента управления "Выбор даты и времени"
title: Создание элемента выбора даты и времени
ms.date: 11/04/2016
helpviewer_keywords:
- DateTimePicker control [MFC], creating
- CDateTimeCtrl class [MFC], creating
ms.assetid: 764ec2fb-98cd-478b-a5f2-d63f0bb12279
ms.openlocfilehash: 0ead228e98fdcbcfe707fee88c175453808e7047
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97309736"
---
# <a name="creating-the-date-and-time-picker-control"></a>Создание элемента выбора даты и времени

Способ создания элемента управления выбор даты и времени зависит от того, используется ли элемент управления в диалоговом окне или создается в диалоговом окне.

### <a name="to-use-cdatetimectrl-directly-in-a-dialog-box"></a>Использование CDateTimeCtrl непосредственно в диалоговом окне

1. В редакторе диалоговых окон добавьте элемент управления выбора даты и времени в ресурс шаблона диалогового окна. Укажите идентификатор элемента управления.

1. Укажите все необходимые стили, используя диалоговое окно Свойства элемента управления выбор даты и времени.

1. Используйте [Мастер добавления переменной-члена](../ide/adding-a-member-variable-visual-cpp.md) , чтобы добавить переменную члена типа [CDateTimeCtrl](reference/cdatetimectrl-class.md) с помощью свойства Control. Этот элемент можно использовать для вызова `CDateTimeCtrl` функций членов.

1. Используйте [мастер классов](reference/mfc-class-wizard.md) для сопоставления функций обработчика в классе диалогового окна с любыми сообщениями [об](processing-notification-messages-in-date-and-time-picker-controls.md) элементе управления средства выбора даты и времени, которые необходимо обменять (см. раздел [сопоставление сообщений с функциями](reference/mapping-messages-to-functions.md)).

1. В [онинитдиалог](reference/cdialog-class.md#oninitdialog)задайте дополнительные стили для `CDateTimeCtrl` объекта.

### <a name="to-use-cdatetimectrl-in-a-nondialog-window"></a>Использование CDateTimeCtrl в недиалоговом окне

1. Объявите элемент управления в классе представления или окна.

1. Вызовите функцию-член [CREATE](reference/ctabctrl-class.md#create) элемента управления, возможно, в [онинитиалупдате](reference/cview-class.md#oninitialupdate), которая может быть раньше, чем функция обработчика [OnCreate](reference/cwnd-class.md#oncreate) родительского окна (если вы подклассировать элемент управления). Задайте стили для элемента управления.

## <a name="see-also"></a>См. также раздел

[Использование CDateTimeCtrl](using-cdatetimectrl.md)<br/>
[Элементы управления](controls-mfc.md)
