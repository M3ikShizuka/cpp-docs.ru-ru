---
description: 'Дополнительные сведения о сериализации: сериализация объекта'
title: Сериализация. Сериализация объекта
ms.date: 11/04/2016
helpviewer_keywords:
- serializing objects [MFC]
- serialization [MFC], objects
- objects [MFC], serializing
ms.assetid: 1db772b1-ad55-4fcf-b133-126cca082510
ms.openlocfilehash: ec0782f7faa0d6400f40013925f4a53495a76c7e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97217477"
---
# <a name="serialization-serializing-an-object"></a>Сериализация. Сериализация объекта

Сериализация статьи [: создание сериализуемого класса](../mfc/serialization-making-a-serializable-class.md) показывает, как сделать класс сериализуемым. После создания сериализуемого класса можно сериализовать объекты этого класса в файл и из него через объект [CArchive](../mfc/reference/carchive-class.md) . В этой статье описано, как выполнить следующие задачи.

- [Объект CArchive](../mfc/what-is-a-carchive-object.md).

- [Два способа создания CArchive](../mfc/two-ways-to-create-a-carchive-object.md).

- [Использование CArchive <\< and >> операторов](../mfc/using-the-carchive-output-and-input-operators.md).

- [Хранение и загрузка CObjects через Архив](../mfc/storing-and-loading-cobjects-via-an-archive.md).

Можно позволить платформе создать Архив для сериализуемого документа или явно создать `CArchive` объект самостоятельно. Вы можете передавать данные между файлом и сериализуемым объектом с помощью \< and > операторов <> для `CArchive` или, в некоторых случаях, путем вызова `Serialize` функции класса, `CObject` производного от.

## <a name="see-also"></a>См. также

[Сериализация](../mfc/serialization-in-mfc.md)
