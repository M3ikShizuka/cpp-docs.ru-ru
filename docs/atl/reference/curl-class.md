---
description: 'Дополнительные сведения о: фигурном классе'
title: Классическое прилистывание
ms.date: 05/06/2019
f1_keywords:
- CUrl
- ATLUTIL/ATL::CUrl
- ATLUTIL/ATL::CUrl::CUrl
- ATLUTIL/ATL::CUrl::Canonicalize
- ATLUTIL/ATL::CUrl::Clear
- ATLUTIL/ATL::CUrl::CrackUrl
- ATLUTIL/ATL::CUrl::CreateUrl
- ATLUTIL/ATL::CUrl::GetExtraInfo
- ATLUTIL/ATL::CUrl::GetExtraInfoLength
- ATLUTIL/ATL::CUrl::GetHostName
- ATLUTIL/ATL::CUrl::GetHostNameLength
- ATLUTIL/ATL::CUrl::GetPassword
- ATLUTIL/ATL::CUrl::GetPasswordLength
- ATLUTIL/ATL::CUrl::GetPortNumber
- ATLUTIL/ATL::CUrl::GetScheme
- ATLUTIL/ATL::CUrl::GetSchemeName
- ATLUTIL/ATL::CUrl::GetSchemeNameLength
- ATLUTIL/ATL::CUrl::GetUrlLength
- ATLUTIL/ATL::CUrl::GetUrlPath
- ATLUTIL/ATL::CUrl::GetUrlPathLength
- ATLUTIL/ATL::CUrl::GetUserName
- ATLUTIL/ATL::CUrl::GetUserNameLength
- ATLUTIL/ATL::CUrl::SetExtraInfo
- ATLUTIL/ATL::CUrl::SetHostName
- ATLUTIL/ATL::CUrl::SetPassword
- ATLUTIL/ATL::CUrl::SetPortNumber
- ATLUTIL/ATL::CUrl::SetScheme
- ATLUTIL/ATL::CUrl::SetSchemeName
- ATLUTIL/ATL::CUrl::SetUrlPath
- ATLUTIL/ATL::CUrl::SetUserName
helpviewer_keywords:
- CUrl class
ms.assetid: b3894d34-47b9-4961-9719-4197153793da
ms.openlocfilehash: e8453c4dd1abbfdcb6d794b89fd55f37d7b3f286
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140300"
---
# <a name="curl-class"></a>Классическое прилистывание

Этот класс представляет URL-адрес. Он позволяет управлять каждым элементом URL-адреса независимо от того, выполняется ли синтаксический анализ существующей строки URL-адреса или создание строки с нуля.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class CUrl
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Прилистывание:: перелистывание](#curl)|Конструктор.|
|[Перелистывание:: ~](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Перелистывание:: канонизировать](#canonicalize)|Вызовите этот метод, чтобы преобразовать строку URL-адреса в каноническую форму.|
|[Прилистывание:: Clear](#clear)|Вызовите этот метод, чтобы очистить все поля URL-адреса.|
|[Перелистывание:: Краккурл](#crackurl)|Вызовите этот метод, чтобы декодировать и проанализировать URL-адрес.|
|[Перелистывание:: Креатеурл](#createurl)|Вызовите этот метод, чтобы создать URL-адрес.|
|[Перелистывание:: Жетекстраинфо](#getextrainfo)|Вызовите этот метод, чтобы получить дополнительные сведения (например, *текст* или # *Text*) из URL-адреса.|
|[Перелистывание:: Жетекстраинфоленгс](#getextrainfolength)|Вызовите этот метод, чтобы получить длину дополнительной информации (например, *текстовой* или # *Text*) для получения из URL-адреса.|
|[Прилистывание:: @ HostName](#gethostname)|Вызовите этот метод, чтобы получить имя узла из URL-адреса.|
|[Перелистывание:: Жесостнамеленгс](#gethostnamelength)|Вызовите этот метод, чтобы получить длину имени узла.|
|[Перелистывание::.](#getpassword)|Вызовите этот метод, чтобы получить пароль из URL-адреса.|
|[Перелистывание:: Жетпассвордленгс](#getpasswordlength)|Вызовите этот метод, чтобы получить длину пароля.|
|[Перелистывание:: GetPortNumber](#getportnumber)|Вызовите этот метод, чтобы получить номер порта с точки зрения ATL_URL_PORT.|
|[Прилистывание:: к схеме](#getscheme)|Вызовите этот метод, чтобы получить схему URL-адресов.|
|[Перелистывание:: Жетсчеменаме](#getschemename)|Вызовите этот метод, чтобы получить имя схемы URL-адреса.|
|[Перелистывание:: Жетсчеменамеленгс](#getschemenamelength)|Вызовите этот метод, чтобы получить длину имени схемы URL-адреса.|
|[Перелистывание:: Жетурлленгс](#geturllength)|Вызовите этот метод, чтобы получить длину URL-адреса.|
|[Перелистывание:: Жетурлпас](#geturlpath)|Вызовите этот метод, чтобы получить URL-путь.|
|[Перелистывание:: Жетурлпасленгс](#geturlpathlength)|Вызовите этот метод, чтобы получить длину URL-пути.|
|[Прилистывание:: имя пользователя](#getusername)|Вызовите этот метод, чтобы получить имя пользователя из URL-адреса.|
|[Перелистывание:: Жетусернамеленгс](#getusernamelength)|Вызовите этот метод, чтобы получить длину имени пользователя.|
|[Перелистывание:: Сетекстраинфо](#setextrainfo)|Вызовите этот метод, чтобы задать дополнительные сведения (например, *текст* или *текст*) URL-адреса.|
|[Перелистывание:: Сесостнаме](#sethostname)|Вызовите этот метод, чтобы задать имя узла.|
|[Перелистывание:: SetPassword](#setpassword)|Вызовите этот метод, чтобы задать пароль.|
|[Перелистывание:: SetPortNumber](#setportnumber)|Вызовите этот метод, чтобы задать номер порта в терминах ATL_URL_PORT.|
|[Перелистывание:: Сетсчеме](#setscheme)|Вызовите этот метод, чтобы задать схему URL-адресов.|
|[Перелистывание:: Сетсчеменаме](#setschemename)|Вызовите этот метод, чтобы задать имя схемы URL-адреса.|
|[Перелистывание:: Сетурлпас](#seturlpath)|Вызовите этот метод, чтобы задать URL-путь.|
|[Перелистывание:: Сетусернаме](#setusername)|Вызовите этот метод, чтобы задать имя пользователя.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Прилистывание:: operator =](#operator_eq)|Присваивает указанный `CUrl` объект текущему `CUrl` объекту.|

## <a name="remarks"></a>Комментарии

`CUrl` позволяет управлять полями URL-адреса, например путем или номером порта. `CUrl` распознает URL-адреса следующего вида:

\<Scheme>://\<UserName>:\<Password>\@\<HostName>:\<PortNumber>/\<UrlPath>\<ExtraInfo>

(Некоторые поля являются необязательными.) Например, рассмотрим следующий URL-адрес:

`http://someone:secret@www.microsoft.com:80/visualc/stuff.htm#contents`

В следующем виде: [: краккурл](#crackurl) анализируется следующим образом:

- Схема: "http" или [ATL_URL_SCHEME_HTTP](atl-url-scheme-enum.md)

- UserName: "кто-нибудь"

- Пароль: "секрет"

- Имя узла: " `www.microsoft.com` "

- Номер_порта: 80

- Урлпас: "VisualC/stuff.htm"

- Екстраинфо: "#contents"

Для работы с полем Урлпас (например,) следует использовать [жетурлпас](#geturlpath), [жетурлпасленгс](#geturlpathlength)и [сетурлпас](#seturlpath). Для создания полной строки URL-адреса следует использовать [креатеурл](#createurl) .

## <a name="requirements"></a>Требования

**Заголовок:** файлов atlutil. h

## <a name="curlcanonicalize"></a><a name="canonicalize"></a> Перелистывание:: канонизировать

Вызовите этот метод, чтобы преобразовать строку URL-адреса в каноническую форму.

```
inline BOOL Canonicalize(DWORD dwFlags = 0) throw();
```

### <a name="parameters"></a>Параметры

*dwFlags*<br/>
Флаги, управляющие каноническим контролем. Если флаги не указаны (*dwFlags* = 0), метод преобразует все ненадежные символы и метатеги (такие как \\ ., \.. и \\ ...) в escape-последовательности. *dwFlags* может иметь одно из следующих значений:

- ATL_URL_BROWSER_MODE: не кодирует и не декодировать символы после "#" или "" и не удаляет конечные пробелы после "". Если это значение не указано, то весь URL-адрес кодируется, а конечные пробелы удаляются.

- ATL_URL _DECODE: преобразует все последовательности% XX в символы, включая escape-последовательности, перед синтаксическим анализом URL.

- ATL_URL _ENCODE_PERCENT: кодирует все обнаруженные знаки процентов. По умолчанию знаки процента не кодируются.

- ATL_URL _ENCODE_SPACES_ONLY: кодирует только пробелы.

- ATL_URL _NO_ENCODE: не преобразует ненадежные символы в escape-последовательности.

- ATL_URL _NO_META: не удаляет метаданные (например, "." и "..") из URL-адреса.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

### <a name="remarks"></a>Комментарии

Преобразование в каноническую форму включает преобразование незащищенных символов и пробелов в escape-последовательности.

## <a name="curlclear"></a><a name="clear"></a> Прилистывание:: Clear

Вызовите этот метод, чтобы очистить все поля URL-адреса.

```
inline void Clear() throw();
```

## <a name="curlcrackurl"></a><a name="crackurl"></a> Перелистывание:: Краккурл

Вызовите этот метод, чтобы декодировать и проанализировать URL-адрес.

```
BOOL CrackUrl(LPCTSTR lpszUrl, DWORD dwFlags = 0) throw();
```

### <a name="parameters"></a>Параметры

*лпсзурл*<br/>
URL-адрес.

*dwFlags*<br/>
Укажите ATL_URL_DECODE или ATL_URL_ESCAPE, чтобы преобразовать все escape-символы в *лпсзурл* к их реальным значениям после синтаксического анализа. (Перед Visual C++ 2005 ATL_URL_DECODE преобразует все escape-символы перед синтаксическим анализом.)

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

## <a name="curlcreateurl"></a><a name="createurl"></a> Перелистывание:: Креатеурл

Этот метод конструирует строку URL-адреса из полей компонента фигурного объекта.

```
inline BOOL CreateUrl(
    LPTSTR lpszUrl,
    DWORD* pdwMaxLength,
    DWORD dwFlags = 0) const throw();
```

### <a name="parameters"></a>Параметры

*лпсзурл*<br/>
Строковый буфер для хранения полной строки URL-адреса.

*пдвмаксленгс*<br/>
Максимальная длина буфера строки *лпсзурл* .

*dwFlags*<br/>
Укажите ATL_URL_ESCAPE, чтобы преобразовать все escape-символы в *лпсзурл* к их реальным значениям.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

### <a name="remarks"></a>Комментарии

Этот метод добавляет отдельные поля для создания полной строки URL-адреса, используя следующий формат:

**\<scheme>://\<user>:\<pass>\@\<domain>:\<port>\<path>\<extra>**

При вызове этого метода параметр *пдвмаксленгс* должен изначально содержать максимальную длину строкового буфера, на который ссылается параметр *лпсзурл* . Значение параметра *пдвмаксленгс* будет изменено на фактическую длину строки URL-адреса.

### <a name="example"></a>Пример

В этом примере демонстрируется создание объекта с фигурными скобками и получение его строки URL-адреса

[!code-cpp[NVC_ATL_Utilities#133](../../atl/codesnippet/cpp/curl-class_1.cpp)]

## <a name="curlcurl"></a><a name="curl"></a> Прилистывание:: перелистывание

Конструктор.

```
CUrl() throw();
CUrl(const CUrl& urlThat) throw();
```

### <a name="parameters"></a>Параметры

*урлсат*<br/>
`CUrl`Копируемый объект для создания URL-адреса.

## <a name="curlcurl"></a><a name="dtor"></a> Перелистывание:: ~

Деструктор

```
~CUrl() throw();
```

## <a name="curlgetextrainfo"></a><a name="getextrainfo"></a> Перелистывание:: Жетекстраинфо

Вызовите этот метод, чтобы получить дополнительные сведения (например, *текст* или # *Text*) из URL-адреса.

```
inline LPCTSTR GetExtraInfo() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает строку, содержащую дополнительные сведения.

## <a name="curlgetextrainfolength"></a><a name="getextrainfolength"></a> Перелистывание:: Жетекстраинфоленгс

Вызовите этот метод, чтобы получить длину дополнительной информации (например, *текстовой* или # *Text*) для получения из URL-адреса.

```
inline DWORD GetExtraInfoLength() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает длину строки, содержащей дополнительные сведения.

## <a name="curlgethostname"></a><a name="gethostname"></a> Прилистывание:: @ HostName

Вызовите этот метод, чтобы получить имя узла из URL-адреса.

```
inline LPCTSTR GetHostName() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает имя узла.

## <a name="curlgethostnamelength"></a><a name="gethostnamelength"></a> Перелистывание:: Жесостнамеленгс

Вызовите этот метод, чтобы получить длину имени узла.

```
inline DWORD GetHostNameLength() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает длину имени узла.

## <a name="curlgetpassword"></a><a name="getpassword"></a> Перелистывание::.

Вызовите этот метод, чтобы получить пароль из URL-адреса.

```
inline LPCTSTR GetPassword() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает пароль.

## <a name="curlgetpasswordlength"></a><a name="getpasswordlength"></a> Перелистывание:: Жетпассвордленгс

Вызовите этот метод, чтобы получить длину пароля.

```
inline DWORD GetPasswordLength() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает длину пароля.

## <a name="curlgetportnumber"></a><a name="getportnumber"></a> Перелистывание:: GetPortNumber

Вызовите этот метод, чтобы получить номер порта.

```
inline ATL_URL_PORT GetPortNumber() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает номер порта.

## <a name="curlgetscheme"></a><a name="getscheme"></a> Прилистывание:: к схеме

Вызовите этот метод, чтобы получить схему URL-адресов.

```
inline ATL_URL_SCHEME GetScheme() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение [ATL_URL_SCHEME](atl-url-scheme-enum.md) , описывающее схему URL-адреса.

## <a name="curlgetschemename"></a><a name="getschemename"></a> Перелистывание:: Жетсчеменаме

Вызовите этот метод, чтобы получить имя схемы URL-адреса.

```
inline LPCTSTR GetSchemeName() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает имя схемы URL-адреса (например, "http" или "FTP").

## <a name="curlgetschemenamelength"></a><a name="getschemenamelength"></a> Перелистывание:: Жетсчеменамеленгс

Вызовите этот метод, чтобы получить длину имени схемы URL-адреса.

```
inline DWORD GetSchemeNameLength() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает длину имени схемы URL-адреса.

## <a name="curlgeturllength"></a><a name="geturllength"></a> Перелистывание:: Жетурлленгс

Вызовите этот метод, чтобы получить длину URL-адреса.

```
inline DWORD GetUrlLength() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает длину URL-адреса.

## <a name="curlgeturlpath"></a><a name="geturlpath"></a> Перелистывание:: Жетурлпас

Вызовите этот метод, чтобы получить URL-путь.

```
inline LPCTSTR GetUrlPath() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает URL-путь.

## <a name="curlgeturlpathlength"></a><a name="geturlpathlength"></a> Перелистывание:: Жетурлпасленгс

Вызовите этот метод, чтобы получить длину URL-пути.

```
inline DWORD GetUrlPathLength() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает длину URL-пути.

## <a name="curlgetusername"></a><a name="getusername"></a> Прилистывание:: имя пользователя

Вызовите этот метод, чтобы получить имя пользователя из URL-адреса.

```
inline LPCTSTR GetUserName() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает имя пользователя.

## <a name="curlgetusernamelength"></a><a name="getusernamelength"></a> Перелистывание:: Жетусернамеленгс

Вызовите этот метод, чтобы получить длину имени пользователя.

```
inline DWORD GetUserNameLength() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает длину имени пользователя.

## <a name="curloperator-"></a><a name="operator_eq"></a> Прилистывание:: operator =

Присваивает указанный `CUrl` объект текущему `CUrl` объекту.

```
CUrl& operator= (const CUrl& urlThat) throw();
```

### <a name="parameters"></a>Параметры

*урлсат*<br/>
`CUrl`Объект, который необходимо скопировать в текущий объект.

### <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку на текущий объект.

## <a name="curlsetextrainfo"></a><a name="setextrainfo"></a> Перелистывание:: Сетекстраинфо

Вызовите этот метод, чтобы задать дополнительные сведения (например, *текст* или *текст*) URL-адреса.

```
inline BOOL SetExtraInfo(LPCTSTR lpszInfo) throw();
```

### <a name="parameters"></a>Параметры

*лпсзинфо*<br/>
Строка, содержащая дополнительные сведения, включаемые в URL-адрес.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

## <a name="curlsethostname"></a><a name="sethostname"></a> Перелистывание:: Сесостнаме

Вызовите этот метод, чтобы задать имя узла.

```
inline BOOL SetHostName(LPCTSTR lpszHost) throw();
```

### <a name="parameters"></a>Параметры

*лпсзост*<br/>
Имя сервера.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

## <a name="curlsetpassword"></a><a name="setpassword"></a> Перелистывание:: SetPassword

Вызовите этот метод, чтобы задать пароль.

```
inline BOOL SetPassword(LPCTSTR lpszPass) throw();
```

### <a name="parameters"></a>Параметры

*лпсзпасс*<br/>
Пароль.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

## <a name="curlsetportnumber"></a><a name="setportnumber"></a> Перелистывание:: SetPortNumber

Вызовите этот метод, чтобы задать номер порта.

```
inline BOOL SetPortNumber(ATL_URL_PORT nPrt) throw();
```

### <a name="parameters"></a>Параметры

*нпрт*<br/>
номер порта.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

## <a name="curlsetscheme"></a><a name="setscheme"></a> Перелистывание:: Сетсчеме

Вызовите этот метод, чтобы задать схему URL-адресов.

```
inline BOOL SetScheme(ATL_URL_SCHEME nScheme) throw();
```

### <a name="parameters"></a>Параметры

*нсчеме*<br/>
Одно из значений [ATL_URL_SCHEME](atl-url-scheme-enum.md) для схемы.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

### <a name="remarks"></a>Комментарии

Схему также можно задать по имени (см. раздел " [сетсчеменаме](#setschemename)").

## <a name="curlsetschemename"></a><a name="setschemename"></a> Перелистывание:: Сетсчеменаме

Вызовите этот метод, чтобы задать имя схемы URL-адреса.

```
inline BOOL SetSchemeName(LPCTSTR lpszSchm) throw();
```

### <a name="parameters"></a>Параметры

*лпсзсчм*<br/>
Имя схемы URL-адреса.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

### <a name="remarks"></a>Комментарии

Схему также можно задать с помощью [ATL_URL_SCHEMEной](atl-url-scheme-enum.md) константы (см. раздел " [сетсчеме](#setscheme)").

## <a name="curlseturlpath"></a><a name="seturlpath"></a> Перелистывание:: Сетурлпас

Вызовите этот метод, чтобы задать URL-путь.

```
inline BOOL SetUrlPath(LPCTSTR lpszPath) throw();
```

### <a name="parameters"></a>Параметры

*лпсзпас*<br/>
Путь URL-адреса.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

## <a name="curlsetusername"></a><a name="setusername"></a> Перелистывание:: Сетусернаме

Вызовите этот метод, чтобы задать имя пользователя.

```
inline BOOL SetUserName(LPCTSTR lpszUser) throw();
```

### <a name="parameters"></a>Параметры

*лпсзусер*<br/>
Имя пользователя.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

## <a name="see-also"></a>См. также раздел

[Классы](../../atl/reference/atl-classes.md)
