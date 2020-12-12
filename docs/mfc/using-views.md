---
description: 'Дополнительные сведения: использование представлений'
title: Использование представлений
ms.date: 11/04/2016
helpviewer_keywords:
- interacting with users and role of view class [MFC]
- drawing [MFC], data
- rendering data
- view classes [MFC], role in managing user interaction
- CView class [MFC], view architecture
- MFC, views
- views [MFC], using
- painting data
- user input [MFC], interpreting through view class [MFC]
- view classes [MFC], role in displaying application data
ms.assetid: dc3de6ad-5c64-4317-8f10-8bdcc38cdbd5
ms.openlocfilehash: f17855c1389da44630a21830033c4457db6e3703
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97236650"
---
# <a name="using-views"></a>Использование представлений

Обязанности представления должны отображать данные документа в графическом виде для пользователя, а также принимать и интерпретировать ввод пользователя как операции над документом. Задачи, выполняемые при написании класса представления,:

- Запишите функцию члена класса представления [OnDraw](../mfc/reference/cview-class.md#ondraw) , которая визуализирует данные документа.

- Подключайте соответствующие сообщения Windows и объекты пользовательского интерфейса, такие как пункты меню, к функциям-членам обработчика сообщений в классе представления.

- Реализуйте эти обработчики для интерпретации вводимых пользователем данных.

Кроме того, может потребоваться переопределить другие `CView` функции члена в производном классе представления. В частности, может потребоваться переопределить [онинитиалупдате](../mfc/reference/cview-class.md#oninitialupdate) , чтобы выполнить специальную инициализацию для представления, и [OnUpdate](../mfc/reference/cview-class.md#onupdate) для выполнения специальной обработки, необходимой непосредственно перед перерисовкой представления. Для многостраничных документов необходимо также переопределить [онпрепарепринтинг](../mfc/reference/cview-class.md#onprepareprinting) , чтобы инициализировать диалоговое окно Печать с числом страниц для печати и другими сведениями. Дополнительные сведения о переопределении `CView` функций элементов см. в разделе класс [CView](../mfc/reference/cview-class.md) в *справочнике по MFC*.

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Производные классы представлений, доступные в MFC](../mfc/derived-view-classes-available-in-mfc.md)

- [Рисование в представлении](../mfc/drawing-in-a-view.md)

- [Интерпретация ввода пользователя через представление](../mfc/interpreting-user-input-through-a-view.md)

- [Роль представления при печати](../mfc/role-of-the-view-in-printing.md)

- [Изменение масштаба и прокрутка представлений](../mfc/scrolling-and-scaling-views.md)

- [Инициализация и очистка документов и представлений](../mfc/initializing-and-cleaning-up-documents-and-views.md)

## <a name="see-also"></a>См. также раздел

[Архитектура документа/представления](../mfc/document-view-architecture.md)<br/>
[Класс CFormView](../mfc/reference/cformview-class.md)<br/>
[Представления записей (доступ к данным MFC)](../data/record-views-mfc-data-access.md)<br/>
[Обход механизма сериализации](../mfc/bypassing-the-serialization-mechanism.md)
