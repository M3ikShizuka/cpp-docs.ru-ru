---
description: 'Дополнительные сведения: использование общего элемента управления в качестве дочернего окна'
title: Использование общего элемента управления как дочернего окна
ms.date: 11/04/2016
helpviewer_keywords:
- controls [MFC], using as child windows
- windows [MFC], common controls as
- child windows [MFC], common controls as
- common controls [MFC], child windows
- Windows common controls [MFC], child windows
ms.assetid: 608f7d47-7854-4fce-bde9-856c51e76753
ms.openlocfilehash: 5a5fda2cbf8d0bf16ccb17f2766b31d24e5c0c67
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97263560"
---
# <a name="using-a-common-control-as-a-child-window"></a>Использование общего элемента управления как дочернего окна

Любой из стандартных элементов управления Windows можно использовать в качестве дочернего окна любого другого окна. Следующая процедура описывает динамическое создание общего элемента управления и работу с ним.

### <a name="to-use-a-common-control-as-a-child-window"></a>Использование общего элемента управления в качестве дочернего окна

1. Определите элемент управления в связанном классе или обработчике.

1. Используйте переопределение элемента управления метода [CWnd:: Create](../mfc/reference/cwnd-class.md#create) , чтобы создать элемент управления Windows.

1. После создания элемента управления (как на ранних этапах `OnCreate` работы с обработчиком, если вы создаете подкласс элемента управления), можно манипулировать элементом управления с помощью его функций-членов. Дополнительные сведения о методах см. в описании отдельных элементов управления в [элементах управления](../mfc/controls-mfc.md) .

1. По завершении работы с элементом управления используйте [CWnd::D естройвиндов](../mfc/reference/cwnd-class.md#destroywindow) , чтобы уничтожить элемент управления.

## <a name="see-also"></a>См. также раздел

[Создание и использование элементов управления](../mfc/making-and-using-controls.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
