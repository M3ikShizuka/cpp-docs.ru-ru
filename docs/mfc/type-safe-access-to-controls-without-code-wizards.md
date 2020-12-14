---
description: 'Дополнительные сведения: Type-Safe доступ к элементам управления без мастеров кода'
title: Типобезопасный доступ к элементам управления без мастеров кода
ms.date: 11/04/2016
helpviewer_keywords:
- dialog boxes [MFC], accessing controls
- dialog box controls [MFC], accessing
ms.assetid: 325b4927-d49b-42b4-8e0b-fc84f31fb059
ms.openlocfilehash: 1e59353a17f0d841cd69fa64f792dcc7cdbfa6ad
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97263781"
---
# <a name="type-safe-access-to-controls-without-code-wizards"></a>Типобезопасный доступ к элементам управления без мастеров кода

Первый подход к созданию строго типизированного доступа к элементам управления использует встроенную функцию-член для приведения возвращаемого типа `CWnd` функции- `GetDlgItem` члена класса к соответствующему типу элемента управления C++, как показано в следующем примере:

[!code-cpp[NVC_MFCControlLadenDialog#50](../mfc/codesnippet/cpp/type-safe-access-to-controls-without-code-wizards_1.cpp)]

Затем эту функцию-член можно использовать для доступа к элементу управления в строго типизированном виде с кодом, аналогичным следующему:

[!code-cpp[NVC_MFCControlLadenDialog#51](../mfc/codesnippet/cpp/type-safe-access-to-controls-without-code-wizards_2.cpp)]

## <a name="see-also"></a>См. также раздел

[Строго типизированный доступ к элементам управления в диалоговом окне](../mfc/type-safe-access-to-controls-in-a-dialog-box.md)<br/>
[Строго типизированный доступ к элементам управления с помощью мастеров кода](../mfc/type-safe-access-to-controls-with-code-wizards.md)
