---
description: Дополнительные сведения о семантике CString
title: Семантика CString
ms.date: 11/04/2016
helpviewer_keywords:
- semantics in Cstring
- CString objects, assignment semantics
- assignment statements, assigning CString objects
ms.assetid: d4023480-526f-499a-85f6-324b4de5b85f
ms.openlocfilehash: 7c6dde91e7f87908c0c6bc2d49ff455eb79f6eb3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167049"
---
# <a name="cstring-semantics"></a>Семантика CString

Несмотря на то, что объекты [CString](../atl-mfc-shared/reference/cstringt-class.md) являются динамическими объектами, которые могут расти, они работают как встроенные примитивные типы и простые классы. Каждый `CString` объект представляет уникальное значение. `CString` объекты следует рассматривать как фактические строки, а не как указатели на строки.

Можно присвоить один `CString` объект другому. Однако при изменении одного из этих двух `CString` объектов другой `CString` объект не изменяется, как показано в следующем примере:

[!code-cpp[NVC_ATLMFC_Utilities#188](../atl-mfc-shared/codesnippet/cpp/cstring-semantics_1.cpp)]

Обратите внимание, что в примере два `CString` объекта считаются равными, так как они представляют одну и ту же строку символов. `CString`Класс перегружает оператор равенства ( `==` ) для сравнения двух `CString` объектов на основе их значения (содержимого), а не их удостоверения (адреса).

## <a name="see-also"></a>См. также раздел

[Строки (ATL и MFC)](../atl-mfc-shared/strings-atl-mfc.md)
