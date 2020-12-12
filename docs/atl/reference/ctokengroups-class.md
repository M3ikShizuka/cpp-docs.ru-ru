---
description: 'Дополнительные сведения о: Ктокенграупс Class'
title: Класс Ктокенграупс
ms.date: 11/04/2016
f1_keywords:
- CTokenGroups
- ATLSECURITY/ATL::CTokenGroups
- ATLSECURITY/ATL::CTokenGroups::CTokenGroups
- ATLSECURITY/ATL::CTokenGroups::Add
- ATLSECURITY/ATL::CTokenGroups::Delete
- ATLSECURITY/ATL::CTokenGroups::DeleteAll
- ATLSECURITY/ATL::CTokenGroups::GetCount
- ATLSECURITY/ATL::CTokenGroups::GetLength
- ATLSECURITY/ATL::CTokenGroups::GetPTOKEN_GROUPS
- ATLSECURITY/ATL::CTokenGroups::GetSidsAndAttributes
- ATLSECURITY/ATL::CTokenGroups::LookupSid
helpviewer_keywords:
- CTokenGroups class
ms.assetid: 2ab08076-4b08-4487-bc70-ec6dee304190
ms.openlocfilehash: 3d6633afbd649aa175196f1fae8e62afdf784f99
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140352"
---
# <a name="ctokengroups-class"></a>Класс Ктокенграупс

Этот класс является оболочкой для `TOKEN_GROUPS` структуры.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class CTokenGroups
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ктокенграупс:: Ктокенграупс](#ctokengroups)|Конструктор.|
|[Ктокенграупс:: ~ Ктокенграупс](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ктокенграупс:: Add](#add)|Добавляет `CSid` или существующую `TOKEN_GROUPS` структуру в `CTokenGroups` объект.|
|[Ктокенграупс::D удалить](#delete)|Удаляет объект `CSid` и связанные с ним атрибуты из `CTokenGroups` объекта.|
|[Ктокенграупс::D Елетеалл](#deleteall)|Удаляет все `CSid` объекты и связанные с ними атрибуты из `CTokenGroups` объекта.|
|[Ктокенграупс:: NOCOUNT](#getcount)|Возвращает количество `CSid` объектов и связанных атрибутов, содержащихся в `CTokenGroups` объекте.|
|[Ктокенграупс:: DATALENGTH](#getlength)|Возвращает размер `CTokenGroups` объекта.|
|[Ктокенграупс:: GetPTOKEN_GROUPS](#getptoken_groups)|Извлекает указатель на `TOKEN_GROUPS` структуру.|
|[Ктокенграупс:: Жетсидсандаттрибутес](#getsidsandattributes)|Извлекает `CSid` объекты и атрибуты, принадлежащие `CTokenGroups` объекту.|
|[Ктокенграупс:: Лукупсид](#lookupsid)|Извлекает атрибуты, связанные с `CSid` объектом.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Ктокенграупс:: operator const TOKEN_GROUPS *](#operator_const_token_groups__star)|Приводит `CTokenGroups` объект к указателю на `TOKEN_GROUPS` структуру.|
|[Ктокенграупс:: operator =](#operator_eq)|Оператор присвоения.|

## <a name="remarks"></a>Комментарии

[Маркер доступа](/windows/win32/SecAuthZ/access-tokens) — это объект, который описывает контекст безопасности процесса или потока и выделяется каждому пользователю, вошедшему в систему Windows.

`CTokenGroups`Класс является оболочкой для структуры [TOKEN_GROUPS](/windows/win32/api/winnt/ns-winnt-token_groups) , содержащей сведения об идентификаторах безопасности групп (SID) в маркере доступа.

Общие сведения о модели управления доступом в Windows см. в разделе [Управление доступом](/windows/win32/SecAuthZ/access-control) в Windows SDK.

## <a name="requirements"></a>Требования

**Заголовок:** атлсекурити. h

## <a name="ctokengroupsadd"></a><a name="add"></a> Ктокенграупс:: Add

Добавляет `CSid` или существующую `TOKEN_GROUPS` структуру в `CTokenGroups` объект.

```cpp
void Add(const CSid& rSid, DWORD dwAttributes) throw(... );
void Add(const TOKEN_GROUPS& rTokenGroups) throw(...);
```

### <a name="parameters"></a>Параметры

*рсид*<br/>
Объект [CSid](../../atl/reference/csid-class.md) .

*дваттрибутес*<br/>
Атрибуты, связываемые с `CSid` объектом.

*ртокенграупс*<br/>
Структура [TOKEN_GROUPS](/windows/win32/api/winnt/ns-winnt-token_groups) .

### <a name="remarks"></a>Комментарии

Эти методы добавляют в объект один или несколько `CSid` объектов и связанных с ними атрибутов `CTokenGroups` .

## <a name="ctokengroupsctokengroups"></a><a name="ctokengroups"></a> Ктокенграупс:: Ктокенграупс

Конструктор.

```
CTokenGroups() throw();
CTokenGroups(const CTokenGroups& rhs) throw(... );
CTokenGroups(const TOKEN_GROUPS& rhs) throw(...);
```

### <a name="parameters"></a>Параметры

*rhs*<br/>
`CTokenGroups`Объект или структура [TOKEN_GROUPS](/windows/win32/api/winnt/ns-winnt-token_groups) , с которой создается `CTokenGroups` объект.

### <a name="remarks"></a>Комментарии

`CTokenGroups`При необходимости объект можно создать с помощью `TOKEN_GROUPS` структуры или ранее определенного `CTokenGroups` объекта.

## <a name="ctokengroupsctokengroups"></a><a name="dtor"></a> Ктокенграупс:: ~ Ктокенграупс

Деструктор

```
virtual ~CTokenGroups() throw();
```

### <a name="remarks"></a>Комментарии

Деструктор освобождает все выделенные ресурсы.

## <a name="ctokengroupsdelete"></a><a name="delete"></a> Ктокенграупс::D удалить

Удаляет объект `CSid` и связанные с ним атрибуты из `CTokenGroups` объекта.

```
bool Delete(const CSid& rSid) throw();
```

### <a name="parameters"></a>Параметры

*рсид*<br/>
Объект [CSid](../../atl/reference/csid-class.md) , для которого необходимо удалить идентификатор безопасности (SID) и атрибуты.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если объект `CSid` удален, и false в противном случае.

## <a name="ctokengroupsdeleteall"></a><a name="deleteall"></a> Ктокенграупс::D Елетеалл

Удаляет все `CSid` объекты и связанные с ними атрибуты из `CTokenGroups` объекта.

```cpp
void DeleteAll() throw();
```

## <a name="ctokengroupsgetcount"></a><a name="getcount"></a> Ктокенграупс:: NOCOUNT

Возвращает количество `CSid` объектов, содержащихся в `CTokenGroups` .

```
UINT GetCount() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает число объектов [CSid](../../atl/reference/csid-class.md) и связанных с ними атрибутов, содержащихся в `CTokenGroups` объекте.

## <a name="ctokengroupsgetlength"></a><a name="getlength"></a> Ктокенграупс:: DATALENGTH

Возвращает размер `CTokenGroup` объекта.

```
UINT GetLength() const throw();
```

### <a name="remarks"></a>Комментарии

Возвращает общий размер `CTokenGroup` объекта в байтах.

## <a name="ctokengroupsgetptoken_groups"></a><a name="getptoken_groups"></a> Ктокенграупс:: GetPTOKEN_GROUPS

Извлекает указатель на `TOKEN_GROUPS` структуру.

```
const TOKEN_GROUPS* GetPTOKEN_GROUPS() const throw(...);
```

### <a name="return-value"></a>Возвращаемое значение

Получает указатель на структуру [TOKEN_GROUPS](/windows/win32/api/winnt/ns-winnt-token_groups) , принадлежащую `CTokenGroups` объекту маркера доступа.

## <a name="ctokengroupsgetsidsandattributes"></a><a name="getsidsandattributes"></a> Ктокенграупс:: Жетсидсандаттрибутес

Извлекает `CSid` объекты и (необязательно) атрибуты, принадлежащие `CTokenGroups` объекту.

```cpp
void GetSidsAndAttributes(
    CSid::CSidArray* pSids,
    CAtlArray<DWORD>* pAttributes = NULL) const throw(...);
```

### <a name="parameters"></a>Параметры

*псидс*<br/>
Указатель на массив объектов [CSid](../../atl/reference/csid-class.md) .

*паттрибутес*<br/>
Указатель на массив DWORD. Если этот параметр опущен или имеет значение NULL, атрибуты не извлекаются.

### <a name="remarks"></a>Комментарии

Этот метод выполняет перечисление всех `CSid` объектов, содержащихся в `CTokenGroups` объекте, и помещает их и (необязательно) флаги атрибута в объекты Array.

## <a name="ctokengroupslookupsid"></a><a name="lookupsid"></a> Ктокенграупс:: Лукупсид

Извлекает атрибуты, связанные с `CSid` объектом.

```
bool LookupSid(
    const CSid& rSid,
    DWORD* pdwAttributes = NULL) const throw();
```

### <a name="parameters"></a>Параметры

*рсид*<br/>
Объект [CSid](../../atl/reference/csid-class.md) .

*пдваттрибутес*<br/>
Указатель на DWORD, который будет принимать `CSid` атрибут объекта. Если значение не указано или равно NULL, атрибут не будет получен.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение true, если объект `CSid` найден, и false в противном случае.

### <a name="remarks"></a>Комментарии

Установка *пдваттрибутес* в значение NULL позволяет подтвердить существование объекта `CSid` без доступа к атрибуту. Обратите внимание, что этот метод не следует использовать для проверки прав доступа. Вместо этого в приложениях следует использовать метод [CAccessToken:: чекктокенмембершип](../../atl/reference/caccesstoken-class.md#checktokenmembership) .

## <a name="ctokengroupsoperator-"></a><a name="operator_eq"></a> Ктокенграупс:: operator =

Оператор присвоения.

```
CTokenGroups& operator= (const TOKEN_GROUPS& rhs) throw(...);
CTokenGroups& operator= (const CTokenGroups& rhs) throw(...);
```

### <a name="parameters"></a>Параметры

*rhs*<br/>
`CTokenGroups`Объект или структура [TOKEN_GROUPS](/windows/win32/api/winnt/ns-winnt-token_groups) , которую необходимо назначить `CTokenGroups` объекту.

### <a name="return-value"></a>Возвращаемое значение

Возвращает обновленный `CTokenGroups` объект.

## <a name="ctokengroupsoperator-const-token_groups-"></a><a name="operator_const_token_groups__star"></a> Ктокенграупс:: operator const TOKEN_GROUPS *

Приводит значение к указателю на `TOKEN_GROUPS` структуру.

```
operator const TOKEN_GROUPS *() const throw(...);
```

### <a name="remarks"></a>Комментарии

Приводит значение к указателю на структуру [TOKEN_GROUPS](/windows/win32/api/winnt/ns-winnt-token_groups) .

## <a name="see-also"></a>См. также раздел

[Пример безопасности](../../overview/visual-cpp-samples.md)<br/>
[CSid, класс](../../atl/reference/csid-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Глобальные функции безопасности](../../atl/reference/security-global-functions.md)
