---
description: 'Дополнительные сведения о: CTreeCtrl и CTreeView'
title: CTreeCtrl или CTreeView
ms.date: 11/04/2016
helpviewer_keywords:
- tree view controls
- CTreeCtrl class [MFC], vs. CTreeView class [MFC]
- CTreeView class [MFC], vs. CTreeCtrl class [MFC]
- tree controls [MFC], and tree view
ms.assetid: bba5af25-103f-4b53-84d3-071bc9bd6494
ms.openlocfilehash: edaf2662d483a23c7618a143ee4aabe7910cf121
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97309424"
---
# <a name="ctreectrl-vs-ctreeview"></a>CTreeCtrl или CTreeView

MFC предоставляет два класса, которые инкапсулируют элементы управления "дерево": [CTreeCtrl](reference/ctreectrl-class.md) и [CTreeView](reference/ctreeview-class.md). Каждый класс полезен в различных ситуациях.

Используется `CTreeCtrl` , если требуется обычный элемент управления "дочернее окно"; например, в диалоговом окне. Особенно желательно использовать `CTreeCtrl` , если в окне есть другие дочерние элементы управления, как в обычном диалоговом окне.

Используется, если необходимо, `CTreeView` чтобы элемент управления "дерево" действовал как окно представления в архитектуре "документ/представление", а также как элемент управления "дерево". `CTreeView`Будет занимать всю клиентскую область окна фрейма или окна-разделителя. Размер автоматически изменяется при изменении размера родительского окна и может обрабатывать сообщения команд из меню, клавиш быстрого вызова и панелей инструментов. Поскольку элемент управления "дерево" содержит данные, необходимые для вывода дерева, соответствующий объект документа не обязательно должен быть сложным — можно даже использовать [CDocument](reference/cdocument-class.md) в качестве типа документа в шаблоне документа.

## <a name="see-also"></a>См. также раздел

[Использование CTreeCtrl](using-ctreectrl.md)<br/>
[Элементы управления](controls-mfc.md)
