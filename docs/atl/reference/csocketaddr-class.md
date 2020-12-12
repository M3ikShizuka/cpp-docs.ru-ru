---
description: 'Дополнительные сведения о: Ксоккетаддр Class'
title: Класс Ксоккетаддр
ms.date: 10/22/2018
f1_keywords:
- CSocketAddr
- ATLSOCKET/ATL::CSocketAddr
- ATLSOCKET/ATL::CSocketAddr::CSocketAddr
- ATLSOCKET/ATL::CSocketAddr::FindAddr
- ATLSOCKET/ATL::CSocketAddr::FindINET4Addr
- ATLSOCKET/ATL::CSocketAddr::FindINET6Addr
- ATLSOCKET/ATL::CSocketAddr::GetAddrInfo
- ATLSOCKET/ATL::CSocketAddr::GetAddrInfoList
helpviewer_keywords:
- CSocketAddr class
ms.assetid: 2fb2d8a7-899e-4a36-a342-cc9f4fcdd68c
ms.openlocfilehash: eff93b6a8e6d0ea487e3571cd52973d9e17115d2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140533"
---
# <a name="csocketaddr-class"></a>Класс Ксоккетаддр

Этот класс предоставляет методы для преобразования имен узлов в адреса узлов, поддерживающих форматы IPv4 и IPV6.

## <a name="syntax"></a>Синтаксис

```
class CSocketAddr
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ксоккетаддр:: Ксоккетаддр](#csocketaddr)|Конструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксоккетаддр:: Финдаддр](#findaddr)|Вызовите этот метод, чтобы преобразовать предоставленное имя узла в адрес узла.|
|[Ксоккетаддр:: FindINET4Addr](#findinet4addr)|Вызовите этот метод, чтобы преобразовать имя узла IPv4 в адрес узла.|
|[Ксоккетаддр:: FindINET6Addr](#findinet6addr)|Вызовите этот метод, чтобы преобразовать имя узла IPv6 в адрес узла.|
|[Ксоккетаддр:: функцию getaddrinfo](#getaddrinfo)|Вызовите этот метод, чтобы вернуть указатель на конкретный элемент в `addrinfo` списке.|
|[Ксоккетаддр:: Жетаддринфолист](#getaddrinfolist)|Вызовите этот метод, чтобы вернуть указатель на `addrinfo` список.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет независимый от IP-версии подход к поиску сетевых адресов для использования с функциями API сокетов Windows и оболочками сокетов в библиотеках.

Члены этого класса, используемые для поиска сетевых адресов, используют функцию Win32 API [функцию getaddrinfo](/windows/win32/api/ws2tcpip/nf-ws2tcpip-getaddrinfo). Версия функции ANSI или UNICODE вызывается в зависимости от того, скомпилирован ли код для ANSI или UNICODE.

Этот класс поддерживает как сетевые адреса IPv4 andIPv6.

## <a name="requirements"></a>Требования

**Заголовок:** атлсоккет. h

## <a name="csocketaddrcsocketaddr"></a><a name="csocketaddr"></a> Ксоккетаддр:: Ксоккетаддр

Конструктор.

```
CSocketAddr();
```

### <a name="remarks"></a>Комментарии

Создает новый `CSocketAddr` объект и инициализирует связанный список, содержащий сведения об ответе узла.

## <a name="csocketaddrfindaddr"></a><a name="findaddr"></a> Ксоккетаддр:: Финдаддр

Вызовите этот метод, чтобы преобразовать предоставленное имя узла в адрес узла.

```
int FindAddr(
    const TCHAR *szHost,
    const TCHAR *szPortOrServiceName,
    int flags,
    int addr_family,
    int sock_type,
    int ai_proto);

int FindAddr(
    const TCHAR *szHost,
    int nPortNo,
    int flags,
    int addr_family,
    int sock_type,
    int ai_proto);
```

### <a name="parameters"></a>Параметры

*сзост*<br/>
Имя узла или IP-адрес с точками.

*сзпорторсервиценаме*<br/>
Номер порта или имя службы на узле.

*нпортно*<br/>
номер порта.

*flags*<br/>
0 или сочетание AI_PASSIVE, AI_CANONNAME или AI_NUMERICHOST.

*addr_family*<br/>
Семейство адресов (например, PF_INET).

*sock_type*<br/>
Тип сокета (например, SOCK_STREAM).

*ai_proto*<br/>
Протокол (например, IPPROTO_IP или IPPROTO_IPV6).

### <a name="return-value"></a>Возвращаемое значение

Возвращает нуль, если адрес успешно вычислен. Возвращает ненулевое значение кода ошибки сокета Windows при сбое. В случае успеха вычисленный адрес сохраняется в связанном списке, на который можно ссылаться с помощью `CSocketAddr::GetAddrInfoList` и `CSocketAddr::GetAddrInfo` .

### <a name="remarks"></a>Комментарии

Параметр имени узла может иметь формат IPv4 или IPv6. Этот метод вызывает функцию Win32 API [функцию getaddrinfo](/windows/win32/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) для выполнения преобразования.

## <a name="csocketaddrfindinet4addr"></a><a name="findinet4addr"></a> Ксоккетаддр:: FindINET4Addr

Вызовите этот метод, чтобы преобразовать имя узла IPv4 в адрес узла.

```
int FindINET4Addr(
    const TCHAR *szHost,
    int nPortNo,
    int flags = 0,
    int sock_type = SOCK_STREAM);
```

### <a name="parameters"></a>Параметры

*сзост*<br/>
Имя узла или IP-адрес с точками.

*нпортно*<br/>
номер порта.

*flags*<br/>
0 или сочетание AI_PASSIVE, AI_CANONNAME или AI_NUMERICHOST.

*sock_type*<br/>
Тип сокета (например, SOCK_STREAM).

### <a name="return-value"></a>Возвращаемое значение

Возвращает нуль, если адрес успешно вычислен. Возвращает ненулевое значение кода ошибки сокета Windows при сбое. В случае успеха вычисленный адрес сохраняется в связанном списке, на который можно ссылаться с помощью `CSocketAddr::GetAddrInfoList` и `CSocketAddr::GetAddrInfo` .

### <a name="remarks"></a>Комментарии

Этот метод вызывает функцию Win32 API [функцию getaddrinfo](/windows/win32/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) для выполнения преобразования.

## <a name="csocketaddrfindinet6addr"></a><a name="findinet6addr"></a> Ксоккетаддр:: FindINET6Addr

Вызовите этот метод, чтобы преобразовать имя узла IPv6 в адрес узла.

```
int FindINET6Addr(
    const TCHAR *szHost,
    int nPortNo,
    int flags = 0,
    int sock_type = SOCK_STREAM);
```

### <a name="parameters"></a>Параметры

*сзост*<br/>
Имя узла или IP-адрес с точками.

*нпортно*<br/>
номер порта.

*flags*<br/>
0 или сочетание AI_PASSIVE, AI_CANONNAME или AI_NUMERICHOST.

*sock_type*<br/>
Тип сокета (например, SOCK_STREAM).

### <a name="return-value"></a>Возвращаемое значение

Возвращает нуль, если адрес успешно вычислен. Возвращает ненулевое значение кода ошибки сокета Windows при сбое. В случае успеха вычисленный адрес сохраняется в связанном списке, на который можно ссылаться с помощью `CSocketAddr::GetAddrInfoList` и `CSocketAddr::GetAddrInfo` .

### <a name="remarks"></a>Комментарии

Этот метод вызывает функцию Win32 API [функцию getaddrinfo](/windows/win32/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) для выполнения преобразования.

## <a name="csocketaddrgetaddrinfo"></a><a name="getaddrinfo"></a> Ксоккетаддр:: функцию getaddrinfo

Вызовите этот метод, чтобы вернуть указатель на конкретный элемент в `addrinfo` списке.

```
addrinfo* const GetAddrInfo(int nIndex = 0) const;
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
Ссылка на конкретный элемент в списке [аддринфо](/windows/win32/api/ws2def/ns-ws2def-addrinfow) .

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на `addrinfo` структуру, на которую ссылается *ниндекс* , в связанном списке, содержащем сведения об ответе для узла.

## <a name="csocketaddrgetaddrinfolist"></a><a name="getaddrinfolist"></a> Ксоккетаддр:: Жетаддринфолист

Вызовите этот метод, чтобы вернуть указатель на `addrinfo` список.

```
addrinfo* const GetAddrInfoList() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на связанный список из одной или нескольких `addrinfo` структур, содержащих сведения об ответе для узла. Дополнительные сведения см. в разделе [Структура аддринфо](/windows/win32/api/ws2def/ns-ws2def-addrinfow).

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
