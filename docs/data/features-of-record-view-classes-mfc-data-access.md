---
description: Дополнительные сведения о функциях классов представлений записей (доступ к данным MFC)
title: Функциональные возможности классов представления записей (доступ к данным MFC)
ms.date: 11/04/2016
helpviewer_keywords:
- record views, classes
- record view classes
ms.assetid: e7b2820f-09c4-483f-83c0-317e8be42bdf
ms.openlocfilehash: bf2a0bd1a609fcb29eb945f60ab22c4632addf1b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97116539"
---
# <a name="features-of-record-view-classes--mfc-data-access"></a>Функциональные возможности классов представления записей (доступ к данным MFC)

Вы можете использовать программирование доступа к данным на основе форм с помощью класса [CFormView](../mfc/reference/cformview-class.md), но в большинстве случаев для класса, который будет производным от, лучше использовать класс [CRecordView](../mfc/reference/crecordview-class.md) . В дополнение к его `CFormView` функциям `CRecordView` :

- Обеспечивает обмен данными диалога (DDX) между элементами управления формы и связанным объектом Recordset.

- Обработка перемещения First, перемещение вперед, перемещение назад и перемещение последних команд для перемещения по записям в связанном объекте набора записей.

- Обновляет изменения текущей записи, когда пользователь переходит на другую запись.

Дополнительные сведения о навигации см. [в разделе представления записей. Поддержка навигации в представлении записей](../data/supporting-navigation-in-a-record-view-mfc-data-access.md).

## <a name="see-also"></a>См. также раздел

[Представления записей (доступ к данным MFC)](../data/record-views-mfc-data-access.md)<br/>
[Список драйверов ODBC](../data/odbc/odbc-driver-list.md)
