---
description: 'Дополнительные сведения о: использование списков изображений в расширенном элементе управления "поле со списком"'
title: Использование списков изображений в элементе управления "Расширенное поле со списком"
ms.date: 11/04/2016
helpviewer_keywords:
- image lists [MFC], combo boxes
- extended combo boxes [MFC], images
- images [MFC], combo box items
ms.assetid: dfff25fe-af70-47a2-8032-3901d1e6842d
ms.openlocfilehash: 9fb4b70f91a8ffc3d0175ec855cd005de10da280
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97154374"
---
# <a name="using-image-lists-in-an-extended-combo-box-control"></a>Использование списков изображений в элементе управления "Расширенное поле со списком"

Основным компонентом расширенных элементов управления "поле со списком" является возможность связывать изображения из списка изображений с отдельными элементами в элементе управления "поле со списком". Каждый элемент может отображать три разных изображения: один для выбранного состояния, один для его невыбранного состояния, а третий — для изображения оверлея.

Следующая процедура связывает список изображений с расширенным элементом управления "поле со списком":

### <a name="to-associate-an-image-list-with-an-extended-combo-box-control"></a>Связывание списка изображений с расширенным элементом управления "поле со списком"

1. Создайте новый список изображений (или используйте существующий объект списка изображений), используя конструктор [CImageList](../mfc/reference/cimagelist-class.md) и сохранив результирующий указатель.

1. Инициализируйте новый объект списка изображений, вызвав метод [CImageList:: Create](../mfc/reference/cimagelist-class.md#create). Следующий код является одним из примеров этого вызова.

   [!code-cpp[NVC_MFCControlLadenDialog#10](../mfc/codesnippet/cpp/using-image-lists-in-an-extended-combo-box-control_1.cpp)]

1. Добавьте дополнительные изображения для каждого возможного состояния: выбрано или не выбрано и наложение. Следующий код добавляет три стандартных изображения.

   [!code-cpp[NVC_MFCControlLadenDialog#11](../mfc/codesnippet/cpp/using-image-lists-in-an-extended-combo-box-control_2.cpp)]

1. Свяжите список изображений с элементом управления с помощью вызова [CComboBoxEx:: сетимажелист](../mfc/reference/ccomboboxex-class.md#setimagelist).

После того как список изображений будет связан с элементом управления, можно отдельно указать изображения, которые будут использоваться для каждого элемента в трех возможных состояниях. Дополнительные сведения см. [в разделе Установка изображений для отдельного элемента](../mfc/setting-the-images-for-an-individual-item.md).

## <a name="see-also"></a>См. также раздел

[Использование CComboBoxEx](../mfc/using-ccomboboxex.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
