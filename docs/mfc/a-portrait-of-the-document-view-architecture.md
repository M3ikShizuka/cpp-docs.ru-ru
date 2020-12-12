---
description: Дополнительные сведения см. в книжной ориентации на архитектуру "документ-представление"
title: Книжная ориентация архитектуры Document-View
ms.date: 11/04/2016
helpviewer_keywords:
- documents [MFC], views
- multiple views [MFC], updating from document
- document/view architecture [MFC]
- views [MFC], and user input
- documents [MFC], accessing data from view
- views [MFC], updating
- input [MFC], view class
- documents [MFC], multiple views
- document/view architecture [MFC], accessing data from view
- document/view architecture [MFC], about document/view architecture
- views [MFC], accessing document data from
ms.assetid: 4e7f65dc-b166-45d8-bcd5-9bb0d399b946
ms.openlocfilehash: e4f8fc636349aaa12ee4481c7f6223c343b6d406
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97169636"
---
# <a name="a-portrait-of-the-documentview-architecture"></a>Портрет архитектуры "документ-представление"

Документы и представления сопряжены в обычном приложении MFC. Данные хранятся в документе, но представление имеет привилегированный доступ к данным. Отделение документа от представления разделяет хранение и обслуживание данных на экране.

## <a name="gaining-access-to-document-data-from-the-view"></a>Получение доступа к данным документа из представления

Представление обращается к данным документа с помощью функции- [документа](reference/cview-class.md#getdocument) , возвращающей указатель на документ, или путем создания класса представления в C++ **`friend`** класса документа. Затем представление использует доступ к данным для получения данных, когда он готов к рисованию или иным образом манипулировать им.

Например, в функции-члене [OnDraw](reference/cview-class.md#ondraw) представления используется `GetDocument` для получения указателя документа. Затем он использует этот указатель для доступа к `CString` элементу данных в документе. Представление передает строку в `TextOut` функцию. Код для этого примера см. в разделе [Рисование в представлении](drawing-in-a-view.md).

## <a name="user-input-to-the-view"></a>Ввод данных пользователем в представление

Представление может также интерпретировать щелчок мыши внутри себя как выбор или изменение данных. Аналогично, он может интерпретировать нажатия клавиш как ввод или редактирование данных. Предположим, что пользователь вводит строку в представление, которое управляет текстом. Представление получает указатель на документ и использует указатель для передачи новых данных в документ, который сохраняет его в некоторой структуре данных.

## <a name="updating-multiple-views-of-the-same-document"></a>Обновление нескольких представлений одного документа

В приложении с несколькими представлениями одного и того же документа, например в окне разделителя в текстовом редакторе, представление сначала передает новые данные в документ. Затем вызывается функция элемента [UpdateAllViews](reference/cdocument-class.md#updateallviews) документа, которая сообщает всем представлениям документа о необходимости обновления, отражая новые данные. Это синхронизирует представления.

### <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Преимущества архитектуры "документ-представление"](advantages-of-the-document-view-architecture.md)

- [Альтернативы архитектуре "документ-представление"](alternatives-to-the-document-view-architecture.md)

## <a name="see-also"></a>См. также раздел

[Архитектура документа/представления](document-view-architecture.md)
