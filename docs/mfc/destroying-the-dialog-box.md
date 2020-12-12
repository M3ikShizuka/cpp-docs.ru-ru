---
description: 'Дополнительные сведения о: уничтожение диалогового окна'
title: Уничтожение диалогового окна
ms.date: 11/04/2016
helpviewer_keywords:
- dialog boxes [MFC], deleting
- destruction, dialog box
- dialog boxes [MFC], destroying
- dialog boxes [MFC], removing
- modeless dialog boxes [MFC], destroying
- MFC dialog boxes [MFC], destroying
- modal dialog boxes [MFC], destroying
ms.assetid: dabceee7-3639-4d85-bf34-73515441b3d0
ms.openlocfilehash: f46c86e5f3e869f321b8306470e5821658ceafcb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327850"
---
# <a name="destroying-the-dialog-box"></a>Уничтожение диалогового окна

Модальные диалоговые окна обычно создаются в кадре стека и уничтожаются при завершении функции, создавшей их. Деструктор объекта диалогового окна вызывается, когда объект выходит из области действия.

Модальные диалоговые окна обычно создаются и принадлежат родительскому представлению или окну фрейма — главному фрейму приложения или окну фрейма документа. Обработчик [OnClose](reference/cwnd-class.md#onclose) по умолчанию вызывает [дестройвиндов](reference/cwnd-class.md#destroywindow), который уничтожает окно диалогового окна. Если диалоговое окно является единственным, без указателей на него или другой особой семантики владения, следует переопределить [постнкдестрой](reference/cwnd-class.md#postncdestroy) для уничтожения объекта диалогового окна C++. Следует также переопределить метод [OnCancel](reference/cdialog-class.md#oncancel) и вызвать `DestroyWindow` из него. В противном случае владелец диалогового окна должен уничтожить объект C++, когда он больше не нужен.

## <a name="see-also"></a>См. также раздел

[Работа с диалоговыми окнами в MFC](life-cycle-of-a-dialog-box.md)
