---
description: Дополнительные сведения о создании элемента управления "Календарь на месяц"
title: Создание элемента управления "Календарь на месяц"
ms.date: 11/04/2016
helpviewer_keywords:
- CMonthCalCtrl class [MFC], creating
- month calendar controls [MFC], creating
- month calendar controls [MFC]
ms.assetid: 185cc642-85e9-4365-8a4c-d90b75b010f7
ms.openlocfilehash: 98c707e16f05a8f5e4d3b42e3c9504f74e4aca29
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97309528"
---
# <a name="creating-the-month-calendar-control"></a>Создание элемента управления "Календарь на месяц"

Создание элемента управления "Календарь на месяц" зависит от того, используется ли элемент управления в диалоговом окне или создается в диалоговом окне.

### <a name="to-use-cmonthcalctrl-directly-in-a-dialog-box"></a>Использование CMonthCalCtrl непосредственно в диалоговом окне

1. В редакторе диалоговых окон добавьте элемент управления "календарь месяца" в ресурс шаблона диалогового окна. Укажите идентификатор элемента управления.

1. Укажите все необходимые стили, используя диалоговое окно Свойства элемента управления ' календарь на месяц '.

1. Используйте [Мастер добавления переменной-члена](../ide/adding-a-member-variable-visual-cpp.md) , чтобы добавить переменную члена типа [CMonthCalCtrl](reference/cmonthcalctrl-class.md) с помощью свойства Control. Этот элемент можно использовать для вызова `CMonthCalCtrl` функций членов.

1. Используйте [мастер классов](reference/mfc-class-wizard.md) для сопоставления функций обработчика в классе диалогового окна для любых сообщений с уведомлениями об управлении календарем месяца, которые необходимо обменять (см. раздел [сопоставление сообщений с функциями](reference/mapping-messages-to-functions.md)).

1. В [онинитдиалог](reference/cdialog-class.md#oninitdialog)задайте дополнительные стили для `CMonthCalCtrl` объекта.

### <a name="to-use-cmonthcalctrl-in-a-nondialog-window"></a>Использование CMonthCalCtrl в недиалоговом окне

1. Определите элемент управления в классе представления или окна.

1. Вызовите функцию-член [CREATE](reference/cmonthcalctrl-class.md#create) элемента управления, возможно, в [онинитиалупдате](reference/cview-class.md#oninitialupdate), которая может быть раньше, чем функция обработчика [OnCreate](reference/cwnd-class.md#oncreate) родительского окна (если вы подклассировать элемент управления). Задайте стили для элемента управления.

## <a name="see-also"></a>См. также раздел

[Использование CMonthCalCtrl](using-cmonthcalctrl.md)<br/>
[Элементы управления](controls-mfc.md)
