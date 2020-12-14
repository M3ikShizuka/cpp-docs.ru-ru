---
description: 'Дополнительные сведения: простые классы типов данных'
title: Классы простых типов данных
ms.date: 11/04/2016
f1_keywords:
- vc.classes.data
helpviewer_keywords:
- scalar classes [MFC]
- data classes [MFC]
- simple data type classes [MFC]
ms.assetid: 0d591d68-0a33-49e9-8a6d-90c90de5c16a
ms.openlocfilehash: 4ce6e799cc30dddde18a50802e01c872c54d1d3a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216968"
---
# <a name="simple-data-type-classes"></a>Классы простых типов данных

Следующие классы инкапсулируют координаты рисования, символьные строки и сведения о времени и датах, позволяя удобно использовать синтаксис C++. Эти объекты широко используются в качестве параметров функций членов классов Windows в библиотеке классов. Поскольку `CPoint` , `CSize` и `CRect` соответствуют структурам **Point**, **SIZE** и **Rect** соответственно, в Windows SDK можно использовать объекты этих классов C++ везде, где можно использовать эти структуры C-Language. Классы предоставляют полезные интерфейсы через их функции-члены. `CStringT` предоставляет очень гибкие динамические строки символов. `CTime`, `COleDateTime` , и `CTimeSpan` `COleTimeSpan` представляют значения времени и даты. Дополнительные сведения об этих классах см. в статье [Дата и время](../atl-mfc-shared/date-and-time.md).

Классы, начинающиеся с " `COle` ", являются инкапсуляцией типов данных, предоставляемых OLE. Эти типы данных могут использоваться в программах Windows независимо от того, используются ли другие функции OLE.

[Класс CStringT](../atl-mfc-shared/reference/cstringt-class.md)<br/>
Содержит символьные строки.

[CTime](../atl-mfc-shared/reference/ctime-class.md)<br/>
Содержит абсолютные значения даты и времени.

[COleDateTime](../atl-mfc-shared/reference/coledatetime-class.md)<br/>
Оболочка для **даты** типа OLE-автоматизации. Представляет значения даты и времени.

[ктимеспан](../atl-mfc-shared/reference/ctimespan-class.md)<br/>
Содержит относительные значения времени и даты.

[коледатетимеспан](../atl-mfc-shared/reference/coledatetimespan-class.md)<br/>
Содержит относительные `COleDateTime` значения, например разницу между двумя `COleDateTime` значениями.

[CPoint](../atl-mfc-shared/reference/cpoint-class.md)<br/>
Содержит координаты координат (x, y).

[CSize](../atl-mfc-shared/reference/csize-class.md)<br/>
Удерживает расстояние, относительное положение или парные значения.

[CRect](../atl-mfc-shared/reference/crect-class.md)<br/>
Содержит координаты прямоугольных областей.

[CImageList](../mfc/reference/cimagelist-class.md)<br/>
Предоставляет функциональные возможности списка образов Windows. Списки изображений используются с элементами управления "список" и "дерево". Они также могут использоваться для хранения и архивации набора точечных рисунков одинакового размера.

[COleVariant](../mfc/reference/colevariant-class.md)<br/>
Оболочка для типа **Variant** OLE Automation Type. Данные в **варианте Variant** s могут храниться во многих форматах.

[COleCurrency](../mfc/reference/colecurrency-class.md)<br/>
Оболочка для **денежного** типа OLE-автоматизации, арифметический тип с фиксированной запятой и 15 цифр перед десятичной запятой и 4 цифры после.

> [!NOTE]
> `CRect`, `CSize` и `CPoint` можно использовать в приложениях ATL или MFC. Кроме того, `CStringT` предоставляет класс, не зависящий `CString` от MFC. Дополнительные сведения о общих классах служебной программы см. в разделе [Общие классы](../atl-mfc-shared/atl-mfc-shared-classes.md).

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../mfc/class-library-overview.md)
