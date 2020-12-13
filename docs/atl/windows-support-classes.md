---
description: Дополнительные сведения о классах поддержки Windows
title: Классы поддержки Windows (ATL)
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- ATL, windows
- windows [C++], ATL
ms.assetid: 750b14d5-d787-4d2b-9728-ac199ccad489
ms.openlocfilehash: c88a6ef878a428581ca090e78b2fac3b5e02131d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97138067"
---
# <a name="windows-support-classes"></a>Классы поддержки Windows

Следующие классы обеспечивают поддержку для Windows:

- [_U_MENUorID](../atl/reference/u-menuorid-class.md) Предоставляет оболочки для `CreateWindow` и `CreateWindowEx` .

- [CWindow](../atl/reference/cwindow-class.md) Содержит методы для управления окном. `CWindow` — это базовый класс для `CWindowImpl`, `CDialogImpl` и `CContainedWindow`.

- [Квиндовимпл](../atl/reference/cwindowimpl-class.md) Реализует окно на основе нового класса окна. Также позволяет создать подкласс или суперкласс для окна.

- [CDialogImpl](../atl/reference/cdialogimpl-class.md) Реализует диалоговое окно.

- [Каксдиалогимпл](../atl/reference/caxdialogimpl-class.md) Реализует диалоговое окно (модальное или немодальное), в котором размещены элементы управления ActiveX.

- [Ксимпледиалог](../atl/reference/csimpledialog-class.md) Реализует диалоговое окно (модальное или немодальное) с базовой функциональностью.

- [Каксвиндов](../atl/reference/caxwindow-class.md) Управляет окном, в котором размещается элемент управления ActiveX.

- [CAxWindow2T](../atl/reference/caxwindow2t-class.md) Предоставляет методы для управления окном, в котором размещается элемент управления ActiveX, а также поддерживает размещение лицензированных элементов управления ActiveX.

- [Кконтаинедвиндовт](../atl/reference/ccontainedwindowt-class.md) Реализует окно, содержащееся в другом объекте.

- [Квндклассинфо](../atl/reference/cwndclassinfo-class.md) Управляет сведениями о новом классе окна.

- [Кдинамикчаин](../atl/reference/cdynamicchain-class.md) Поддерживает динамическое связывание карт сообщений.

- [Кмессажемап](../atl/reference/cmessagemap-class.md) Позволяет объекту предоставлять свои карты сообщений другим объектам.

- [Квинтраитс](../atl/reference/cwintraits-class.md) Предоставляет простой способ стандартизации признаков объекта окна ATL.

- [Квинтраитсор](../atl/reference/cwintraitsor-class.md) Предоставляет значения по умолчанию для стилей окон и расширенных стилей, используемых для создания окна. Эти значения добавляются с помощью оператора логического или к значениям, указанным во время создания окна.

## <a name="related-articles"></a>Похожие статьи

[Классы окон ATL](../atl/atl-window-classes.md)

[Учебник по ATL](../atl/active-template-library-atl-tutorial.md)

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../atl/atl-class-overview.md)<br/>
[Макросы схемы сообщений](../atl/reference/message-map-macros-atl.md)<br/>
[Макросы класса Window](../atl/reference/window-class-macros.md)
