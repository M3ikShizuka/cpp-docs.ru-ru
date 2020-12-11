---
description: 'Дополнительные сведения о: использование документов'
title: Использование документов
ms.date: 11/04/2016
helpviewer_keywords:
- documents [MFC], C++ applications
- data [MFC], reading
- documents [MFC]
- files [MFC], writing to
- data [MFC], documents
- files [MFC]
- views [MFC], C++ applications
- document/view architecture [MFC], documents
- reading data [MFC], documents and views
- printing [MFC], documents
- writing to files [MFC]
ms.assetid: f390d6d8-d0e1-4497-9b6a-435f7ce0776c
ms.openlocfilehash: 486604733808fb027d6dd0fbf81bb670c85313f8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97154504"
---
# <a name="using-documents"></a>Использование документов

Совместная работа, документы и представления:

- Содержат, управляют и отображают [данные](../mfc/managing-data-with-document-data-variables.md), относящиеся к приложению.

- Предоставьте интерфейс, состоящий из [переменных данных документа](../mfc/managing-data-with-document-data-variables.md) для управления данными.

- Участвуйте в [написании и чтении файлов](../mfc/serializing-data-to-and-from-files.md).

- Участвуйте в [печати](../mfc/role-of-the-view-in-printing.md).

- [Обрабатывайте](../mfc/handling-commands-in-the-document.md) большинство команд и сообщений вашего приложения.

Документ особенно связан с управлением данными. Храните данные обычно в переменных членов класса Document. Представление использует эти переменные для доступа к данным для отображения и обновления. Механизм сериализации документа по умолчанию управляет чтением и записью данных в файлы и из них. Документы также могут работать с командами (но не с сообщениями Windows, кроме WM_COMMAND).

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Наследование класса документов от CDocument](../mfc/deriving-a-document-class-from-cdocument.md)

- [Управление данными с помощью переменных данных документа](../mfc/managing-data-with-document-data-variables.md)

- [Сериализация данных в файлы и из них](../mfc/serializing-data-to-and-from-files.md)

- [Обход механизма сериализации](../mfc/bypassing-the-serialization-mechanism.md)

- [Обработка команд в документе](../mfc/handling-commands-in-the-document.md)

- [Функция члена Онневдокумент](../mfc/reference/cdocument-class.md#onnewdocument)

- [Функция члена Делетеконтентс](../mfc/reference/cdocument-class.md#deletecontents)

## <a name="see-also"></a>См. также раздел

[Архитектура документа/представления](../mfc/document-view-architecture.md)
