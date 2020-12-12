---
description: 'Дополнительные сведения о: буфер обмена: когда следует использовать механизм каждого буфера обмена'
title: Буфер обмена. Выбор механизма буфера обмена
ms.date: 11/04/2016
helpviewer_keywords:
- applications [OLE], Clipboard
- OLE Clipboard, guidelines
- Clipboard [MFC], mechanisms
- OLE Clipboard, formats
- formats [MFC], Clipboard for OLE
- Clipboard [MFC], formats
ms.assetid: fd071996-ef8c-488b-81bd-89057095a201
ms.openlocfilehash: e2fae9fd2af38a9b39c488ec17adf1433edc098c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338406"
---
# <a name="clipboard-when-to-use-each-clipboard-mechanism"></a>Буфер обмена. Выбор механизма буфера обмена

Следуйте этим рекомендациям в работе с буфером обмена:

- Используйте механизм буфера обмена OLE, чтобы включить новые возможности в будущем. Хотя стандартный API буфера обмена будет поддерживаться, механизм OLE является будущим перемещением данных.

- Используйте механизм буфера обмена OLE, если вы пишете приложение OLE или хотите использовать любые функции OLE, такие как перетаскивание.

- Используйте механизм буфера обмена OLE, если вы предоставляете форматы OLE.

## <a name="what-do-you-want-to-do"></a>Что Вы хотите делать

- [Использование механизма буфера обмена OLE](clipboard-using-the-ole-clipboard-mechanism.md)

- [Использование механизма буфера обмена Windows](clipboard-using-the-windows-clipboard.md)

## <a name="see-also"></a>См. также раздел

[Буфер обмена](clipboard.md)
