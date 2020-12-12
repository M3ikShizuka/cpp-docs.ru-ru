---
description: 'Дополнительные сведения: разрывы слов в элементах управления Rich Edit'
title: Разбиение слов с использованием элементов управления "Rich Edit"
ms.date: 11/04/2016
helpviewer_keywords:
- CRichEditCtrl class [MFC], word breaks in
- word breaks
- breaking words in CRichEditCtrl
- rich edit controls [MFC], word breaks in
ms.assetid: 641dcf9e-7b40-4dc0-85f7-575a8c142f73
ms.openlocfilehash: 662a6b8441c4a9041a539acdabcab74f12d52782
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97172717"
---
# <a name="word-breaks-in-rich-edit-controls"></a>Разбиение слов с использованием элементов управления "Rich Edit"

Форматированный элемент управления "поле ввода" ([CRichEditCtrl](../mfc/reference/cricheditctrl-class.md)) вызывает функцию с именем "процедура разрыва слов" для поиска разрывов между словами и определения места, где она может разбивать строки. Этот элемент управления использует эти сведения при выполнении операций переноса по словам и при обработке сочетания клавиш CTRL + LEFT и CTRL + RIGHT. Приложение может отправить сообщения в элемент управления Rich Edit, чтобы заменить процедуру разбиения по словам по умолчанию, получить сведения о разрыве слов и определить линию, на которую попадает заданный символ.

## <a name="see-also"></a>См. также раздел

[Использование CRichEditCtrl](../mfc/using-cricheditctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
