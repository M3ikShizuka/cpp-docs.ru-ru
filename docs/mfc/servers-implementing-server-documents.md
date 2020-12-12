---
description: 'Дополнительные сведения о: серверы: реализация серверных документов'
title: Серверы. Реализация документов сервера
ms.date: 11/04/2016
helpviewer_keywords:
- OLE server applications [MFC], managing server documents
- OLE server applications [MFC], implementing OLE servers
- servers, server documents
- server documents [MFC], implementing
ms.assetid: cca1451a-ad09-47ed-b56e-bccd78fc86d1
ms.openlocfilehash: b8843d3e2ac662cbb018a3063c9f04f5dd8d6f10
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97217332"
---
# <a name="servers-implementing-server-documents"></a>Серверы. Реализация документов сервера

В этой статье описываются действия, которые необходимо выполнить для успешной реализации серверного документа, если в мастере приложений не был указан параметр OLE-сервера.

#### <a name="to-define-a-server-document-class"></a>Определение класса серверного документа

1. Создайте производный класс документа от `COleServerDoc` вместо `CDocument` .

1. Создайте класс элемента сервера, производный от `COleServerItem` .

1. Реализуйте `OnGetEmbeddedItem` функцию члена класса серверного документа.

   `OnGetEmbeddedItem` вызывается, когда пользователь приложения-контейнера создает или редактирует внедренный элемент. Он должен возвращать элемент, представляющий весь документ. Это должен быть объект `COleServerItem` класса, производного от.

1. Переопределите `Serialize` функцию члена для сериализации содержимого документа. Не нужно выполнять сериализацию списка элементов сервера, если они не используются для представления собственных данных в документе. Дополнительные сведения см. в разделе *Реализация элементов сервера* на [серверах статей: элементы сервера](../mfc/servers-server-items.md).

При создании серверного документа платформа автоматически регистрирует документ в библиотеках DLL системы OLE. Это позволяет библиотекам DLL обнаруживать серверные документы.

Дополнительные сведения см. в разделе [COleServerItem](../mfc/reference/coleserveritem-class.md) и [колесервердок](../mfc/reference/coleserverdoc-class.md) в *справочнике по библиотеке классов*.

## <a name="see-also"></a>См. также раздел

[Серверы](../mfc/servers.md)<br/>
[Серверы: элементы сервера](../mfc/servers-server-items.md)<br/>
[Серверы: реализация сервера](../mfc/servers-implementing-a-server.md)<br/>
[Серверы: реализация окон кадров In-Place](../mfc/servers-implementing-in-place-frame-windows.md)
