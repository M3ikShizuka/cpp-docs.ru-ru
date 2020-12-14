---
description: Дополнительные сведения о функциях элементов "Счетчик"
title: Функции-члены счетчика
ms.date: 11/04/2016
helpviewer_keywords:
- spin button control, methods
- CSpinButtonCtrl class [MFC], methods
ms.assetid: a08a26fd-b803-4cbe-a509-395fa357d057
ms.openlocfilehash: 6a03ab33d29634ed85d807eb5b51edfdef310d65
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216838"
---
# <a name="spin-button-member-functions"></a>Функции-члены счетчика

Существует несколько функций-членов, доступных для элемента управления "Счетчик" ([CSpinButtonCtrl](../mfc/reference/cspinbuttonctrl-class.md)). Используйте эти функции, чтобы изменить следующие атрибуты кнопки "Счетчик".

- **Ускорение** Можно настроить частоту изменения позиции, когда пользователь удерживает кнопку со стрелкой. Для работы с ускорением используйте [функции члена](../mfc/reference/cspinbuttonctrl-class.md#getaccel) [сетакцел](../mfc/reference/cspinbuttonctrl-class.md#setaccel) и.

- **Базовый** Можно изменить базовое значение (10 или 16), используемое для вывода расположения в заголовке окна собеседника. Чтобы работать с базой, используйте функции членов [сетбасе](../mfc/reference/cspinbuttonctrl-class.md#setbase) и [polybase](../mfc/reference/cspinbuttonctrl-class.md#getbase) .

- **Окно собеседника** Можно динамически задать окно собеседника. Для запроса или изменения того, какой элемент управления является окном контакта [,](../mfc/reference/cspinbuttonctrl-class.md#getbuddy) используйте функции-члены [сетбудди](../mfc/reference/cspinbuttonctrl-class.md#setbuddy) и.

- **Расположение** Можно запрашивать и изменять расположение. Для работы непосредственно с положением используйте функции члена [жетпос](../mfc/reference/cspinbuttonctrl-class.md#getpos) и [сетпос](../mfc/reference/cspinbuttonctrl-class.md#setpos) . Так как заголовок элемента управления может измениться (например, в случае, если он является элементом управления редактирования), `GetPos` извлекает текущий заголовок и корректирует его соответствующим образом.

- **Диапазон значений** Вы можете изменить максимальное и минимальное положение кнопки счетчика. По умолчанию максимальное значение равно 0, а минимальное значение — 100. Так как максимальное значение по умолчанию меньше минимального значения по умолчанию, действия кнопок со стрелками являются интуитивно понятными. Как правило, диапазон задается с помощью функции члена [SetRange](../mfc/reference/cspinbuttonctrl-class.md#setrange) . Чтобы запросить диапазон, используйте параметр " [дальнее](../mfc/reference/cspinbuttonctrl-class.md#getrange)".

## <a name="see-also"></a>См. также раздел

[Использование CSpinButtonCtrl](../mfc/using-cspinbuttonctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
