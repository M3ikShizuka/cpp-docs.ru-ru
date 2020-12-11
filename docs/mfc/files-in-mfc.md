---
description: Дополнительные сведения о файлах в MFC
title: Файлы в MFC
ms.date: 11/04/2016
helpviewer_keywords:
- serialization [MFC], MFC files
- I/O [MFC], MFC classes
- files [MFC], MFC
- files [MFC], serialization
- binary access, binary file operations in MFC
- file I/O classes [MFC]
- I/O [MFC]
- persistence [MFC]
- MFC, file operations
- files [MFC], manipulating
- binary access [MFC]
ms.assetid: ae25e2c5-2859-4679-ab97-438824e93ce1
ms.openlocfilehash: 47fab5876efd7d06ec4364721a09b7ed09da9744
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97155050"
---
# <a name="files-in-mfc"></a>Файлы в MFC

В библиотека Microsoft Foundation Class (MFC) класс [кфиле](reference/cfile-class.md) обрабатывает обычные операции файлового ввода-вывода. В этом семействе статей объясняется, как открывать и закрывать файлы, а также считывать и записывать данные в эти файлы. В нем также обсуждаются операции по состоянию файлов. Описание использования функций сериализации на основе объектов MFC в качестве альтернативного способа чтения и записи данных в файлах см. в статье [сериализация](serialization-in-mfc.md).

> [!NOTE]
> При использовании объектов MFC `CDocument` платформа выполняет большую часть сериализации. В частности, платформа создает и использует `CFile` объект. Вам нужно только написать код в переопределении `Serialize` функции члена класса `CDocument` .

`CFile`Класс предоставляет интерфейс для операций с двоичными файлами общего назначения. `CStdioFile`Классы и, `CMemFile` производные от `CFile` , и класс, `CSharedFile` производный от, `CMemFile` предоставляют более специализированные файловые службы.

Дополнительные сведения о альтернативных вариантах обработки файлов MFC см. в разделе [Обработка файлов](../c-runtime-library/file-handling.md) в *справочнике по библиотеке времени выполнения*.

Дополнительные сведения о производных `CFile` классах см. в разделе [диаграмма иерархии MFC](hierarchy-chart.md).

## <a name="what-do-you-want-to-do"></a>Что Вы хотите делать

*Использование Кфиле*

- [Открытие файла с помощью Кфиле](opening-files.md)

- [Чтение и запись файла с помощью Кфиле](reading-and-writing-files.md)

- [Закрытие файла с помощью Кфиле](closing-files.md)

- [Доступ к состоянию файла с помощью Кфиле](accessing-file-status.md)

*Использовать сериализацию MFC (сохраняемость объектов)*

- [Создание сериализуемого класса](serialization-making-a-serializable-class.md)

- [Сериализация объекта с помощью объекта CArchive](serialization-serializing-an-object.md)

- [Создание объекта CArchive](two-ways-to-create-a-carchive-object.md)

- [Использование CArchive <\< and > операторов>](using-the-carchive-output-and-input-operators.md)

- [Хранение и загрузка CObject и производных от CObject объектов с помощью архива](storing-and-loading-cobjects-via-an-archive.md)

## <a name="see-also"></a>См. также раздел

[Основные понятия](mfc-concepts.md)<br/>
[Общие разделы по MFC](general-mfc-topics.md)<br/>
[Класс CArchive](reference/carchive-class.md)<br/>
[CObject, класс](reference/cobject-class.md)
