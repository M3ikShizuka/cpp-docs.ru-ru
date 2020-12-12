---
description: 'Дополнительные сведения о: параметры для элемента управления progress'
title: Параметры элемента управления "Индикатор выполнения"
ms.date: 11/04/2016
helpviewer_keywords:
- CProgressCtrl class [MFC], settings
- progress controls [MFC], settings
ms.assetid: f4616e91-74fa-4000-ba0d-d3ddc0ee075b
ms.openlocfilehash: 0cf3caa5e7b87062b1714f8e5e350840157ff7ba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97217072"
---
# <a name="settings-for-the-progress-control"></a>Параметры элемента управления "Индикатор выполнения"

Основными параметрами для элемента управления progress ([CProgressCtrl](../mfc/reference/cprogressctrl-class.md)) являются диапазон и текущее расположение. Диапазон представляет всю длительность операции. Текущая заданная позицией представляет ход выполнения работы приложения. Любые изменения в диапазоне или положении приводят к перерисовки элемента управления progress.

По умолчанию диапазон имеет значение 0-100, а начальное значение равно 0. Чтобы получить текущие параметры диапазона для элемента управления выполнением, используйте функцию члена с помощью функции [дальнего действия](../mfc/reference/cprogressctrl-class.md#getrange) . Чтобы изменить диапазон, используйте функцию члена [SetRange](../mfc/reference/cprogressctrl-class.md#setrange) .

Чтобы задать расположение, используйте [сетпос](../mfc/reference/cprogressctrl-class.md#setpos). Чтобы получить текущую точку без указания нового значения, используйте [жетпос](../mfc/reference/cprogressctrl-class.md#getpos). Например, может потребоваться просто запросить состояние текущей операции.

Чтобы перейти к текущему положению элемента управления ходом выполнения, используйте [степит](../mfc/reference/cprogressctrl-class.md#stepit). Чтобы задать количество каждого шага, используйте [сетстеп](../mfc/reference/cprogressctrl-class.md#setstep) .

## <a name="see-also"></a>См. также раздел

[Использование CProgressCtrl](../mfc/using-cprogressctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
