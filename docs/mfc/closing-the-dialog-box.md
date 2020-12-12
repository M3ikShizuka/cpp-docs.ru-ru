---
description: 'Дополнительные сведения: закрытие диалогового окна'
title: Закрытие диалогового окна
ms.date: 11/04/2016
helpviewer_keywords:
- MFC dialog boxes [MFC], closing
- dialog boxes [MFC], closing
ms.assetid: 946f5675-c482-46a4-a5dd-34fe138ffae5
ms.openlocfilehash: 4e60bdfb1ecb6968996d6c657f0c667ad2686a56
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338376"
---
# <a name="closing-the-dialog-box"></a>Закрытие диалогового окна

Модальное диалоговое окно закрывается, когда пользователь нажимает одну из кнопок, как правило, кнопка ОК или Отмена. Нажатие кнопки ОК или Отмена приводит к тому, что Windows отправляет объект диалогового окна **BN_CLICKED** сообщение с уведомлением об управлении с идентификатором кнопки **идок** или **идканцел**. `CDialog` предоставляет функции обработчика по умолчанию для этих сообщений: `OnOK` и `OnCancel` . Обработчики по умолчанию вызывают `EndDialog` функцию члена для закрытия диалогового окна. Вы также можете вызвать `EndDialog` из собственного кода. Дополнительные сведения см. в описании функции элемента [EndDialog](reference/cdialog-class.md#enddialog) класса `CDialog` в *справочнике по MFC*.

Чтобы расположиться на закрытие и удаление немодального диалогового окна, переопределите `PostNcDestroy` и вызовите **`delete`** оператор для **`this`** указателя. [Удаление диалогового окна объясняет,](destroying-the-dialog-box.md) что происходит дальше.

## <a name="see-also"></a>См. также раздел

[Работа с диалоговыми окнами в MFC](life-cycle-of-a-dialog-box.md)
