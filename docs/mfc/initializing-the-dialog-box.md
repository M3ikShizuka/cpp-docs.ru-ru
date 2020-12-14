---
description: 'Дополнительные сведения: инициализация диалогового окна'
title: Инициализация диалогового окна
ms.date: 11/04/2016
helpviewer_keywords:
- initializing dialog boxes [MFC]
- OnInitDialog method [MFC]
- modal dialog boxes [MFC], initializing
- modeless dialog boxes [MFC], initializing
- MFC dialog boxes [MFC], initializing
ms.assetid: 968142f5-19f9-4b34-a1d4-8e6412d4379b
ms.openlocfilehash: 317098a8c0cc745bbd4c94b9ed02401774cb0df9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97197625"
---
# <a name="initializing-the-dialog-box"></a>Инициализация диалогового окна

После создания диалогового окна и всех его элементов управления, но непосредственно перед тем, как на экране появится диалоговое окно (любого из типов), вызывается функция-член [онинитдиалог](reference/cdialog-class.md#oninitdialog) объекта диалогового окна. Для модального диалогового окна это происходит во время `DoModal` вызова. Для немодального диалогового окна `OnInitDialog` вызывается при `Create` вызове метода. Обычно переопределяется `OnInitDialog` для инициализации элементов управления диалогового окна, например для установки исходного текста поля ввода. В `OnInitDialog` переопределении необходимо вызвать функцию члена базового класса `CDialog` `OnInitDialog` .

Если вы хотите задать цвет фона диалогового окна (и всех остальных диалоговых окон приложения), см. раздел [Настройка цвета фона диалогового окна](setting-the-dialog-boxs-background-color.md).

## <a name="see-also"></a>См. также раздел

[Работа с диалоговыми окнами в MFC](life-cycle-of-a-dialog-box.md)
