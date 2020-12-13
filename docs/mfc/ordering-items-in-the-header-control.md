---
description: 'Дополнительные сведения: упорядочивание элементов в элементе управления "заголовок"'
title: Сортировка элементов в элементе управления "Заголовок"
ms.date: 11/04/2016
f1_keywords:
- DS_DRAGDROP
helpviewer_keywords:
- sequence [MFC]
- sequence [MFC], header control items
- OrderToIndex method [MFC]
- DS_DRAGDROP notification [MFC]
- GetOrderArray method [MFC]
- SetOrderArray method [MFC]
- header controls [MFC], ordering items
ms.assetid: 5aaef872-75b5-49c5-8fed-6f9a81fca812
ms.openlocfilehash: 6f6db7b134121c4084d9406ad537bf0ce5dc12cb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330120"
---
# <a name="ordering-items-in-the-header-control"></a>Сортировка элементов в элементе управления "Заголовок"

После [добавления элементов в элемент управления "заголовок](adding-items-to-the-header-control.md)" можно обрабатывать или получать сведения о их заказе с помощью следующих функций:

- [CHeaderCtrl:: жетордераррай](reference/cheaderctrl-class.md#getorderarray) и [CHeaderCtrl:: сетордераррай](reference/cheaderctrl-class.md#setorderarray)

   Извлекает и устанавливает порядок элементов заголовка слева направо.

- [CHeaderCtrl:: ордертоиндекс](reference/cheaderctrl-class.md#ordertoindex).

   Извлекает значение индекса для определенного элемента заголовка.

В дополнение к предыдущим функциям элементов, стиль HDS_DRAGDROP позволяет пользователю перетаскивать элементы заголовка в элементе управления заголовка. Дополнительные сведения см. в разделе [предоставление поддержки перетаскивания для элементов заголовка](providing-drag-and-drop-support-for-header-items.md).

## <a name="see-also"></a>См. также раздел

[Использование CHeaderCtrl](using-cheaderctrl.md)
