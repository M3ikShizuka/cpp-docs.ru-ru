---
description: 'Дополнительные сведения: действия в типичном клиентском приложении gopher'
title: Шаги для организации типичного клиентского приложения Gopher
ms.date: 11/04/2016
helpviewer_keywords:
- WinInet classes [MFC], gopher
- Internet applications [MFC], gopher client applications
- Gopher client applications [MFC]
- Internet client applications [MFC], gopher table
ms.assetid: 3e4e1869-5da0-453d-8ba9-b648c894bb90
ms.openlocfilehash: 23940457acf52009b6d334deec129324a53a7583
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216630"
---
# <a name="steps-in-a-typical-gopher-client-application"></a>Шаги для организации типичного клиентского приложения Gopher

В следующей таблице приведены действия, которые можно выполнить в типичном клиентском приложении gopher.

|Ваша цель|Действия, которые вы принимаете|Произведенный эффект|
|---------------|----------------------|-------------|
|Начните сеанс Gopher.|Создайте объект [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) .|Инициализирует WinInet и подключается к серверу.|
|Подключитесь к серверу Gopher.|Используйте [Цинтернетсессион:: жетгоферконнектион](../mfc/reference/cinternetsession-class.md#getgopherconnection).|Возвращает объект [кгоферконнектион](../mfc/reference/cgopherconnection-class.md) .|
|Найдите первый ресурс в Gopher.|Используйте [кгоферфилефинд:: финдфиле](../mfc/reference/cgopherfilefind-class.md#findfile).|Находит первый файл. Возвращает значение FALSE, если файлы не найдены.|
|Найдите следующий ресурс в Gopher.|Используйте [кгоферфилефинд:: FindNextFile](../mfc/reference/cgopherfilefind-class.md#findnextfile).|Поиск следующего файла. Возвращает значение FALSE, если файл не найден.|
|Откройте файл, найденный `FindFile` или `FindNextFile` для чтения.|Получение локатора gopher с помощью [кгоферфилефинд::-Locator](../mfc/reference/cgopherfilefind-class.md#getlocator). Используйте [кгоферконнектион:: OpenFile](../mfc/reference/cgopherconnection-class.md#openfile).|Открывает файл, указанный указателем. `OpenFile` Возвращает объект [CGopherFile](../mfc/reference/cgopherfile-class.md) .|
|Откройте файл, используя предоставленный указатель gopher.|Создайте локатор gopher с помощью [кгоферконнектион:: CreateLocator](../mfc/reference/cgopherconnection-class.md#createlocator). Используйте [кгоферконнектион:: OpenFile](../mfc/reference/cgopherconnection-class.md#openfile).|Открывает файл, указанный указателем. `OpenFile` Возвращает объект [CGopherFile](../mfc/reference/cgopherfile-class.md) .|
|Считывает из файла.|Используйте [CGopherFile](../mfc/reference/cgopherfile-class.md).|Считывает указанное число байтов с помощью предоставленного буфера.|
|Выполните обработку исключений.|Используйте класс [Цинтернетексцептион](../mfc/reference/cinternetexception-class.md) .|Обрабатывает все распространенные типы исключений Интернета.|
|Завершите сеанс Gopher.|Удаление объекта [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) .|Автоматически очищает открытые дескрипторы файлов и соединения.|

## <a name="see-also"></a>См. также раздел

[Расширения Интернета Win32 (WinInet)](../mfc/win32-internet-extensions-wininet.md)<br/>
[Необходимые условия для клиентских классов Интернета](../mfc/prerequisites-for-internet-client-classes.md)<br/>
[Написание Интернет клиентского приложения с помощью классов MFC WinInet](../mfc/writing-an-internet-client-application-using-mfc-wininet-classes.md)
