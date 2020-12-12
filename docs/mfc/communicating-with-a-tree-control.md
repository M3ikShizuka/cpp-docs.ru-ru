---
description: Дополнительные сведения о взаимодействии с элементом управления "дерево"
title: Установка связи с древовидным элементом управления
ms.date: 11/04/2016
helpviewer_keywords:
- tree controls [MFC], communicating with
- CTreeCtrl class [MFC], calling member functions
- communications, tree controls
- tree controls
ms.assetid: 680ad9ee-b11f-452d-93fa-501ca7d7e069
ms.openlocfilehash: 82ee4fe0beb65e44166b4d68ffd44923b7fe0c76
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97310568"
---
# <a name="communicating-with-a-tree-control"></a>Установка связи с древовидным элементом управления

Для вызова функций-членов в объекте [CTreeCtrl](reference/ctreectrl-class.md) используются различные методы в зависимости от способа создания объекта.

- Если элемент управления "дерево" находится в диалоговом окне, используйте переменную-член типа `CTreeCtrl` , созданную в классе диалогового окна.

- Если элемент управления "дерево" является дочерним окном, используйте `CTreeCtrl` объект (или указатель), который использовался для создания объекта.

- Если вы используете `CTreeView` объект, используйте функцию [CTreeView:: GetTreeCtrl](reference/ctreeview-class.md#gettreectrl) , чтобы получить ссылку на элемент управления "дерево". Можно инициализировать другую ссылку с этим значением или назначить адрес ссылки на `CTreeCtrl` указатель.

## <a name="see-also"></a>См. также раздел

[Использование CTreeCtrl](using-ctreectrl.md)<br/>
[Элементы управления](controls-mfc.md)
