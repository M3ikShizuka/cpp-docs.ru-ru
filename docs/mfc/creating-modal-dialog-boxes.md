---
description: 'Дополнительные сведения: создание модальных диалоговых окон'
title: Создание модальных диалоговых окон
ms.date: 11/04/2016
helpviewer_keywords:
- modal dialog boxes [MFC], creating
- MFC dialog boxes [MFC], creating
- MFC dialog boxes [MFC], modal
ms.assetid: 26c7a68c-79f6-4862-a5a8-6024984644d2
ms.openlocfilehash: 82fa10c65161df98ea3d377e302c0fb787feb14c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97309801"
---
# <a name="creating-modal-dialog-boxes"></a>Создание модальных диалоговых окон

Чтобы создать модальное диалоговое окно, вызовите один из двух открытых конструкторов, объявленных в [CDialog](reference/cdialog-class.md). Затем вызовите функцию члена [DoModal](reference/cdialog-class.md#domodal) объекта Dialog, чтобы отобразить диалоговое окно и управлять взаимодействием с ним до тех пор, пока пользователь не нажмет кнопку ОК или Отмена. Это управление, которое `DoModal` делает диалоговое окно модальным. Для модальных диалоговых окон `DoModal` загружает ресурс диалогового окна.

## <a name="see-also"></a>См. также раздел

[Работа с диалоговыми окнами в MFC](life-cycle-of-a-dialog-box.md)
