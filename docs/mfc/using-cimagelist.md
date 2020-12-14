---
description: 'Дополнительные сведения о: использование CImageList'
title: Использование CImageList
ms.date: 11/04/2016
helpviewer_keywords:
- image list control
- CImageList class [MFC], using
ms.assetid: 3d2a909e-d641-46b7-aada-81cab1a29b41
ms.openlocfilehash: 9e0126e3d5b083dc4a88bfb1ca2130be0e9fbaaa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202539"
---
# <a name="using-cimagelist"></a>Использование CImageList

Список изображений, представленный классом [CImageList](../mfc/reference/cimagelist-class.md), представляет собой коллекцию изображений одинакового размера, на каждый из которых можно ссылаться по индексу. Списки изображений используются для эффективного управления большими наборами значков или точечных рисунков. Списки изображений не являются элементами управления, так как они не являются окнами Windows; Однако они используются с различными типами элементов управления, включая элементы управления "список" ([CListCtrl](../mfc/reference/clistctrl-class.md)), элементы управления "дерево" ([CTreeCtrl](../mfc/reference/ctreectrl-class.md)) и элементы управления "Вкладка" ([CTabCtrl](../mfc/reference/ctabctrl-class.md)).

Все изображения в списке изображений содержатся в одном расширенном точечном рисунке в формате экранного устройства. Список изображений может также включать монохромное растровое изображение, которое содержит маски, используемые для прозрачного рисования изображений (стиль значка). `CImageList` предоставляет функции элементов, позволяющие рисовать изображения, создавать и уничтожать списки изображений, добавлять и удалять изображения, заменять изображения, объединять изображения и перетаскивать изображения.

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Типы списков изображений](../mfc/types-of-image-lists.md)

- [Использование списка изображений](../mfc/using-an-image-list.md)

- [Управление списками изображений](../mfc/manipulating-image-lists.md)

- [Рисование изображений из списка изображений](../mfc/drawing-images-from-an-image-list.md)

- [Наложение изображений в списках изображений](../mfc/image-overlays-in-image-lists.md)

- [Перетаскивание изображений из списка изображений](../mfc/dragging-images-from-an-image-list.md)

- [Сведения об образе в списках изображений](../mfc/image-information-in-image-lists.md)

## <a name="see-also"></a>См. также раздел

[Элементы управления](../mfc/controls-mfc.md)
