---
description: Дополнительные сведения см. в статье изображения в списках изображений.
title: Сведения об изображениях в списках изображений
ms.date: 11/04/2016
helpviewer_keywords:
- CImageList class [MFC], image information in
- image lists [MFC], image information in
ms.assetid: 73c41543-fa91-405d-b15b-0feffa6a72c1
ms.openlocfilehash: c3a5f1cee0a06177d12b72673bf0ebf8e1a73933
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97290145"
---
# <a name="image-information-in-image-lists"></a>Сведения об изображениях в списках изображений

[CImageList](reference/cimagelist-class.md) включает ряд функций, которые извлекают информацию из списка изображений. Функция-член [жетимажеинфо](reference/cimagelist-class.md#getimageinfo) заполняет `IMAGEINFO` структуру сведениями об отдельном изображении, включая маркеры точечных рисунков изображения и маски, число цветовых плоскостей и бит на пиксель, а также ограничивающий прямоугольник изображения в точечном рисунке изображения. Эти сведения можно использовать для непосредственного управления точечными рисунками изображения.

Функция члена [жетимажекаунт](reference/cimagelist-class.md#getimagecount) извлекает количество изображений в списке изображений.

Вы можете создать значок на основе изображения и маски в списке изображений с помощью функции члена [екстрактикон](reference/cimagelist-class.md#extracticon) . Функция возвращает маркер нового значка.

## <a name="see-also"></a>См. также раздел

[Использование CImageList](using-cimagelist.md)<br/>
[Элементы управления](controls-mfc.md)
