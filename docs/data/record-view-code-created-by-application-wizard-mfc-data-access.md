---
description: См. Дополнительные сведения о коде представления записей, созданном мастером приложений (доступ к данным MFC).
title: Код представления записей, создаваемый мастером приложений (доступ к данным MFC)
ms.date: 11/04/2016
helpviewer_keywords:
- application wizards [C++], record view code
- record views, refreshing controls
- record views, application wizard code
ms.assetid: 18fd4703-5939-491d-b759-985f767b951f
ms.openlocfilehash: b0fa7a4960096f11ab66194fa6e41be60b45d4c1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332439"
---
# <a name="record-view-code-created-by-application-wizard--mfc-data-access"></a>Код представления записей, создаваемый мастером приложений (доступ к данным MFC)

[Мастер приложений MFC](../mfc/reference/database-support-mfc-application-wizard.md) переопределяет `OnInitialUpdate` функции представления и `OnGetRecordset` элемента. После того как платформа создает фрейм окна, документ и представление, она вызывает `OnInitialUpdate` для инициализации представления. `OnInitialUpdate` Получает указатель на набор записей из документа. Вызов базового класса, функция [CView:: онинитиалупдате](../mfc/reference/cview-class.md#oninitialupdate) открывает набор записей. В следующем коде показан этот процесс для `CRecordView` :

```cpp
void CSectionForm::OnInitialUpdate()
{
   m_pSet = &GetDocument()->m_sectionSet;
   CRecordView::OnInitialUpdate();
}
```

При открытии набора записей происходит выбор записей. [CRecordset:: Open](../mfc/reference/crecordset-class.md#open) делает первую запись текущей записью, а DDX перемещает данные из элементов данных полей набора записей в соответствующие элементы управления формы в представлении. Дополнительные сведения о RFX см. в статье [Обмен полями записей (RFX)](../data/odbc/record-field-exchange-rfx.md). Дополнительные сведения об DDX см [обмен данными окон и проверка](../mfc/dialog-data-exchange-and-validation.md). Сведения о процессе создания документа/представления см. в разделе [Использование классов для написания приложений для Windows](../mfc/using-the-classes-to-write-applications-for-windows.md).

> [!NOTE]
> Следует предоставить конечным пользователям возможность обновления элементов управления представления записи из набора записей. Без этой возможности, если пользователь изменяет значение в элементе управления на недопустимое значение, пользователь может застрять на текущей записи. Чтобы обновить элементы управления, вызовите `CWnd` функцию-член [упдатедата](../mfc/reference/cwnd-class.md#updatedata) с параметром false.

## <a name="see-also"></a>См. также раздел

[Использование представления записей](../data/using-a-record-view-mfc-data-access.md)
