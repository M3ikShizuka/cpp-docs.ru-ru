---
description: 'Дополнительные сведения: методы создания строки состояния'
title: Способы создания строки состояния
ms.date: 11/04/2016
helpviewer_keywords:
- CStatusBar class [MFC], vs. CStatusBarCtrl
- methods [MFC], creating status bars
- CStatusBarCtrl class [MFC], vs. CStatusBar
- CStatusBarCtrl class [MFC], creating
- methods [MFC]
- status bars [MFC], creating
ms.assetid: 9aeaf290-7099-4762-a5ba-9c26705333c9
ms.openlocfilehash: 06ae4002fdffb8ba90964b5ef488d0c115b3a0e0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97203059"
---
# <a name="methods-of-creating-a-status-bar"></a>Способы создания строки состояния

MFC предоставляет два класса для создания строк состояния: [CStatusBar](reference/cstatusbar-class.md) и [CStatusBarCtrl](reference/cstatusbarctrl-class.md) (который заключает в оболочку общий API элемента управления Windows). `CStatusBar` предоставляет все функции общего элемента управления "строка состояния", он автоматически взаимодействует с меню и панелями инструментов и обрабатывает многие из необходимых общих параметров и структур элементов управления. Однако итоговый исполняемый файл обычно будет больше, чем созданный с помощью `CStatusBarCtrl` .

`CStatusBarCtrl` обычно приводит к уменьшению исполняемого файла, и вы можете использовать его, `CStatusBarCtrl` если не собираетесь интегрировать строку состояния в архитектуру MFC. Если вы планируете использовать `CStatusBarCtrl` и интегрировать строку состояния в архитектуру MFC, необходимо принять дополнительные меры, чтобы передавать управление строками состояния в MFC. Это несложная связь. Однако это дополнительная работа, которая не требуется при использовании `CStatusBar` .

Visual C++ предоставляет два способа использования общего элемента управления строки состояния.

- Создайте строку состояния с помощью `CStatusBar` , а затем вызовите метод [CStatusBar:: жетстатусбарктрл](reference/cstatusbar-class.md#getstatusbarctrl) , чтобы получить доступ к `CStatusBarCtrl` функциям элементов.

- Создайте строку состояния с помощью конструктора [CStatusBarCtrl](reference/cstatusbarctrl-class.md).

Любой из методов предоставит доступ к функциям элементов управления строки состояния. При вызове `CStatusBar::GetStatusBarCtrl` он возвращает ссылку на `CStatusBarCtrl` объект, чтобы можно было использовать любой набор функций-членов. Сведения о создании и создании строки состояния с помощью см. в разделе [CStatusBar](reference/cstatusbar-class.md) `CStatusBar` .

## <a name="see-also"></a>См. также раздел

[Использование CStatusBarCtrl](using-cstatusbarctrl.md)<br/>
[Элементы управления](controls-mfc.md)
