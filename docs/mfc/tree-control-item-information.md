---
description: 'Дополнительные сведения о: сведения об элементе управления дерева'
title: Сведения об элементе древовидного элемента управления
ms.date: 11/04/2016
helpviewer_keywords:
- tree controls [MFC], item information
- CTreeCtrl class [MFC], item information
ms.assetid: 8dcab855-27de-49e9-95d8-f78ba963ea71
ms.openlocfilehash: ced75bdf6ed6a10e3a34536adf4af0ed1c7e0c86
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97264145"
---
# <a name="tree-control-item-information"></a>Сведения об элементе древовидного элемента управления

Элементы управления "дерево" ([CTreeCtrl](../mfc/reference/ctreectrl-class.md)) имеют ряд функций-членов, которые извлекают сведения об элементах в элементе управления. Функция элемента [Item](../mfc/reference/ctreectrl-class.md#getitem) возвращает некоторые или все данные, связанные с элементом. Эти данные могут включать текст, состояние, изображения, количество дочерних элементов и определяемое приложением 32-разрядное значение данных. Существует также функция [сетитем](../mfc/reference/ctreectrl-class.md#setitem) , которая может задавать некоторые или все данные, связанные с элементом.

Функции элементов [жетитемстате](../mfc/reference/ctreectrl-class.md#getitemstate), [жетитемтекст](../mfc/reference/ctreectrl-class.md#getitemtext), [жетитемдата](../mfc/reference/ctreectrl-class.md#getitemdata)и [GetItemImage](../mfc/reference/ctreectrl-class.md#getitemimage) извлекают отдельные атрибуты элемента. Каждая из этих функций имеет соответствующую функцию Set для установки атрибутов элемента.

Функция члена [жетнекститем](../mfc/reference/ctreectrl-class.md#getnextitem) извлекает элемент управления "дерево", который несет указанную связь с текущим элементом. Эта функция может извлекать родительский элемент, следующий или предыдущий видимый элемент, первый дочерний элемент и т. д. Существуют также функции элементов для обхода дерева: [жетрутитем](../mfc/reference/ctreectrl-class.md#getrootitem), [жетфирствисиблеитем](../mfc/reference/ctreectrl-class.md#getfirstvisibleitem), [жетнекствисиблеитем](../mfc/reference/ctreectrl-class.md#getnextvisibleitem), [жетпреввисиблеитем](../mfc/reference/ctreectrl-class.md#getprevvisibleitem), [жетчилдитем](../mfc/reference/ctreectrl-class.md#getchilditem), [GetNextSiblingItem](../mfc/reference/ctreectrl-class.md#getnextsiblingitem), [GetPrevSiblingItem](../mfc/reference/ctreectrl-class.md#getprevsiblingitem), [GetParentItem](../mfc/reference/ctreectrl-class.md#getparentitem), [GetSelectedItem](../mfc/reference/ctreectrl-class.md#getselecteditem)и [GetDropHilightItem](../mfc/reference/ctreectrl-class.md#getdrophilightitem).

Функция-член [жетитемрект](../mfc/reference/ctreectrl-class.md#getitemrect) извлекает ограничивающий прямоугольник для элемента управления "дерево". Функции-члены [NOCOUNT](../mfc/reference/ctreectrl-class.md#getcount) и [жетвисиблекаунт](../mfc/reference/ctreectrl-class.md#getvisiblecount) извлекают количество элементов в элементе управления "дерево" и число элементов, которые в данный момент видимы в окне элемента управления "дерево" соответственно. Чтобы убедиться, что конкретный элемент виден, вызовите функцию-член [енсуревисибле](../mfc/reference/ctreectrl-class.md#ensurevisible) .

## <a name="see-also"></a>См. также раздел

[Использование CTreeCtrl](../mfc/using-ctreectrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
