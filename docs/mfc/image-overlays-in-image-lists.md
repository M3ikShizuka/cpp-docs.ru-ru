---
description: 'Дополнительные сведения: наложение изображений в списках изображений'
title: Перекрытия изображений в списках изображений
ms.date: 11/04/2016
helpviewer_keywords:
- overlays [MFC]
- image lists [MFC], image overlays in
- CImageList class [MFC], image overlays in
ms.assetid: aaf4e1c4-cd12-42c8-9af4-1bb458889b4e
ms.openlocfilehash: dd65a27c9ef66311311195c1493e91be8c66d100
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97290119"
---
# <a name="image-overlays-in-image-lists"></a>Перекрытия изображений в списках изображений

Каждый список изображений ([CImageList](reference/cimagelist-class.md)) содержит список изображений для использования в качестве масок наложения. "Маска оверлея" — это изображение, которое прозрачно рисуется на другом изображении. Любой образ можно использовать в качестве маски оверлея. Можно указать до четырех масок оверлея для каждого списка изображений.

Вы добавляете индекс изображения в список масок наложения с помощью функции члена [сетоверлайимаже](reference/cimagelist-class.md#setoverlayimage) , индекса изображения и индекса маски оверлея. Обратите внимание, что индексы для масок наложения основаны на единицах, а не на нуле.

Вы рисуете маску наложения на изображение с помощью одного вызова `Draw` . Параметры включают индекс изображения для рисования и индекс маски оверлея. Для указания индекса маски наложения необходимо использовать макрос [индекстуверлаймаск](/windows/win32/api/commctrl/nf-commctrl-indextooverlaymask) . Можно также указать изображение оверлея при вызове функции члена [дравиндирект](reference/cimagelist-class.md#drawindirect) .

## <a name="see-also"></a>См. также раздел

[Использование CImageList](using-cimagelist.md)<br/>
[Элементы управления](controls-mfc.md)
