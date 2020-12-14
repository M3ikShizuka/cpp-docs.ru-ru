---
description: Дополнительные сведения о выборе элементов элемента управления "дерево"
title: Выбор элемента древовидного элемента управления
ms.date: 11/04/2016
helpviewer_keywords:
- tree controls [MFC], item selection
- controls [MFC], selecting items in
- CTreeCtrl class [MFC], item selection
- item selection in tree controls
ms.assetid: 7bcb3b16-b9c8-4c06-9350-7bc3c1c5009b
ms.openlocfilehash: 46e1256eea3e8175b996a1b6bdfdd7c1de2739d8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97264041"
---
# <a name="tree-control-item-selection"></a>Выбор элемента древовидного элемента управления

Когда выбор изменяется от одного элемента к другому, элемент управления "дерево" ([CTreeCtrl](../mfc/reference/ctreectrl-class.md)) отправляет [TVN_SELCHANGING](/windows/win32/Controls/tvn-selchanging) и [TVN_SELCHANGED](/windows/win32/Controls/tvn-selchanged) уведомления. Оба уведомления включают значение, указывающее, является ли изменение результатом щелчка мыши или нажатия клавиши. Уведомления также содержат сведения об элементе, который получает выделение, и элементе, который теряет выделение. Эти сведения можно использовать для задания атрибутов элементов, зависящих от состояния выбора элемента. При возврате значения **true** в ответе `TVN_SELCHANGING` предотвращается изменение выбора; возврат значения **false** позволяет изменить.

Приложение может изменить выбор, вызвав функцию члена [селектитем](../mfc/reference/ctreectrl-class.md#selectitem) .

## <a name="see-also"></a>См. также раздел

[Использование CTreeCtrl](../mfc/using-ctreectrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
