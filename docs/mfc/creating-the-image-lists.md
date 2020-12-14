---
description: 'Дополнительные сведения: создание списков изображений'
title: Создание списков изображений
ms.date: 11/04/2016
helpviewer_keywords:
- CListCtrl class [MFC], creating image lists for
- image lists [MFC], creating for CListCtrl
- lists [MFC], image
ms.assetid: c2768515-deba-49e8-a6f3-5be6482afb19
ms.openlocfilehash: f2776902e7be06161bdbcfad23bd21d9188467f3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97309671"
---
# <a name="creating-the-image-lists"></a>Создание списков изображений

Создание списков изображений одинаково при использовании [CListView](reference/clistview-class.md) или [CListCtrl](reference/clistctrl-class.md).

> [!NOTE]
> Если элемент управления "список" содержит стиль, необходимы только списки изображений `LVS_ICON` .

Класс используется `CImageList` для создания одного или нескольких списков изображений (для значков полного размера, мелких значков и состояний). См. раздел [CImageList](reference/cimagelist-class.md)и [Просмотр списка изображений](/windows/win32/Controls/using-list-view-controls) в Windows SDK.

Вызовите [CListCtrl:: сетимажелист](reference/clistctrl-class.md#setimagelist) для каждого списка изображений. передайте указатель на соответствующий `CImageList` объект.

## <a name="see-also"></a>См. также раздел

[Использование CListCtrl](using-clistctrl.md)<br/>
[Элементы управления](controls-mfc.md)
