---
description: 'Дополнительные сведения: классы, связанные с элементами управления Rich Edit'
title: Классы, связанные с элементами управления "Rich Edit"
ms.date: 11/04/2016
helpviewer_keywords:
- rich edit controls [MFC], and CRichEditItem
- CRichEditCtrl class [MFC], related classes
- CRichEditDoc class [MFC], Rich Edit controls
- rich edit controls [MFC], classes related to
- classes [MFC], related to rich edit controls
- rich edit controls [MFC], and CRichEditView
- CRichEditCtrlItem class and CRichEditCtrl
- rich edit controls [MFC], and CRichEditDoc
- CRichEditView class [MFC], and CRichEditCtrl
ms.assetid: 4b31c2cc-6ea1-4146-b7c5-b0b5b419f14d
ms.openlocfilehash: b44c5a874c7f48c132f31483bf5ee73eafbe4da5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97176682"
---
# <a name="classes-related-to-rich-edit-controls"></a>Классы, связанные с элементами управления "Rich Edit"

Классы [CRichEditView](reference/cricheditview-class.md), [CRichEditDoc](reference/cricheditdoc-class.md)и [кричедиткнтритем](reference/cricheditcntritem-class.md) предоставляют функциональные возможности элемента управления Rich Edit ([CRichEditCtrl](reference/cricheditctrl-class.md)) в контексте архитектуры документов и представлений MFC. `CRichEditView` поддерживает текстовую характеристику текста и форматирования текста. `CRichEditDoc` поддерживает список элементов OLE, которые находятся в представлении. `CRichEditCntrItem` предоставляет доступ на стороне контейнера к элементу OLE-клиента. Чтобы изменить содержимое `CRichEditView` , используйте [CRichEditView:: жетричедитктрл](reference/cricheditview-class.md#getricheditctrl) для доступа к базовому элементу управления Rich Edit.

## <a name="see-also"></a>См. также раздел

[Использование CRichEditCtrl](using-cricheditctrl.md)<br/>
[Элементы управления](controls-mfc.md)
