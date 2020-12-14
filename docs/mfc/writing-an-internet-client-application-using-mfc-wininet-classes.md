---
description: Дополнительные сведения см. в статье Создание клиентского приложения для Интернета с помощью классов MFC WinInet.
title: Создание клиентских приложений в Интернете с использованием классов MFC WinInet
ms.date: 11/04/2016
helpviewer_keywords:
- Internet client applications [MFC]
- WinInet classes [MFC], programming
- Internet client applications [MFC], writing
- Internet applications [MFC], WinInet
- Internet applications [MFC], client applications
- MFC, Internet applications
ms.assetid: a2c4a40c-a94e-4b3e-9dbf-f8a8dc8e5428
ms.openlocfilehash: 61cfe3e9892f2bde6d233728b7b95ca0edd16ee8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97189136"
---
# <a name="writing-an-internet-client-application-using-mfc-wininet-classes"></a>Создание клиентских приложений в Интернете с использованием классов MFC WinInet

В качестве основания для каждого клиентского приложения Интернета используется Интернет-сеанс. MFC реализует сеансы Интернета как объекты класса [Цинтернетсессион](../mfc/reference/cinternetsession-class.md). С помощью этого класса можно создать один сеанс Интернета или несколько одновременных сеансов.

Для взаимодействия с сервером необходим объект [Цинтернетконнектион](../mfc/reference/cinternetconnection-class.md) и `CInternetSession` . Можно создать с `CInternetConnection` помощью [Цинтернетсессион:: жетфтпконнектион](../mfc/reference/cinternetsession-class.md#getftpconnection), [Цинтернетсессион:: жесттпконнектион](../mfc/reference/cinternetsession-class.md#gethttpconnection)или [Цинтернетсессион:: GetGopherConnection](../mfc/reference/cinternetsession-class.md#getgopherconnection). Каждый из этих вызовов зависит от типа протокола. Эти вызовы не открывают файл на сервере для чтения или записи. Если вы собираетесь читать или записывать данные, необходимо открыть файл как отдельный шаг.

Для большинства Интернет `CInternetSession` -сеансов объект работает вручную с объектом [Цинтернетфиле](../mfc/reference/cinternetfile-class.md) :

- Для сеанса Интернета необходимо создать экземпляр [Цинтернетсессион](../mfc/reference/cinternetsession-class.md).

- Если Интернет-сеанс считывает или записывает данные, необходимо создать экземпляр `CInternetFile` (или его подклассы, [Чттпфиле](../mfc/reference/chttpfile-class.md) или [CGopherFile](../mfc/reference/cgopherfile-class.md)). Самый простой способ считать данные — вызвать [Цинтернетсессион:: OpenURL](../mfc/reference/cinternetsession-class.md#openurl). Эта функция анализирует предоставленный вами универсальный указатель ресурсов (URL-адрес), открывает соединение с сервером, указанным в URL-адресе, и возвращает объект, который доступен только для чтения `CInternetFile` . `CInternetSession::OpenURL` не относится к одному типу протокола — один и тот же вызов работает для любого URL-адреса FTP, HTTP или gopher. `CInternetSession::OpenURL` даже работает с локальными файлами (возвращая `CStdioFile` вместо `CInternetFile` ).

- Если Интернет-сеанс не считывает или не записывает данные, но выполняет другие задачи, такие как удаление файла в FTP-каталоге, то, возможно, не потребуется создавать экземпляр `CInternetFile` .

Существует два способа создания `CInternetFile` объекта.

- При использовании `CInternetSession::OpenURL` для установления соединения с сервером вызов метода `OpenURL` возвращает `CStdioFile` .

- При использовании `CInternetSession::GetFtpConnection` , `GetGopherConnection` или `GetHttpConnection` для установления соединения с сервером необходимо вызвать `CFtpConnection::OpenFile` , `CGopherConnection::OpenFile` или `CHttpConnection::OpenRequest` , соответственно, для возврата `CInternetFile` , `CGopherFile` или `CHttpFile` соответственно.

Действия по реализации клиентского Интернет-приложения зависят от того, создается ли универсальный Интернет-клиент на основе `OpenURL` или зависящий от протокола клиент, использующий одну из `GetConnection` функций.

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Разделы справки написание Интернет-клиентского приложения, которое работает с помощью FTP, HTTP и Gopher](../mfc/steps-in-a-typical-internet-client-application.md)

- [Разделы справки записи клиентского приложения FTP, открывающего файл](../mfc/steps-in-a-typical-ftp-client-application.md)

- [Разделы справки Написание клиентского приложения FTP, которое не открывает файл, но выполняет операцию с каталогом, например удаление файла.](../mfc/steps-in-a-typical-ftp-client-application-to-delete-a-file.md)

- [Разделы справки записи клиентского приложения Gopher](../mfc/steps-in-a-typical-gopher-client-application.md)

- [Разделы справки записи клиентского приложения HTTP](../mfc/steps-in-a-typical-http-client-application.md)

## <a name="see-also"></a>См. также раздел

[Расширения Интернета Win32 (WinInet)](../mfc/win32-internet-extensions-wininet.md)<br/>
[Классы MFC для создания Интернет клиентских приложений](../mfc/mfc-classes-for-creating-internet-client-applications.md)<br/>
[Необходимые условия для клиентских классов Интернета](../mfc/prerequisites-for-internet-client-classes.md)
