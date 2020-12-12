---
description: 'Дополнительные сведения: точки входа в процедуру Windows'
title: Точки входа процедуры окна
ms.date: 11/04/2016
helpviewer_keywords:
- state management, window procedures
- MFC, managing state data
- window procedure entry points
- entry points, window procedures
ms.assetid: a6b46a7f-6e42-45f2-9ae6-82e19fc57148
ms.openlocfilehash: 2c2e5dc5d37a2e6f187e694d39205c4cd95b3810
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97214485"
---
# <a name="window-procedure-entry-points"></a>Точки входа процедуры окна

Для защиты процедур окна MFC статические ссылки модуля с помощью специальной реализации процедуры окна. Компоновка происходит автоматически при связывании модуля с MFC. В этой процедуре окна используется макрос AFX_MANAGE_STATE для правильной установки действительного состояния модуля, затем вызывается `AfxWndProc` , который, в свою очередь, делегирует `WindowProc` функции-члену соответствующего `CWnd` объекта, производного от.

## <a name="see-also"></a>См. также раздел

[Управление данными состояния модулей MFC](../mfc/managing-the-state-data-of-mfc-modules.md)
