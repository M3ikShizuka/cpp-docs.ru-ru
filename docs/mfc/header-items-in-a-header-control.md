---
description: Дополнительные сведения о элементах заголовка в элементе управления "заголовок"
title: Элементы заголовка в элементе управления "Заголовок"
ms.date: 11/04/2016
helpviewer_keywords:
- header controls [MFC], header items in
- header items in header controls [MFC]
- CHeaderCtrl class [MFC], header items in
- controls [MFC], header
ms.assetid: ac79ef1f-a671-4ab2-93e9-b1aa016a48bf
ms.openlocfilehash: 4b91ef1395d814b89ff12234b0aa8f2d674512ab
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97172860"
---
# <a name="header-items-in-a-header-control"></a>Элементы заголовка в элементе управления "Заголовок"

У вас есть значительный контроль над внешним видом и поведением элементов заголовка, составляющих элемент управления "заголовок" ([CHeaderCtrl](reference/cheaderctrl-class.md)). Каждый элемент заголовка может иметь строку, Растровое изображение, изображение из связанного списка изображений или определяемое приложением 32-разрядное значение. Строка, точечный рисунок или изображение отображаются в элементе заголовка.

Можно настроить внешний вид и содержимое новых элементов при их создании, вызвав [CHeaderCtrl:: InsertItem](reference/cheaderctrl-class.md#insertitem) или изменив существующий элемент с помощью вызова [CHeaderCtrl::-Item](reference/cheaderctrl-class.md#getitem) и [CHeaderCtrl:: сетитем](reference/cheaderctrl-class.md#setitem).

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Настройка внешнего вида элемента заголовка](customizing-the-header-item-s-appearance.md)

- [Сортировка элементов в элементе управления "Заголовок"](ordering-items-in-the-header-control.md)

- [Предоставление поддержки перетаскивания для элементов заголовка](providing-drag-and-drop-support-for-header-items.md)

- [Использование списков изображений с элементами управления "Заголовок"](using-image-lists-with-header-controls.md)

## <a name="see-also"></a>См. также раздел

[Использование CHeaderCtrl](using-cheaderctrl.md)
