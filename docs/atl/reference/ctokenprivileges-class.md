---
description: 'Дополнительные сведения о: Ктокенпривилежес Class'
title: Класс Ктокенпривилежес
ms.date: 11/04/2016
f1_keywords:
- CTokenPrivileges
- ATLSECURITY/ATL::CTokenPrivileges
- ATLSECURITY/ATL::CTokenPrivileges::CTokenPrivileges
- ATLSECURITY/ATL::CTokenPrivileges::Add
- ATLSECURITY/ATL::CTokenPrivileges::Delete
- ATLSECURITY/ATL::CTokenPrivileges::DeleteAll
- ATLSECURITY/ATL::CTokenPrivileges::GetCount
- ATLSECURITY/ATL::CTokenPrivileges::GetDisplayNames
- ATLSECURITY/ATL::CTokenPrivileges::GetLength
- ATLSECURITY/ATL::CTokenPrivileges::GetLuidsAndAttributes
- ATLSECURITY/ATL::CTokenPrivileges::GetNamesAndAttributes
- ATLSECURITY/ATL::CTokenPrivileges::GetPTOKEN_PRIVILEGES
- ATLSECURITY/ATL::CTokenPrivileges::LookupPrivilege
helpviewer_keywords:
- CTokenPrivileges class
ms.assetid: 89590105-f001-4014-870d-142926091231
ms.openlocfilehash: 22953c0d2aa8c4fa7dd0b79b001e46797bd3ca25
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140313"
---
# <a name="ctokenprivileges-class"></a>Класс Ктокенпривилежес

Этот класс является оболочкой для `TOKEN_PRIVILEGES` структуры.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class CTokenPrivileges
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ктокенпривилежес:: Ктокенпривилежес](#ctokenprivileges)|Конструктор.|
|[Ктокенпривилежес:: ~ Ктокенпривилежес](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ктокенпривилежес:: Add](#add)|Добавляет один или несколько привилегий к `CTokenPrivileges` объекту.|
|[Ктокенпривилежес::D удалить](#delete)|Удаляет права доступа из `CTokenPrivileges` объекта.|
|[Ктокенпривилежес::D Елетеалл](#deleteall)|Удаляет все привилегии из `CTokenPrivileges` объекта.|
|[Ктокенпривилежес:: NOCOUNT](#getcount)|Возвращает число записей привилегий в `CTokenPrivileges` объекте.|
|[Ктокенпривилежес:: DisplayName](#getdisplaynames)|Извлекает отображаемые имена для привилегий, содержащихся в `CTokenPrivileges` объекте.|
|[Ктокенпривилежес:: DATALENGTH](#getlength)|Возвращает размер буфера в байтах, необходимый для хранения `TOKEN_PRIVILEGES` структуры, представленной `CTokenPrivileges` объектом.|
|[Ктокенпривилежес:: Жетлуидсандаттрибутес](#getluidsandattributes)|Извлекает локально уникальные идентификаторы (LUID) и флаги атрибутов из `CTokenPrivileges` объекта.|
|[Ктокенпривилежес:: Жетнамесандаттрибутес](#getnamesandattributes)|Возвращает имена привилегий и флаги атрибутов из `CTokenPrivileges` объекта.|
|[Ктокенпривилежес:: GetPTOKEN_PRIVILEGES](#getptoken_privileges)|Возвращает указатель на `TOKEN_PRIVILEGES` структуру.|
|[Ктокенпривилежес:: Лукуппривилеже](#lookupprivilege)|Извлекает атрибут, связанный с заданным именем привилегии.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Ктокенпривилежес:: operator const TOKEN_PRIVILEGES *](#operator_const_token_privileges__star)|Приводит значение к указателю на `TOKEN_PRIVILEGES` структуру.|
|[Ктокенпривилежес:: operator =](#operator_eq)|Оператор присвоения.|

## <a name="remarks"></a>Комментарии

[Маркер доступа](/windows/win32/SecAuthZ/access-tokens) — это объект, который описывает контекст безопасности процесса или потока и выделяется каждому пользователю, вошедшему в систему Windows.

Маркер доступа используется для описания различных привилегий безопасности, предоставляемых каждому пользователю. Привилегия состоит из 64-разрядного числа, которое называется локальным уникальным идентификатором ( [LUID](/windows/win32/api/winnt/ns-winnt-luid)) и строкой дескриптора.

`CTokenPrivileges`Класс является оболочкой для структуры [TOKEN_PRIVILEGES](/windows/win32/api/winnt/ns-winnt-token_privileges) и содержит 0 или более привилегий. Права доступа могут добавляться, удаляться или запрашиваться с помощью предоставленных методов класса.

Общие сведения о модели управления доступом в Windows см. в разделе [Управление доступом](/windows/win32/SecAuthZ/access-control) в Windows SDK.

## <a name="requirements"></a>Требования

**Заголовок:** атлсекурити. h

## <a name="ctokenprivilegesadd"></a><a name="add"></a> Ктокенпривилежес:: Add

Добавляет один или несколько привилегий к `CTokenPrivileges` объекту маркера доступа.

```
bool Add(LPCTSTR pszPrivilege, bool bEnable) throw(...);
void Add(const TOKEN_PRIVILEGES& rPrivileges) throw(...);
```

### <a name="parameters"></a>Параметры

*псзпривилеже*<br/>
Указатель на строку, завершающуюся нулем, которая указывает имя привилегии, как определено в WINNT. Файл заголовка H.

*bEnable*<br/>
Если задано значение true, привилегия включена. Если задано значение false, привилегия отключена.

*рпривилежес*<br/>
Ссылка на структуру [TOKEN_PRIVILEGES](/windows/win32/api/winnt/ns-winnt-token_privileges) . Права и атрибуты копируются из этой структуры и добавляются в `CTokenPrivileges` объект.

### <a name="return-value"></a>Возвращаемое значение

Первая форма этого метода возвращает значение true, если привилегии успешно добавлены, и false в противном случае.

## <a name="ctokenprivilegesctokenprivileges"></a><a name="ctokenprivileges"></a> Ктокенпривилежес:: Ктокенпривилежес

Конструктор.

```
CTokenPrivileges() throw();
CTokenPrivileges(const CTokenPrivileges& rhs) throw(... );
CTokenPrivileges(const TOKEN_PRIVILEGES& rPrivileges) throw(...);
```

### <a name="parameters"></a>Параметры

*rhs*<br/>
`CTokenPrivileges`Объект, присваиваемый новому объекту.

*рпривилежес*<br/>
Структура [TOKEN_PRIVILEGES](/windows/win32/api/winnt/ns-winnt-token_privileges) , которую нужно назначить новому `CTokenPrivileges` объекту.

### <a name="remarks"></a>Комментарии

`CTokenPrivileges`При необходимости объект можно создать с помощью `TOKEN_PRIVILEGES` структуры или ранее определенного `CTokenPrivileges` объекта.

## <a name="ctokenprivilegesctokenprivileges"></a><a name="dtor"></a> Ктокенпривилежес:: ~ Ктокенпривилежес

Деструктор

```
virtual ~CTokenPrivileges() throw();
```

### <a name="remarks"></a>Комментарии

Деструктор освобождает все выделенные ресурсы.

## <a name="ctokenprivilegesdelete"></a><a name="delete"></a> Ктокенпривилежес::D удалить

Удаляет привилегии из `CTokenPrivileges` объекта маркера доступа.

```
bool Delete(LPCTSTR pszPrivilege) throw();
```

### <a name="parameters"></a>Параметры

*псзпривилеже*<br/>
Указатель на строку, завершающуюся нулем, которая указывает имя привилегии, как определено в WINNT. Файл заголовка H. Например, этот параметр может указать константу SE_SECURITY_NAME или соответствующую строку "SeSecurityPrivilege."

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если привилегия успешно удалена; в противном случае — значение false.

### <a name="remarks"></a>Комментарии

Этот метод полезен в качестве средства для создания ограниченных маркеров.

## <a name="ctokenprivilegesdeleteall"></a><a name="deleteall"></a> Ктокенпривилежес::D Елетеалл

Удаляет все привилегии из `CTokenPrivileges` объекта маркера доступа.

```cpp
void DeleteAll() throw();
```

### <a name="remarks"></a>Комментарии

Удаляет все привилегии, содержащиеся в `CTokenPrivileges` объекте маркера доступа.

## <a name="ctokenprivilegesgetdisplaynames"></a><a name="getdisplaynames"></a> Ктокенпривилежес:: DisplayName

Извлекает отображаемые имена для привилегий, содержащихся в `CTokenPrivileges` объекте маркера доступа.

```cpp
void GetDisplayNames(CNames* pDisplayNames) const throw(...);
```

### <a name="parameters"></a>Параметры

*пдисплайнамес*<br/>
Указатель на массив объектов `CString`. `CNames` определяется как typedef: `CTokenPrivileges::CAtlArray<CString>` .

### <a name="remarks"></a>Комментарии

Параметр `pDisplayNames` является указателем на массив `CString` объектов, которые будут принимать отображаемые имена, соответствующие привилегиям, содержащимся в `CTokenPrivileges` объекте. Этот метод извлекает отображаемые имена только для привилегий, указанных в разделе "определенные привилегии" файла WINNT. H.

Этот метод получает отображаемое имя: например, если имя атрибута — SE_REMOTE_SHUTDOWN_NAME, воспроизводимое имя — "принудительное завершение работы от удаленной системы". Чтобы получить имя системы, используйте [ктокенпривилежес:: жетнамесандаттрибутес](#getnamesandattributes).

## <a name="ctokenprivilegesgetcount"></a><a name="getcount"></a> Ктокенпривилежес:: NOCOUNT

Возвращает число записей привилегий в `CTokenPrivileges` объекте.

```
UINT GetCount() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает количество привилегий, содержащихся в `CTokenPrivileges` объекте.

## <a name="ctokenprivilegesgetlength"></a><a name="getlength"></a> Ктокенпривилежес:: DATALENGTH

Возвращает длину `CTokenPrivileges` объекта.

```
UINT GetLength() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает число байтов, необходимое для хранения `TOKEN_PRIVILEGES` структуры, представленной `CTokenPrivileges` объектом, включая все записи прав доступа, которые он содержит.

## <a name="ctokenprivilegesgetluidsandattributes"></a><a name="getluidsandattributes"></a> Ктокенпривилежес:: Жетлуидсандаттрибутес

Извлекает локально уникальные идентификаторы (LUID) и флаги атрибутов из `CTokenPrivileges` объекта.

```cpp
void GetLuidsAndAttributes(
    CLUIDArray* pPrivileges,
    CAttributes* pAttributes = NULL) const throw(...);
```

### <a name="parameters"></a>Параметры

*ппривилежес*<br/>
Указатель на массив объектов [LUID](/windows/win32/api/winnt/ns-winnt-luid) . `CLUIDArray` — Это определение типа, определенное как `CAtlArray<LUID> CLUIDArray` .

*паттрибутес*<br/>
Указатель на массив объектов типа DWORD. Если этот параметр опущен или имеет значение NULL, атрибуты не извлекаются. `CAttributes` — Это определение типа, определенное как `CAtlArray <DWORD> CAttributes` .

### <a name="remarks"></a>Комментарии

Этот метод выполняет перечисление всех привилегий, содержащихся в `CTokenPrivileges` объекте маркера доступа, и помещает отдельные LUID и (необязательно) флаги атрибута в объекты Array.

## <a name="ctokenprivilegesgetnamesandattributes"></a><a name="getnamesandattributes"></a> Ктокенпривилежес:: Жетнамесандаттрибутес

Извлекает флаги имени и атрибута из `CTokenPrivileges` объекта.

```cpp
void GetNamesAndAttributes(
    CNames* pNames,
    CAttributes* pAttributes = NULL) const throw(...);
```

### <a name="parameters"></a>Параметры

*пнамес*<br/>
Указатель на массив `CString` объектов. `CNames` — Это определение типа, определенное как `CAtlArray <CString> CNames` .

*паттрибутес*<br/>
Указатель на массив объектов типа DWORD. Если этот параметр опущен или имеет значение NULL, атрибуты не извлекаются. `CAttributes` — Это определение типа, определенное как `CAtlArray <DWORD> CAttributes` .

### <a name="remarks"></a>Комментарии

Этот метод выполняет перечисление всех привилегий, содержащихся в `CTokenPrivileges` объекте, помещая имя и (необязательно) флаги атрибута в объекты Array.

Этот метод получает имя атрибута, а не отображаемое имя: например, если имя атрибута — SE_REMOTE_SHUTDOWN_NAME, системным именем является "Серемотешутдовнпривилеже". Чтобы получить отображаемое имя, используйте метод [ктокенпривилежес::](#getdisplaynames)lt.

## <a name="ctokenprivilegesgetptoken_privileges"></a><a name="getptoken_privileges"></a> Ктокенпривилежес:: GetPTOKEN_PRIVILEGES

Возвращает указатель на `TOKEN_PRIVILEGES` структуру.

```
const TOKEN_PRIVILEGES* GetPTOKEN_PRIVILEGES() const throw(...);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на структуру [TOKEN_PRIVILEGES](/windows/win32/api/winnt/ns-winnt-token_privileges) .

## <a name="ctokenprivilegeslookupprivilege"></a><a name="lookupprivilege"></a> Ктокенпривилежес:: Лукуппривилеже

Извлекает атрибут, связанный с заданным именем привилегии.

```
bool LookupPrivilege(
    LPCTSTR pszPrivilege,
    DWORD* pdwAttributes = NULL) const throw(...);
```

### <a name="parameters"></a>Параметры

*псзпривилеже*<br/>
Указатель на строку, завершающуюся нулем, которая указывает имя привилегии, как определено в WINNT. Файл заголовка H. Например, этот параметр может указать константу SE_SECURITY_NAME или соответствующую строку "SeSecurityPrivilege."

*пдваттрибутес*<br/>
Указатель на переменную, которая получает атрибуты.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если атрибут успешно получен, и false в противном случае.

## <a name="ctokenprivilegesoperator-"></a><a name="operator_eq"></a> Ктокенпривилежес:: operator =

Оператор присвоения.

```
CTokenPrivileges& operator= (const TOKEN_PRIVILEGES& rPrivileges) throw(...);
CTokenPrivileges& operator= (const CTokenPrivileges& rhs) throw(...);
```

### <a name="parameters"></a>Параметры

*рпривилежес*<br/>
Структура [TOKEN_PRIVILEGES](/windows/win32/api/winnt/ns-winnt-token_privileges) , которую необходимо назначить `CTokenPrivileges` объекту.

*rhs*<br/>
`CTokenPrivileges`Объект, присваиваемый объекту.

### <a name="return-value"></a>Возвращаемое значение

Возвращает обновленный `CTokenPrivileges` объект.

## <a name="ctokenprivilegesoperator-const-token_privileges-"></a><a name="operator_const_token_privileges__star"></a> TOKEN_PRIVILEGES Ктокенпривилежес:: operator const \*

Приводит значение к указателю на `TOKEN_PRIVILEGES` структуру.

```
operator const TOKEN_PRIVILEGES *() const throw(...);
```

### <a name="remarks"></a>Комментарии

Приводит значение к указателю на структуру [TOKEN_PRIVILEGES](/windows/win32/api/winnt/ns-winnt-token_privileges) .

## <a name="see-also"></a>См. также раздел

[Пример безопасности](../../overview/visual-cpp-samples.md)<br/>
[TOKEN_PRIVILEGES](/windows/win32/api/winnt/ns-winnt-token_privileges)<br/>
[LUID](/windows/win32/api/winnt/ns-winnt-luid)<br/>
[LUID_AND_ATTRIBUTES](/windows/win32/api/winnt/ns-winnt-luid_and_attributes)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Глобальные функции безопасности](../../atl/reference/security-global-functions.md)
