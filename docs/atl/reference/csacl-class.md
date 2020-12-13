---
description: 'Дополнительные сведения о: Ксакл Class'
title: Класс Ксакл
ms.date: 11/04/2016
f1_keywords:
- CSacl
- ATLSECURITY/ATL::CSacl
- ATLSECURITY/ATL::CSacl::CSacl
- ATLSECURITY/ATL::CSacl::AddAuditAce
- ATLSECURITY/ATL::CSacl::GetAceCount
- ATLSECURITY/ATL::CSacl::RemoveAce
- ATLSECURITY/ATL::CSacl::RemoveAllAces
helpviewer_keywords:
- CSacl class
ms.assetid: 8624889b-aebc-4183-9d29-a20f07837f05
ms.openlocfilehash: 504276d22da963b9e8ec407e88ca73d63dd71541
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140859"
---
# <a name="csacl-class"></a>Класс Ксакл

Этот класс является оболочкой для структуры SACL (системный доступ к списку управления).

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class CSacl : public CAcl
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ксакл:: Ксакл](#csacl)|Конструктор.|
|[Ксакл:: ~ Ксакл](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксакл:: Аддаудитаце](#addauditace)|Добавляет запись управления доступом (ACE) аудита в `CSacl` объект.|
|[Ксакл:: Жетацекаунт](#getacecount)|Возвращает число записей управления доступом (ACE) в `CSacl` объекте.|
|[Ксакл:: Ремовеаце](#removeace)|Удаляет конкретный элемент ACE (запись управления доступом) из `CSacl` объекта.|
|[Ксакл:: Ремовеаллацес](#removeallaces)|Удаляет все элементы ACE, содержащиеся в `CSacl` объекте.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Ксакл:: operator =](#operator_eq)|Оператор присвоения.|

## <a name="remarks"></a>Комментарии

Список SACL содержит записи управления доступом (ACE), которые указывают типы попыток доступа, которые создают записи аудита в журнале событий безопасности контроллера домена. Обратите внимание, что список SACL создает записи журнала только на контроллере домена, где произошла попыток доступа, а не на каждом контроллере домена, содержащем реплику объекта.

Чтобы задать или получить список SACL в дескрипторе безопасности объекта, необходимо включить SE_SECURITY_NAME права в маркере доступа запрашивающего потока. Эта привилегия предоставляется группе "Администраторы" по умолчанию и может быть предоставлена другим пользователям или группам. Предоставление предоставленной привилегии не является обязательным: перед выполнением операции, определяемой привилегией, необходимо включить ее в маркере доступа безопасности, чтобы она вступила в силу. Модель позволяет включать привилегии только для конкретных операций системы, а затем отключена, когда они больше не нужны. Примеры включения SE_SECURITY_NAME см. в разделе [атлжетсакл](security-global-functions.md#atlgetsacl) и [атлсетсакл](security-global-functions.md#atlsetsacl) .

Используйте методы класса, предоставляемые для добавления, удаления, создания и удаления записей ACE из `SACL` объекта. См. также [атлжетсакл](security-global-functions.md#atlgetsacl) и [атлсетсакл](security-global-functions.md#atlsetsacl).

Общие сведения о модели управления доступом в Windows см. в разделе [Управление доступом](/windows/win32/SecAuthZ/access-control) в Windows SDK.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[какл](../../atl/reference/cacl-class.md)

`CSacl`

## <a name="requirements"></a>Требования

**Заголовок:** атлсекурити. h

## <a name="csacladdauditace"></a><a name="addauditace"></a> Ксакл:: Аддаудитаце

Добавляет запись управления доступом (ACE) аудита в `CSacl` объект.

```
bool AddAuditAce(
    const CSid& rSid,
    ACCESS_MASK AccessMask,
    bool bSuccess,
    bool bFailure,
    BYTE AceFlags = 0) throw(...);

bool AddAuditAce(
    const CSid& rSid,
    ACCESS_MASK AccessMask,
    bool bSuccess,
    bool bFailure,
    BYTE AceFlags,
    const GUID* pObjectType,
    const GUID* pInheritedObjectType) throw(...);
```

### <a name="parameters"></a>Параметры

*рсид*<br/>
Объект [CSid](../../atl/reference/csid-class.md) .

*AccessMask*<br/>
Указывает маску прав доступа для аудита для указанного `CSid` объекта.

*бсукцесс*<br/>
Указывает, разрешены ли аудит попыток доступа. Установите для этого флага значение true, чтобы включить аудит. в противном случае задайте для него значение false.

*бфаилуре*<br/>
Указывает, следует ли выполнять аудит попыток отказа в доступе. Установите для этого флага значение true, чтобы включить аудит. в противном случае задайте для него значение false.

*AceFlags*<br/>
Набор битовых флагов, управляющих наследованием ACE.

*побжекттипе*<br/>
Тип объекта.

*пинхеритедобжекттипе*<br/>
Тип наследуемого объекта.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если ACE добавляется к `CSacl` объекту, и false при сбое.

### <a name="remarks"></a>Комментарии

`CSacl`Объект содержит записи управления доступом (ACE), которые указывают типы попыток доступа, которые создают записи аудита в журнале событий безопасности. Этот метод добавляет такой элемент управления доступом к `CSacl` объекту.

Описание различных флагов, которые можно задать в параметре *AceFlags* , см. в разделе [ACE_HEADER](/windows/win32/api/winnt/ns-winnt-ace_header) .

## <a name="csaclcsacl"></a><a name="csacl"></a> Ксакл:: Ксакл

Конструктор.

```
CSacl() throw();
CSacl(const ACL& rhs) throw(...);
```

### <a name="parameters"></a>Параметры

*rhs*<br/>
Существующая `ACL` Структура (список управления доступом).

### <a name="remarks"></a>Комментарии

`CSacl`При необходимости можно создать объект с помощью существующей `ACL` структуры. Убедитесь, что этот параметр является системным списком управления доступом (SACL), а не списком управления доступом на уровне пользователей (DACL). В отладочных сборках, если указан список DACL, произойдет утверждение. В выпуске сборки все записи из списка DACL игнорируются.

## <a name="csaclcsacl"></a><a name="dtor"></a> Ксакл:: ~ Ксакл

Деструктор

```
~CSacl() throw();
```

### <a name="remarks"></a>Комментарии

Деструктор освобождает все ресурсы, полученные объектом, включая все записи управления доступом (ACE).

## <a name="csaclgetacecount"></a><a name="getacecount"></a> Ксакл:: Жетацекаунт

Возвращает число записей управления доступом (ACE) в `CSacl` объекте.

```
UINT GetAceCount() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает количество записей ACE, содержащихся в `CSacl` объекте.

## <a name="csacloperator-"></a><a name="operator_eq"></a> Ксакл:: operator =

Оператор присвоения.

```
CSacl& operator=(const ACL& rhs) throw(...);
```

### <a name="parameters"></a>Параметры

*rhs*<br/>
`ACL`Объект (список управления доступом) для назначения существующему объекту.

### <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку на обновленный `CSacl` объект. Убедитесь, что `ACL` параметр на самом деле является системным списком управления доступом (SACL), а не списком управления доступом (DACL). В отладочных сборках выполняется утверждение, и в выпуске сборки `ACL` параметр будет проигнорирован.

## <a name="csaclremoveace"></a><a name="removeace"></a> Ксакл:: Ремовеаце

Удаляет конкретный элемент ACE (запись управления доступом) из `CSacl` объекта.

```cpp
void RemoveAce(UINT nIndex) throw();
```

### <a name="parameters"></a>Параметры

*ниндекс*<br/>
Индекс удаляемой записи ACE.

### <a name="remarks"></a>Комментарии

Этот метод является производным от [CAtlArray:: RemoveAt](../../atl/reference/catlarray-class.md#removeat).

## <a name="csaclremoveallaces"></a><a name="removeallaces"></a> Ксакл:: Ремовеаллацес

Удаляет все записи управления доступом (ACE), содержащиеся в `CSacl` объекте.

```cpp
void RemoveAllAces() throw();
```

### <a name="remarks"></a>Комментарии

Удаляет все `ACE` структуры (если таковые имеются) в `CSacl` объекте.

## <a name="see-also"></a>См. также раздел

[Класс Какл](../../atl/reference/cacl-class.md)<br/>
[списки управления доступом;](/windows/win32/SecAuthZ/access-control-lists)<br/>
[Туз](/windows/win32/SecAuthZ/access-control-entries)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Глобальные функции безопасности](../../atl/reference/security-global-functions.md)
