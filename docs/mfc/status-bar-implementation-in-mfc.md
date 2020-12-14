---
description: Дополнительные сведения см. в статье реализация строки состояния в MFC.
title: Реализация строки состояния в MFC
ms.date: 11/19/2018
f1_keywords:
- COldStatusBar
helpviewer_keywords:
- status bars [MFC], implementing in MFC
- CStatusBarCtrl class [MFC], and MFC status bars
- CStatusBar class [MFC], and CStatusBarCtrl class [MFC]
- CStatusBarCtrl class [MFC], and CStatusBar class [MFC]
- status bars [MFC], backward compatibility
- status bars [MFC], old with COldStatusBar class [MFC]
- COldStatusBar class [MFC]
- status bars [MFC], and CStatusBarCtrl class
- CStatusBar class [MFC], and MFC status bars
- status indicators
- status bars [MFC], Windows 95 implementation
ms.assetid: be5cd876-38e3-4d5c-b8cb-16d57a16a142
ms.openlocfilehash: d42f8b4bf6ae72cf8eb4a12d1f5eafb8603c5e1b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216760"
---
# <a name="status-bar-implementation-in-mfc"></a>Реализация строки состояния в MFC

Объект [CStatusBar](../mfc/reference/cstatusbar-class.md) — это панель элементов управления со строкой панелей вывода текста. Области вывода обычно используются в качестве линий сообщений и в качестве индикаторов состояния. Примеры включают в себя строки справки меню, поясняющие выбранную команду меню, и индикаторы, отображающие состояние блокировки прокрутки, NUM LOCK и других клавиш.

Начиная с MFC версии 4,0, строки состояния реализуются с помощью класса [CStatusBarCtrl](../mfc/reference/cstatusbarctrl-class.md), который инкапсулирует общий элемент управления строки состояния. Для обеспечения обратной совместимости MFC оставляет старую реализацию строки состояния в классе `COldStatusBar` . Документация для более ранних версий MFC описывается `COldStatusBar` в разделе `CStatusBar` .

[CStatusBar:: жетстатусбарктрл](../mfc/reference/cstatusbar-class.md#getstatusbarctrl), функция-член, новая для MFC 4,0, позволяет воспользоваться преимуществами поддержки общего элемента управления Windows для настройки строки состояния и дополнительных функций. `CStatusBar` функции элементов предоставляют большую часть функциональных возможностей стандартных элементов управления Windows. Однако при вызове вы `GetStatusBarCtrl` можете присвоить строкам состояния еще больше характеристик строки состояния. При вызове `GetStatusBarCtrl` будет возвращена ссылка на `CStatusBarCtrl` объект. Эту ссылку можно использовать для работы с элементом управления "строка состояния".

На следующем рисунке показана строка состояния, на которой отображается несколько индикаторов.

![Строка состояния](../mfc/media/vc37dy1.gif "Строка состояния") <br/>
Строка состояния

Как и панель инструментов, объект строки состояния внедряется в родительское окно фрейма и создается автоматически при создании фрейма окна. Строка состояния, как и все панели управления, уничтожается автоматически, а также при уничтожении родительского фрейма.

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Обновление текста панели строки состояния](../mfc/updating-the-text-of-a-status-bar-pane.md)

- Классы MFC [CStatusBar](../mfc/reference/cstatusbar-class.md) и [CStatusBarCtrl](../mfc/reference/cstatusbarctrl-class.md)

- [Панели элементов управления](../mfc/control-bars.md)

- [Диалоговые панели](../mfc/dialog-bars.md)

- [Панели инструментов (реализация MFC на панели инструментов)](../mfc/mfc-toolbar-implementation.md)

## <a name="see-also"></a>См. также раздел

[Строки состояния](../mfc/status-bars.md)
