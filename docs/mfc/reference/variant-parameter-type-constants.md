---
description: 'Дополнительные сведения: константы типа параметра Variant'
title: Константы типа параметра Variant
ms.date: 11/04/2016
f1_keywords:
- VTS_YPOS_HIMETRIC
- VTS_PICTURE
- VTS_FONT
- VTS_XPOS_HIMETRIC
- VTS_XPOS_PIXELS
- VTS_XSIZE_HIMETRIC
- VTS_YPOS_PIXELS
- VTS_TRISTATE
- VTS_HANDLE
- VTS_YSIZE_HIMETRIC
- VTS_COLOR
- VTS_OPTEXCLUSIVE
- VTS_YSIZE_PIXELS
- VTS_XSIZE_PIXELS
helpviewer_keywords:
- VTS_XPOS_HIMETRIC constant [MFC]
- VTS_FONT constant [MFC]
- VTS_XPOS_PIXELS constant [MFC]
- VTS_COLOR constant [MFC]
- Variants [MFC]
- VTS_YPOS_PIXELS constant [MFC]
- VTS_YSIZE_HIMETRIC constant [MFC]
- VTS_YPOS_HIMETRIC constant [MFC]
- Variants, parameter type constants
- Variant data constants [MFC]
- VTS_PICTURE constant [MFC]
- VTS_TRISTATE constant [MFC]
- VTS_XSIZE_HIMETRIC constant [MFC]
- VTS_HANDLE constant [MFC]
- VTS_XSIZE_PIXELS constant [MFC]
- VTS_OPTEXCLUSIVE constant [MFC]
- VTS_YSIZE_PIXELS constant [MFC]
ms.assetid: de99c7a9-7aae-4dc4-b723-40c6380543ab
ms.openlocfilehash: 5bc3dcc8a0a888b21b88700db99b05c0f12a4c5e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97218502"
---
# <a name="variant-parameter-type-constants"></a>Константы типа параметра Variant

В этом разделе перечислены новые константы, указывающие типы параметров Variant, предназначенные для использования с классами элементов управления OLE библиотека Microsoft Foundation Class.

Ниже приведен список констант класса.

## <a name="variant-data-constants"></a><a name="_mfc_variant_data_constants"></a> Константы данных Variant

- VTS_COLOR 32-разрядное целое число, используемое для представления значения цвета RGB.

- VTS_FONT указатель на `IFontDisp` интерфейс объекта ШРИФТА OLE.

- VTS_HANDLE значение обработчика Windows.

- VTS_PICTURE указатель на `IPictureDisp` интерфейс объекта изображения OLE.

- VTS_OPTEXCLUSIVE 16-разрядное значение, используемое для элемента управления, предназначенного для использования в группе элементов управления, например переключателей. Этот тип сообщает контейнеру, что если один элемент управления в группе имеет значение TRUE, все остальные должны быть ЛОЖНЫми.

- VTS_TRISTATE 16-разрядное целое число со знаком, используемое для свойств, которые могут иметь одно из трех возможных значений (выбрано, снято, недоступно), например, флажок.

- VTS_XPOS_HIMETRIC 32-разрядное целое число без знака, используемое для представления расположения вдоль оси x в единицах HIMETRIC.

- VTS_YPOS_HIMETRIC 32-разрядное целое число без знака, используемое для представления расположения вдоль оси y в единицах HIMETRIC.

- VTS_XPOS_PIXELS 32-разрядное целое число без знака, используемое для представления расположения вдоль оси x в пикселях.

- VTS_YPOS_PIXELS 32-разрядное целое число без знака, используемое для представления расположения вдоль оси y в пикселях.

- VTS_XSIZE_PIXELS 32-разрядное целое число без знака, используемое для представления ширины экранного объекта в пикселях.

- VTS_YSIZE_PIXELS 32-разрядное целое число без знака, используемое для представления высоты экранного объекта в пикселях.

- VTS_XSIZE_HIMETRIC 32-разрядное целое число без знака, используемое для представления ширины экранного объекта в единицах HIMETRIC.

- VTS_YSIZE_HIMETRIC 32-разрядное целое число без знака, используемое для представления высоты экранного объекта в единицах HIMETRIC.

    > [!NOTE]
    >  Дополнительные константы типа Variant определены для всех типов Variant, за исключением VTS_FONT и VTS_PICTURE, которые предоставляют указатель на константу данных Variant. Эти константы именуются с помощью `constantname` соглашения VTS_P. Например, VTS_PCOLOR является указателем на VTS_COLORую константу.

## <a name="requirements"></a>Требования

**Заголовок:** afxdisp.h

## <a name="see-also"></a>См. также раздел

[Макросы и глобальные объекты](../../mfc/reference/mfc-macros-and-globals.md)
