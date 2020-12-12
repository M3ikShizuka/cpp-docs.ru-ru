---
description: 'Дополнительные сведения о: контейнерные элементы управления и полосы'
title: Элементы управления и зоны главной панели
ms.date: 11/04/2016
helpviewer_keywords:
- rebar controls [MFC], working with bands in
- bands, in rebar controls
ms.assetid: b647e7a5-9ea7-48b1-8e5f-096d104748f0
ms.openlocfilehash: 27ada3633a560ad8b5852b05bdd6330a0936fb99
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97248571"
---
# <a name="rebar-controls-and-bands"></a>Элементы управления и зоны главной панели

Главным назначением элемента управления "Главная панель" является работа в качестве контейнера для дочерних окон, общих элементов управления диалогового окна, меню, панелей инструментов и т. д. Это включение поддерживается понятием "полоса". Каждая полоса главных панелей может содержать любое сочетание полосы захвата, точечного рисунка, метки текста и дочернего окна.

Класс `CReBarCtrl` содержит множество функций-членов, которые можно использовать для получения и управления данными для конкретной панели главной группы:

- [Жетбандкаунт](../mfc/reference/crebarctrl-class.md#getbandcount) Возвращает количество текущих полос в элементе управления "Главная панель".

- [Жетбандинфо](../mfc/reference/crebarctrl-class.md#getbandinfo) Инициализирует структуру **ребарбандинфо** со сведениями из указанного диапазона. Имеется соответствующая функция-член [сетбандинфо](../mfc/reference/crebarctrl-class.md#setbandinfo) .

- [Коrect](../mfc/reference/crebarctrl-class.md#getrect) Извлекает ограничивающий прямоугольник указанной полосы.

- Число [строк](../mfc/reference/crebarctrl-class.md#getrowcount) Возвращает количество строк полос в элементе управления "Главная панель".

- [Идтоиндекс](../mfc/reference/crebarctrl-class.md#idtoindex) Извлекает индекс указанного диапазона.

- [Жетбандбордерс](../mfc/reference/crebarctrl-class.md#getbandborders) Извлекает границы полосы.

Помимо манипуляций предоставляется несколько функций, позволяющих работать с конкретными полосами главной панели.

[Инсертбанд](../mfc/reference/crebarctrl-class.md#insertband) и [делетебанд](../mfc/reference/crebarctrl-class.md#deleteband) Добавление и удаление полос главной панели. [Минимизебанд](../mfc/reference/crebarctrl-class.md#minimizeband) и [максимизебанд](../mfc/reference/crebarctrl-class.md#maximizeband) влияют на текущий размер заданной области главной панели. [Мовебанд](../mfc/reference/crebarctrl-class.md#moveband) изменяет индекс определенной полосы главной панели. [Шовбанд](../mfc/reference/crebarctrl-class.md#showband) показывает или скрывает полосу элементов главной панели от пользователя.

В следующем примере демонстрируется добавление панели инструментов (*m_wndToolBar*) к существующему элементу управления главной панели (*m_wndReBar*). Диапазон описан путем инициализации `rbi` структуры и последующего вызова `InsertBand` функции-члена:

[!code-cpp[NVC_MFCControlLadenDialog#27](../mfc/codesnippet/cpp/rebar-controls-and-bands_1.cpp)]

## <a name="see-also"></a>См. также раздел

[Использование CReBarCtrl](../mfc/using-crebarctrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
