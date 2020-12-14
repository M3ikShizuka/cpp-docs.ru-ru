---
description: 'Дополнительные сведения: действия в типичном клиентском приложении FTP для удаления файла'
title: Шаги для удаления файла в типичном клиентском приложении FTP
ms.date: 11/04/2016
helpviewer_keywords:
- Internet client applications [MFC], FTP delete
- WinInet classes [MFC], FTP
- FTP (File Transfer Protocol) [MFC], client applications
- Internet applications [MFC], FTP client applications
ms.assetid: 2c347a96-c0a4-4827-98fe-668406e552bc
ms.openlocfilehash: 0de5ba71ac127a44c964571d243997bcb49faaa0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216656"
---
# <a name="steps-in-a-typical-ftp-client-application-to-delete-a-file"></a>Шаги для удаления файла в типичном клиентском приложении FTP

В следующей таблице приведены действия, которые можно выполнить в типичном клиентском приложении FTP, которое удаляет файл.

|Ваша цель|Действия, которые вы принимаете|Произведенный эффект|
|---------------|----------------------|-------------|
|Начните сеанс FTP.|Создайте объект [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) .|Инициализирует WinInet и подключается к серверу.|
|Подключается к FTP-серверу.|Используйте [Цинтернетсессион:: жетфтпконнектион](../mfc/reference/cinternetsession-class.md#getftpconnection).|Возвращает объект [кфтпконнектион](../mfc/reference/cftpconnection-class.md) .|
|Убедитесь, что вы находитесь в правильном каталоге на FTP-сервере.|Используйте [кфтпконнектион:: GetCurrentDirectory](../mfc/reference/cftpconnection-class.md#getcurrentdirectory) или [Кфтпконнектион:: жеткуррентдиректорясурл](../mfc/reference/cftpconnection-class.md#getcurrentdirectoryasurl).|Возвращает имя или URL-адрес каталога, к которому вы подключены в данный момент на сервере, в зависимости от выбранной функции-члена.|
|Перейдите в новый каталог FTP на сервере.|Используйте [кфтпконнектион:: сеткуррентдиректори](../mfc/reference/cftpconnection-class.md#setcurrentdirectory).|Изменяет каталог, к которому вы подключены в данный момент на сервере.|
|Найти первый файл в каталоге FTP.|Используйте [кфтпфилефинд:: финдфиле](../mfc/reference/cftpfilefind-class.md#findfile).|Находит первый файл. Возвращает значение FALSE, если файлы не найдены.|
|Найдите следующий файл в каталоге FTP.|Используйте [кфтпфилефинд:: FindNextFile](../mfc/reference/cftpfilefind-class.md#findnextfile).|Поиск следующего файла. Возвращает значение FALSE, если файл не найден.|
|Удалите файл, найденный `FindFile` или `FindNextFile` .|Используйте [кфтпконнектион:: Remove](../mfc/reference/cftpconnection-class.md#remove), используя имя файла, возвращенное `FindFile` или `FindNextFile` .|Удаляет файл на сервере для чтения или записи.|
|Выполните обработку исключений.|Используйте класс [Цинтернетексцептион](../mfc/reference/cinternetexception-class.md) .|Обрабатывает все распространенные типы исключений Интернета.|
|Завершите сеанс FTP.|Удаление объекта [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) .|Автоматически очищает открытые дескрипторы файлов и соединения.|

## <a name="see-also"></a>См. также раздел

[Расширения Интернета Win32 (WinInet)](../mfc/win32-internet-extensions-wininet.md)<br/>
[Необходимые условия для клиентских классов Интернета](../mfc/prerequisites-for-internet-client-classes.md)<br/>
[Написание Интернет клиентского приложения с помощью классов MFC WinInet](../mfc/writing-an-internet-client-application-using-mfc-wininet-classes.md)
