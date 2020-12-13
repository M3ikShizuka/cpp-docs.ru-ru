---
description: 'Дополнительные сведения о: Общие сведения о классах окон ATL'
title: Общие сведения о классах окон ATL
ms.date: 11/04/2016
helpviewer_keywords:
- window classes
ms.assetid: 503efc2c-a269-495d-97cf-3fb300d52f3d
ms.openlocfilehash: 54a9d9764450025e51f9fac368a3434ca786fe09
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152728"
---
# <a name="introduction-to-atl-window-classes"></a>Общие сведения о классах окон ATL

Следующие классы ATL предназначены для реализации и управления Windows:

- [CWindow](../atl/reference/cwindow-class.md) позволяет присоединить к объекту маркер окна `CWindow` . Затем вызываются `CWindow` методы для управления окном.

- [Квиндовимпл](../atl/reference/cwindowimpl-class.md) позволяет реализовать новое окно и обрабатывать сообщения с помощью схемы сообщений. Можно создать окно на основе нового класса Windows, суперкласса существующего класса или подклассировать существующее окно.

- [CDialogImpl](../atl/reference/cdialogimpl-class.md) позволяет реализовать модальное или немодальное диалоговое окно и обрабатывать сообщения с помощью схемы сообщений.

- [Кконтаинедвиндовт](../atl/reference/ccontainedwindowt-class.md) — это предварительно созданный класс, который реализует окно, схема сообщений которого содержится в другом классе. Использование `CContainedWindowT` позволяет централизовать обработку сообщений в одном классе.

- [Каксдиалогимпл](../atl/reference/caxdialogimpl-class.md) позволяет реализовать диалоговое окно (модальное или немодальное), в котором размещены элементы управления ActiveX.

- [Ксимпледиалог](../atl/reference/csimpledialog-class.md) позволяет реализовать модальное диалоговое окно с базовой функциональностью.

- [Каксвиндов](../atl/reference/caxwindow-class.md) позволяет реализовать окно, в котором размещается элемент управления ActiveX.

- [CAxWindow2T](../atl/reference/caxwindow2t-class.md) позволяет реализовать окно, в котором размещен лицензированный элемент управления ActiveX.

В дополнение к конкретным классам окон ATL предоставляет несколько классов, предназначенных для упрощения реализации объекта окна ATL. Вот они:

- [Квндклассинфо](../atl/reference/cwndclassinfo-class.md) управляет сведениями о новом классе окна.

- [Квинтраитс](../atl/reference/cwintraits-class.md) и [квинтраитсор](../atl/reference/cwintraitsor-class.md) предоставляют простой способ стандартизации признаков объекта окна ATL.

## <a name="see-also"></a>См. также раздел

[Классы окон](../atl/atl-window-classes.md)
