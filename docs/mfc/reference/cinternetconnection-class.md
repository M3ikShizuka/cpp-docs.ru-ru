---
description: 'Дополнительные сведения о: Цинтернетконнектион Class'
title: Класс Цинтернетконнектион
ms.date: 11/04/2016
f1_keywords:
- CInternetConnection
- AFXINET/CInternetConnection
- AFXINET/CInternetConnection::CInternetConnection
- AFXINET/CInternetConnection::GetContext
- AFXINET/CInternetConnection::GetServerName
- AFXINET/CInternetConnection::GetSession
helpviewer_keywords:
- CInternetConnection [MFC], CInternetConnection
- CInternetConnection [MFC], GetContext
- CInternetConnection [MFC], GetServerName
- CInternetConnection [MFC], GetSession
ms.assetid: 62a5d1c3-8471-4e36-a064-48831829b2a7
ms.openlocfilehash: 2ae869e8cbf3bbfb3ce19e78088a465ae1d6aa65
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97143550"
---
# <a name="cinternetconnection-class"></a>Класс Цинтернетконнектион

Управление подключением к интернет-серверу.

## <a name="syntax"></a>Синтаксис

```
class CInternetConnection : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Цинтернетконнектион:: Цинтернетконнектион](#cinternetconnection)|Формирует объект `CInternetConnection`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Цинтернетконнектион:: SPContext](#getcontext)|Возвращает идентификатор контекста для данного объекта соединения.|
|[Цинтернетконнектион::/имя_сервера](#getservername)|Возвращает имя сервера, связанного с соединением.|
|[Цинтернетконнектион::/Session](#getsession)|Возвращает указатель на объект [Цинтернетсессион](../../mfc/reference/cinternetsession-class.md) , связанный с соединением.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Цинтернетконнектион:: operator ХИНТЕРНЕТ](#operator_hinternet)|Маркер сеанса Интернета.|

## <a name="remarks"></a>Комментарии

Это базовый класс для классов MFC [кфтпконнектион](../../mfc/reference/cftpconnection-class.md), [чттпконнектион](../../mfc/reference/chttpconnection-class.md)и [кгоферконнектион](../../mfc/reference/cgopherconnection-class.md). Каждый из этих классов предоставляет дополнительные функциональные возможности для взаимодействия с соответствующим FTP-, HTTP-или сервером Gopher.

Чтобы напрямую взаимодействовать с Интернет-сервером, необходимо иметь объект [Цинтернетсессион](../../mfc/reference/cinternetsession-class.md) и `CInternetConnection` объект.

Дополнительные сведения о работе классов WinInet см. в статье [Интернет – программирование с помощью WinInet](../../mfc/win32-internet-extensions-wininet.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CInternetConnection`

## <a name="requirements"></a>Требования

**Заголовок:** афксинет. h

## <a name="cinternetconnectioncinternetconnection"></a><a name="cinternetconnection"></a> Цинтернетконнектион:: Цинтернетконнектион

Эта функция-член вызывается при `CInternetConnection` создании объекта.

```
CInternetConnection(
    CInternetSession* pSession,
    LPCTSTR pstrServer,
    INTERNET_PORT nPort = INTERNET_INVALID_PORT_NUMBER,
    DWORD_PTR dwContext = 1);
```

### <a name="parameters"></a>Параметры

*псессион*<br/>
Указатель на объект [Цинтернетсессион](../../mfc/reference/cinternetsession-class.md) .

*пстрсервер*<br/>
Указатель на строку, содержащую имя сервера.

*Nпорт*<br/>
Номер, определяющий порт Интернета для данного соединения.

*двконтекст*<br/>
Идентификатор контекста для `CInternetConnection` объекта. Дополнительные сведения о *двконтекст* см. в разделе **Примечания** .

### <a name="remarks"></a>Комментарии

Вы никогда не вызываете `CInternetConnection` себя самостоятельно; вместо этого вызовите функцию члена [Цинтернетсессион](../../mfc/reference/cinternetsession-class.md) для типа соединения, которое нужно установить:

- [Цинтернетсессион:: Жетфтпконнектион](../../mfc/reference/cinternetsession-class.md#getftpconnection)

- [Цинтернетсессион:: Жесттпконнектион](../../mfc/reference/cinternetsession-class.md#gethttpconnection)

- [Цинтернетсессион:: Жетгоферконнектион](../../mfc/reference/cinternetsession-class.md#getgopherconnection)

Значение по умолчанию для *двконтекст* ОТПРАВЛЯЕТся библиотекой MFC `CInternetConnection` производному объекту из объекта [Цинтернетсессион](../../mfc/reference/cinternetsession-class.md) , который создал производный **интернетконнектион** объект. Значение по умолчанию — 1; Однако для соединения можно явно назначить конкретный идентификатор контекста в конструкторе [Цинтернетсессион](../../mfc/reference/cinternetsession-class.md#cinternetsession) . Объект и все его работа будут связаны с ИДЕНТИФИКАТОРом контекста. Идентификатор контекста возвращается в [Цинтернетсессион:: онстатускаллбакк](../../mfc/reference/cinternetsession-class.md#onstatuscallback) , чтобы предоставить состояние для объекта, с которым он определен. Дополнительные сведения об идентификаторе контекста см. в статье [первые шаги в Интернете: WinInet](../../mfc/wininet-basics.md) .

## <a name="cinternetconnectiongetcontext"></a><a name="getcontext"></a> Цинтернетконнектион:: SPContext

Вызовите эту функцию члена, чтобы получить идентификатор контекста для этого сеанса.

```
DWORD_PTR GetContext() const;
```

### <a name="return-value"></a>Возвращаемое значение

Идентификатор контекста, назначенный приложению.

### <a name="remarks"></a>Комментарии

Идентификатор контекста изначально указывается в [Цинтернетсессион](../../mfc/reference/cinternetsession-class.md) и распространяет на `CInternetConnection` классы, производные от [Цинтернетфиле](../../mfc/reference/cinternetfile-class.md), если не указано иное в вызове функции, открывающей соединение. Идентификатор контекста связан с любой операцией заданного объекта и определяет сведения о состоянии операции, возвращаемые [Цинтернетсессион:: онстатускаллбакк](../../mfc/reference/cinternetsession-class.md#onstatuscallback).

Дополнительные сведения о том `GetContext` , как работает с другими классами WinInet для предоставления сведений о состоянии пользователя, см. в статье [первые шаги в Интернете: WinInet](../../mfc/wininet-basics.md) для получения дополнительных сведений об идентификаторе контекста.

## <a name="cinternetconnectiongetservername"></a><a name="getservername"></a> Цинтернетконнектион::/имя_сервера

Вызовите эту функцию члена, чтобы получить имя сервера, связанного с этим подключением к Интернету.

```
CString GetServerName() const;
```

### <a name="return-value"></a>Возвращаемое значение

Имя сервера, с которым работает этот объект соединения.

## <a name="cinternetconnectiongetsession"></a><a name="getsession"></a> Цинтернетконнектион::/Session

Вызовите эту функцию-член, чтобы получить указатель на `CInternetSession` объект, связанный с этим соединением.

```
CInternetSession* GetSession() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на объект [Цинтернетсессион](../../mfc/reference/cinternetsession-class.md) , связанный с этим объектом подключения к Интернету.

## <a name="cinternetconnectionoperator-hinternet"></a><a name="operator_hinternet"></a> Цинтернетконнектион:: operator ХИНТЕРНЕТ

Используйте этот оператор, чтобы получить маркер уровня API для текущего сеанса Интернета.

```
operator HINTERNET() const;
```

## <a name="see-also"></a>См. также раздел

[CObject, класс](../../mfc/reference/cobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
