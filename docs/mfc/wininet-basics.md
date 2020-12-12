---
description: 'Дополнительные сведения о: Общие сведения о WinInet'
title: Основные сведения о WinInet
ms.date: 11/04/2016
helpviewer_keywords:
- OnStatusCallback method [MFC]
- WinInet classes [MFC], displaying progress
- WinInet classes [MFC], about WinInet classes
ms.assetid: 665de5ac-e80d-427d-8d91-2ae466885940
ms.openlocfilehash: 1ba8f9b898476849ca9bbb39b7850bbce3605154
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97172782"
---
# <a name="wininet-basics"></a>Основные сведения о WinInet

С помощью WinInet можно добавить поддержку FTP для скачивания и передачи файлов в приложении. Можно переопределить [онстатускаллбакк](../mfc/reference/cinternetsession-class.md#onstatuscallback) и использовать параметр *двконтекст* для предоставления пользователям сведений о ходе выполнения при поиске и скачивании файлов.

Эта статья содержит следующие разделы:

- [Создание очень простого браузера](#_core_create_a_very_simple_browser)

- [Загрузка веб-страницы](#_core_download_a_web_page)

- [FTP-файл](#_core_ftp_a_file)

- [Получение каталога Gopher](#_core_retrieve_a_gopher_directory)

- [Отображать сведения о ходе выполнения во время передачи файлов](#_core_display_progress_information_while_transferring_files)

В фрагментах кода ниже показано, как создать простой браузер, загрузить веб-страницу, файл FTP и найти файл gopher. Они не предназначены как полные примеры, а не все содержат обработку исключений.

Дополнительные сведения о WinInet см. в разделе [расширения Интернета (WinInet) Win32](../mfc/win32-internet-extensions-wininet.md).

## <a name="create-a-very-simple-browser"></a><a name="_core_create_a_very_simple_browser"></a> Создание очень простого браузера

[!code-cpp[NVC_MFCWinInet#1](../mfc/codesnippet/cpp/wininet-basics_1.cpp)]

## <a name="download-a-web-page"></a><a name="_core_download_a_web_page"></a> Загрузка веб-страницы

[!code-cpp[NVC_MFCWinInet#2](../mfc/codesnippet/cpp/wininet-basics_2.cpp)]

## <a name="ftp-a-file"></a><a name="_core_ftp_a_file"></a> FTP-файл

[!code-cpp[NVC_MFCWinInet#3](../mfc/codesnippet/cpp/wininet-basics_3.cpp)]

## <a name="retrieve-a-gopher-directory"></a><a name="_core_retrieve_a_gopher_directory"></a> Получение каталога Gopher

[!code-cpp[NVC_MFCWinInet#4](../mfc/codesnippet/cpp/wininet-basics_4.cpp)]

## <a name="use-onstatuscallback"></a>Использование Онстатускаллбакк

При использовании классов WinInet можно использовать член [онстатускаллбакк](../mfc/reference/cinternetsession-class.md#onstatuscallback) объекта [Цинтернетсессион](../mfc/reference/cinternetsession-class.md) приложения для получения сведений о состоянии. Если вы наследуете собственный `CInternetSession` объект, переопределить `OnStatusCallback` и включить обратные вызовы состояния, MFC будет вызывать `OnStatusCallback` функцию с информацией о ходе выполнения всех действий в этом сеансе Интернета.

Поскольку один сеанс может поддерживать несколько соединений (которые, в течение всего времени существования, могут выполнять множество различных операций), `OnStatusCallback` необходим механизм для определения каждого изменения состояния с определенным соединением или транзакцией. Этот механизм предоставляется параметром идентификатора контекста, присвоенным многим функциям-членам в классах поддержки WinInet. Этот параметр всегда имеет тип **DWORD** и всегда называется *двконтекст*.

Контекст, назначенный конкретному объекту Интернета, используется только для обнаружения действия, которое объект вызывает в элементе `OnStatusCallback` `CInternetSession` объекта. Вызов `OnStatusCallback` получает несколько параметров; эти параметры работают вместе, чтобы сообщить приложению, что было выполнено, для какой транзакции и подключения.

При создании `CInternetSession` объекта можно указать в конструкторе параметр *двконтекст* . `CInternetSession` сам по себе идентификатор контекста не используется; Вместо этого он передает идентификатор контекста в любые объекты, производные от **интернетконнектион**, которые явно не получают идентификатор контекста. В свою очередь эти `CInternetConnection` объекты передают идентификатор контекста в `CInternetFile` созданные объекты, если явно не указать другой идентификатор контекста. Если, с другой стороны, вы указываете собственный идентификатор контекста, объект и все выполняемые им действия будут связаны с ИДЕНТИФИКАТОРом контекста. Идентификаторы контекста можно использовать для идентификации сведений о состоянии, предоставляемых вам в `OnStatusCallback` функции.

## <a name="display-progress-information-while-transferring-files"></a><a name="_core_display_progress_information_while_transferring_files"></a> Отображать сведения о ходе выполнения во время передачи файлов

Например, при написании приложения, которое создает соединение с FTP-сервером для чтения файла и подключается к серверу HTTP для получения веб-страницы, у вас будет `CInternetSession` объект, два объекта `CInternetConnection` (один может быть, `CFtpSession` а другой — `CHttpSession` ) и два `CInternetFile` объекта (по одному для каждого соединения). Если вы использовали значения по умолчанию для параметров *двконтекст* , вы не сможете различить `OnStatusCallback` вызовы, указывающие ход выполнения FTP-соединения, и вызовы, указывающие на ход HTTP-соединения. Если указать идентификатор *двконтекст* , который впоследствии можно будет протестировать в, вы узнаете, `OnStatusCallback` какая операция создала обратный вызов.

## <a name="see-also"></a>См. также раздел

[Основные сведения о программировании Интернета MFC](../mfc/mfc-internet-programming-basics.md)<br/>
[Расширения Интернета Win32 (WinInet)](../mfc/win32-internet-extensions-wininet.md)
