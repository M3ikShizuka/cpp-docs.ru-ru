---
description: 'Дополнительные сведения: потоковые операции в элементах управления Rich Edit'
title: Потоковые операции с использованием элементов управления "Rich Edit"
ms.date: 11/04/2016
helpviewer_keywords:
- CRichEditCtrl class [MFC], stream operations
- CRichEditCtrl class [MFC], stream storage
- rich edit controls [MFC], stream operations
- storage, stream in CRichEditCtrl
- stream operations in CRichEditCtrl
- stream storage and CRichEditCtrl
ms.assetid: 110b4684-1e76-4ca6-9ef0-5bc8b2d93c78
ms.openlocfilehash: 3f9dcfb837d9a4f26454a597507712293d3d895c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216487"
---
# <a name="stream-operations-in-rich-edit-controls"></a>Потоковые операции с использованием элементов управления "Rich Edit"

Потоки можно использовать для перемещения данных в элемент управления Rich Edit ([CRichEditCtrl](../mfc/reference/cricheditctrl-class.md)) или из него. Поток определяется структурой [едитстреам](/windows/win32/api/richedit/ns-richedit-editstream) , которая задает буфер и функцию обратного вызова, определяемую приложением.

Для чтения данных в элементе управления Rich Edit (т. е. потоковая передача данных в) используется функция-член [Stream](../mfc/reference/cricheditctrl-class.md#streamin) . Элемент управления вызывает функцию обратного вызова, определяемую приложением, которая каждый раз передает часть данных в буфер.

Чтобы сохранить содержимое элемента управления Rich Edit (то есть потоковая передача данных), можно использовать функцию-член [Streaming](../mfc/reference/cricheditctrl-class.md#streamout) . Элемент управления многократно записывает данные в буфер, а затем вызывает функцию обратного вызова, определенную приложением. Для каждого вызова функция обратного вызова сохраняет содержимое буфера.

## <a name="see-also"></a>См. также раздел

[Использование CRichEditCtrl](../mfc/using-cricheditctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
