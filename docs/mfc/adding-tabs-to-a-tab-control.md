---
description: 'Дополнительные сведения: Добавление вкладок в элемент управления "Вкладка"'
title: Добавление вкладок в элемент управления "Вкладка"
ms.date: 11/04/2016
helpviewer_keywords:
- tab controls [MFC], adding tabs
- putting tabs on CTabCtrls [MFC]
- CTabCtrl class [MFC], adding tabs
- tabs [MFC], adding to CTabCtrl class [MFC]
ms.assetid: 7f3d9340-e3c7-4c71-9912-be57534ecc78
ms.openlocfilehash: ca25edf349fb11271d4e355241f4724d11bc4ac0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185470"
---
# <a name="adding-tabs-to-a-tab-control"></a>Добавление вкладок в элемент управления "Вкладка"

После создания элемента управления "Вкладка" ([CTabCtrl](reference/ctabctrl-class.md)) добавьте столько вкладок, сколько необходимо.

### <a name="to-add-a-tab-item"></a>Добавление элемента вкладки

1. Подготовьте структуру [тЦитем](/windows/win32/api/commctrl/ns-commctrl-tcitemw) .

1. Вызовите метод [CTabCtrl:: InsertItem](reference/ctabctrl-class.md#insertitem), передав структуру.

1. Повторите шаги 1 и 2 для дополнительных элементов вкладки.

Дополнительные сведения см. в разделе [Создание элемента управления "Вкладка"](/windows/win32/Controls/tab-controls) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Использование CTabCtrl](using-ctabctrl.md)<br/>
[Элементы управления](controls-mfc.md)
