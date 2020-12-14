---
description: 'Дополнительные сведения о: использование списка изображений'
title: Использование списка изображений
ms.date: 11/04/2016
helpviewer_keywords:
- lists [MFC], image
- CImageList class [MFC], using
- image lists [MFC]
ms.assetid: e0aed188-a1e6-400e-9f51-033d61c5541f
ms.openlocfilehash: 92587bd80a4f613a04cae22322ab258e9869d247
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202695"
---
# <a name="using-an-image-list"></a>Использование списка изображений

Типичное использование списка изображений соответствует шаблону, приведенному ниже.

- Создайте объект [CImageList](../mfc/reference/cimagelist-class.md) и вызовите одну из перегрузок его функции [CREATE](../mfc/reference/cimagelist-class.md#create) , чтобы создать список изображений и присоединить его к `CImageList` объекту.

- Если вы не добавили образы при создании списка образов, добавьте изображения в список изображений, вызвав функцию [добавления](../mfc/reference/cimagelist-class.md#add) или [чтения](../mfc/reference/cimagelist-class.md#read) члена.

- Свяжите список изображений с элементом управления, вызвав соответствующую функцию-член этого элемента управления или нарисуйте изображения из списка изображений самостоятельно с помощью функции-члена [Draw](../mfc/reference/cimagelist-class.md#draw) в списке изображений.

- Возможно, пользователь может перетащить изображение, используя встроенную поддержку перетаскивания списка изображений.

> [!NOTE]
> Если список изображений был создан с помощью **`new`** оператора, то `CImageList` при завершении его создания необходимо уничтожить объект.

## <a name="see-also"></a>См. также раздел

[Использование CImageList](../mfc/using-cimagelist.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
