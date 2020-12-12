---
description: Дополнительные сведения о действиях в типичном клиентском приложении Интернета
title: Шаги для организации типичного клиентского приложения в Интернете
ms.date: 11/04/2016
helpviewer_keywords:
- Internet client applications [MFC], general table
- WinInet classes [MFC], programming
- Internet applications [MFC], client applications
ms.assetid: 7aba135c-7c15-4e2f-8c34-bbaf792c89a6
ms.openlocfilehash: 9660687136361efb0256ecdd1fd19b577c46ab26
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216552"
---
# <a name="steps-in-a-typical-internet-client-application"></a>Шаги для организации типичного клиентского приложения в Интернете

В следующей таблице приведены действия, которые можно выполнить в обычном клиентском интернет-приложении.

|Ваша цель|Действия, которые вы принимаете|Произведенный эффект|
|---------------|----------------------|-------------|
|Начните сеанс в Интернете.|Создайте объект [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) .|Инициализирует WinInet и подключается к серверу.|
|Задайте параметр Интернет-запроса (например, предельное время ожидания или число повторных попыток).|Используйте [Цинтернетсессион:: SetOption](../mfc/reference/cinternetsession-class.md#setoption).|Возвращает значение FALSE, если операция завершилась неудачно.|
|Установите функцию обратного вызова для отслеживания состояния сеанса.|Используйте [Цинтернетсессион:: енаблестатускаллбакк](../mfc/reference/cinternetsession-class.md#enablestatuscallback).|Устанавливает обратный вызов для [Цинтернетсессион:: онстатускаллбакк](../mfc/reference/cinternetsession-class.md#onstatuscallback). Переопределите `OnStatusCallback` , чтобы создать собственную подпрограммы обратного вызова.|
|Подключитесь к серверу Интернета, серверу интрасети или локальному файлу.|Используйте [Цинтернетсессион:: OpenURL](../mfc/reference/cinternetsession-class.md#openurl).|Выполняет синтаксический анализ URL-адреса и открывает подключение к указанному серверу. Возвращает [кстдиофиле](../mfc/reference/cstdiofile-class.md) (если вы передаете `OpenURL` Локальное имя файла). Это объект, с помощью которого осуществляется доступ к данным, полученным с сервера или из файла.|
|Считывает из файла.|Используйте [Цинтернетфиле:: Read](../mfc/reference/cinternetfile-class.md#read).|Считывает указанное число байтов с помощью предоставленного буфера.|
|Выполните обработку исключений.|Используйте класс [Цинтернетексцептион](../mfc/reference/cinternetexception-class.md) .|Обрабатывает все распространенные типы исключений Интернета.|
|Завершите сеанс Интернета.|Удаление объекта [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) .|Автоматически очищает открытые дескрипторы файлов и соединения.|

## <a name="see-also"></a>См. также раздел

[Расширения Интернета Win32 (WinInet)](../mfc/win32-internet-extensions-wininet.md)<br/>
[Необходимые условия для клиентских классов Интернета](../mfc/prerequisites-for-internet-client-classes.md)<br/>
[Написание Интернет клиентского приложения с помощью классов MFC WinInet](../mfc/writing-an-internet-client-application-using-mfc-wininet-classes.md)
