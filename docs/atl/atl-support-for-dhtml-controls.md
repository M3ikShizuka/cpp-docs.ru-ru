---
description: Дополнительные сведения см. в статье поддержка ATL для элементов управления DHTML.
title: Поддержка элементов управления DHTML в ATL
ms.date: 11/04/2016
helpviewer_keywords:
- HTML controls, ATL support
- DHTML controls, ATL support
- DHTML controls
ms.assetid: 4ba98098-da5d-4362-96ad-8372f816c307
ms.openlocfilehash: 7527527bc5574470fd361bae2375c25ce9345f3a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97148594"
---
# <a name="atl-support-for-dhtml-controls"></a>Поддержка элементов управления DHTML в ATL

С помощью ATL можно создать элемент управления с возможностью динамического HTML (DHTML). Элемент управления DHTML ATL:

- Размещает элемент управления WebBrowser.

- Указывает, что используется HTML, Пользовательский интерфейс элемента управления DHTML.

- Обращается к объекту WebBrowser и его методам через интерфейс [IWebBrowser2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127\(v=vs.85\)).

- Управляет связью между кодом C++ и HTML.

Элемент управления DHTML аналогичен любому другому элементу управления ATL, за исключением того, что элемент управления DHTML включает дополнительный интерфейс диспетчеризации. Иллюстрация интерфейсов, предоставленных в проекте DHTML по умолчанию, показана на рисунке [Определение элементов в проекте элемента управления DHTML](../atl/identifying-the-elements-of-the-dhtml-control-project.md) .

Элемент управления DHTML ATL можно просмотреть в веб-браузере или другом контейнере, например в тестовом контейнере элемента управления ActiveX.

## <a name="in-this-section"></a>в этом разделе

[Определение элементов проекта элемента управления DHTML](../atl/identifying-the-elements-of-the-dhtml-control-project.md)<br/>
Описывает элементы проекта элемента управления DHTML.

[Вызов кода C++ из DHTML](../atl/calling-cpp-code-from-dhtml.md)<br/>
Содержит пример вызова кода C++ из элемента управления DHTML.

[Создание элемента управления DHTML ATL](../atl/creating-an-atl-dhtml-control.md)<br/>
Список действий по созданию элемента управления DHTML.

[Тестирование элемента управления DHTML ATL](../atl/testing-the-atl-dhtml-control.md)<br/>
Демонстрирует создание и тестирование исходного проекта элемента управления DHTML.

[Изменение элемента управления ATL DHTML](../atl/modifying-the-atl-dhtml-control.md)<br/>
Показывает, как добавить некоторые функциональные возможности в элемент управления.

[Тестирование измененного элемента управления DHTML ATL](../atl/testing-the-modified-atl-dhtml-control.md)<br/>
Показывает, как создать и проверить дополнительные функциональные возможности элемента управления.

## <a name="related-sections"></a>Связанные разделы

[ATL](../atl/active-template-library-atl-concepts.md)<br/>
Ссылки на разделы о программировании с использованием библиотеки ATL.
