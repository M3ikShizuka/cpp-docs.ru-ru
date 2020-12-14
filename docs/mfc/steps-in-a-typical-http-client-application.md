---
description: 'Дополнительные сведения: действия в типичном клиентском приложении HTTP'
title: Шаги для организации типичного клиентского приложения HTTP
ms.date: 11/04/2016
helpviewer_keywords:
- HTTP client applications [MFC]
- client applications [MFC], HTTP
- Internet applications [MFC], HTTP client applications
- applications [MFC], HTTP client
- Internet client applications [MFC], HTTP table
- WinInet classes [MFC], HTTP
ms.assetid: f86552e8-8acd-4b23-bdc5-0c3a247ebd74
ms.openlocfilehash: 0f08ca7629c389df67b579b8c20acceeb16b0cd3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216604"
---
# <a name="steps-in-a-typical-http-client-application"></a>Шаги для организации типичного клиентского приложения HTTP

В следующей таблице приведены действия, которые можно выполнить в типичном клиентском приложении HTTP.

|Ваша цель|Действия, которые вы принимаете|Произведенный эффект|
|---------------|----------------------|-------------|
|Начало сеанса HTTP.|Создайте объект [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) .|Инициализирует WinInet и подключается к серверу.|
|Подключитесь к HTTP-серверу.|Используйте [Цинтернетсессион:: жесттпконнектион](../mfc/reference/cinternetsession-class.md#gethttpconnection).|Возвращает объект [чттпконнектион](../mfc/reference/chttpconnection-class.md) .|
|Откройте HTTP-запрос.|Используйте [чттпконнектион:: опенрекуест](../mfc/reference/chttpconnection-class.md#openrequest).|Возвращает объект [чттпфиле](../mfc/reference/chttpfile-class.md) .|
|Отправка HTTP-запроса.|Используйте [чттпфиле:: аддрекуессеадерс](../mfc/reference/chttpfile-class.md#addrequestheaders) и [Чттпфиле:: SendRequest](../mfc/reference/chttpfile-class.md#sendrequest).|Находит файл. Возвращает значение FALSE, если файл не найден.|
|Считывает из файла.|Используйте [чттпфиле](../mfc/reference/chttpfile-class.md).|Считывает указанное число байтов с помощью предоставленного буфера.|
|Выполните обработку исключений.|Используйте класс [Цинтернетексцептион](../mfc/reference/cinternetexception-class.md) .|Обрабатывает все распространенные типы исключений Интернета.|
|Завершите сеанс HTTP.|Удаление объекта [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) .|Автоматически очищает открытые дескрипторы файлов и соединения.|

## <a name="see-also"></a>См. также раздел

[Расширения Интернета Win32 (WinInet)](../mfc/win32-internet-extensions-wininet.md)<br/>
[Необходимые условия для клиентских классов Интернета](../mfc/prerequisites-for-internet-client-classes.md)<br/>
[Написание Интернет клиентского приложения с помощью классов MFC WinInet](../mfc/writing-an-internet-client-application-using-mfc-wininet-classes.md)
