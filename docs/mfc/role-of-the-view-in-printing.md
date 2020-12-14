---
description: Дополнительные сведения о роли представления в печати
title: Роль просмотра при печати
ms.date: 11/04/2016
helpviewer_keywords:
- views [MFC], printing
- OnDraw method [MFC], and printing
- printing [MFC], OnDraw method [MFC]
- printing [MFC], views
- CView class [MFC], role in printing
- printing views [MFC]
ms.assetid: 8d4a3c8e-1fce-4edc-b608-94cb5f3e487e
ms.openlocfilehash: b8d59442c6d2214f65bb53788c77df672478f68c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97217904"
---
# <a name="role-of-the-view-in-printing"></a>Роль просмотра при печати

Представление также играет две важные роли при печати связанного с ним документа.

Представление:

- Использует тот же код [OnDraw](../mfc/reference/cview-class.md#ondraw) для рисования на принтере, как при рисовании на экране.

- Управляет разделением документа на страницы для печати.

Дополнительные сведения о печати и о роли представления в выводе на печать см. в разделе [Печать и предварительный просмотр](../mfc/printing-and-print-preview.md).

## <a name="see-also"></a>См. также раздел

[Использование представлений](../mfc/using-views.md)
