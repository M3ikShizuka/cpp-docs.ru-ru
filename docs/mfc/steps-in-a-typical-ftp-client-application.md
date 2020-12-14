---
description: 'Дополнительные сведения: действия в типичном клиентском приложении FTP'
title: Шаги для организации типичного клиентского приложения FTP
ms.date: 11/04/2016
helpviewer_keywords:
- Internet client applications [MFC], FTP table
- FTP (File Transfer Protocol)
- WinInet classes [MFC], FTP
- FTP (File Transfer Protocol) [MFC], client applications
- Internet applications [MFC], FTP client applications
ms.assetid: 70bed7b5-6040-40d1-bc77-702e63a698f2
ms.openlocfilehash: caac613adf3ad886c4b36ae567a3b8c5c928ee10
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216643"
---
# <a name="steps-in-a-typical-ftp-client-application"></a>Шаги для организации типичного клиентского приложения FTP

Типичное клиентское приложение FTP создает [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) и объект [кфтпконнектион](../mfc/reference/cftpconnection-class.md) . Обратите внимание, что эти классы MFC WinInet фактически не управляют параметрами типа прокси-сервера. Службы IIS.

В следующей таблице приведены действия, которые можно выполнить в типичном клиентском приложении FTP.

|Ваша цель|Действия, которые вы принимаете|Произведенный эффект|
|---------------|----------------------|-------------|
|Начните сеанс FTP.|Создайте объект [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) .|Инициализирует WinInet и подключается к серверу.|
|Подключается к FTP-серверу.|Используйте [Цинтернетсессион:: жетфтпконнектион](../mfc/reference/cinternetsession-class.md#getftpconnection).|Возвращает объект [кфтпконнектион](../mfc/reference/cftpconnection-class.md) .|
|Перейдите в новый каталог FTP на сервере.|Используйте [кфтпконнектион:: сеткуррентдиректори](../mfc/reference/cftpconnection-class.md#setcurrentdirectory).|Изменяет каталог, к которому вы подключены в данный момент на сервере.|
|Найти первый файл в каталоге FTP.|Используйте [кфтпфилефинд:: финдфиле](../mfc/reference/cftpfilefind-class.md#findfile).|Находит первый файл. Возвращает значение FALSE, если файлы не найдены.|
|Найдите следующий файл в каталоге FTP.|Используйте [кфтпфилефинд:: FindNextFile](../mfc/reference/cftpfilefind-class.md#findnextfile).|Поиск следующего файла. Возвращает значение FALSE, если файл не найден.|
|Откройте файл, найденный `FindFile` или `FindNextFile` для чтения или записи.|Используйте [кфтпконнектион:: OpenFile](../mfc/reference/cftpconnection-class.md#openfile), используя имя файла, возвращенное [финдфиле](../mfc/reference/cftpfilefind-class.md#findfile) или [FindNextFile](../mfc/reference/cftpfilefind-class.md#findnextfile).|Открывает файл на сервере для чтения или записи. Возвращает объект [Цинтернетфиле](../mfc/reference/cinternetfile-class.md) .|
|Чтение из файла или запись в него.|Используйте [Цинтернетфиле:: Read](../mfc/reference/cinternetfile-class.md#read) или [Цинтернетфиле:: Write](../mfc/reference/cinternetfile-class.md#write).|Считывает или записывает указанное число байтов, используя предоставленный буфер.|
|Выполните обработку исключений.|Используйте класс [Цинтернетексцептион](../mfc/reference/cinternetexception-class.md) .|Обрабатывает все распространенные типы исключений Интернета.|
|Завершите сеанс FTP.|Удаление объекта [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) .|Автоматически очищает открытые дескрипторы файлов и соединения.|

## <a name="see-also"></a>См. также раздел

[Расширения Интернета Win32 (WinInet)](../mfc/win32-internet-extensions-wininet.md)<br/>
[Необходимые условия для клиентских классов Интернета](../mfc/prerequisites-for-internet-client-classes.md)<br/>
[Написание Интернет клиентского приложения с помощью классов MFC WinInet](../mfc/writing-an-internet-client-application-using-mfc-wininet-classes.md)
