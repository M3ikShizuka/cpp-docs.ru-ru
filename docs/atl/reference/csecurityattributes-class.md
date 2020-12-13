---
description: 'Дополнительные сведения о: Ксекуритяттрибутес Class'
title: Класс Ксекуритяттрибутес
ms.date: 11/04/2016
f1_keywords:
- CSecurityAttributes
- ATLSECURITY/ATL::CSecurityAttributes
- ATLSECURITY/ATL::CSecurityAttributes::CSecurityAttributes
- ATLSECURITY/ATL::CSecurityAttributes::Set
helpviewer_keywords:
- CSecurityAttributes class
ms.assetid: a094880c-52e1-4a28-97ff-752d5869908e
ms.openlocfilehash: 8cb772e574aef4ad941feef1cb838fb91d937576
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140820"
---
# <a name="csecurityattributes-class"></a>Класс Ксекуритяттрибутес

Этот класс является тонкой оболочкой для структуры атрибутов безопасности.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class CSecurityAttributes : public SECURITY_ATTRIBUTES
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ксекуритяттрибутес:: Ксекуритяттрибутес](#csecurityattributes)|Конструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксекуритяттрибутес:: Set](#set)|Вызовите этот метод, чтобы задать атрибуты `CSecurityAttributes` объекта.|

## <a name="remarks"></a>Комментарии

`SECURITY_ATTRIBUTES`Структура содержит [дескриптор безопасности](/windows/win32/api/winnt/ns-winnt-security_descriptor) , используемый для создания объекта, и указывает, наследуется ли полученный дескриптор путем указания этой структуры.

Общие сведения о модели управления доступом в Windows см. в разделе [Управление доступом](/windows/win32/SecAuthZ/access-control) в Windows SDK.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`SECURITY_ATTRIBUTES`

`CSecurityAttributes`

## <a name="requirements"></a>Требования

**Заголовок:** атлсекурити. h

## <a name="csecurityattributescsecurityattributes"></a><a name="csecurityattributes"></a> Ксекуритяттрибутес:: Ксекуритяттрибутес

Конструктор.

```
CSecurityAttributes() throw();
explicit CSecurityAttributes(const CSecurityDesc& rSecurityDescriptor, bool bInheritsHandle = false) throw(...);
```

### <a name="parameters"></a>Параметры

*рсекуритидескриптор*<br/>
Ссылка на дескриптор безопасности.

*бинхеритшандле*<br/>
Определяет, наследуется ли возвращаемый дескриптор при создании процесса. Если этот элемент имеет значение true, новый процесс наследует дескриптор.

## <a name="csecurityattributesset"></a><a name="set"></a> Ксекуритяттрибутес:: Set

Вызовите этот метод, чтобы задать атрибуты `CSecurityAttributes` объекта.

```cpp
void Set(const CSecurityDesc& rSecurityDescriptor, bool bInheritHandle = false) throw(...);
```

### <a name="parameters"></a>Параметры

*рсекуритидескриптор*<br/>
Ссылка на дескриптор безопасности.

*бинхерисандле*<br/>
Определяет, наследуется ли возвращаемый дескриптор при создании процесса. Если этот элемент имеет значение true, новый процесс наследует дескриптор.

### <a name="remarks"></a>Комментарии

Этот метод используется конструктором для инициализации `CSecurityAttributes` объекта.

## <a name="see-also"></a>См. также раздел

[Пример безопасности](../../overview/visual-cpp-samples.md)<br/>
[SECURITY_ATTRIBUTES](/previous-versions/windows/desktop/legacy/aa379560\(v=vs.85\))<br/>
[Дескриптор безопасности](/windows/win32/api/winnt/ns-winnt-security_descriptor)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Глобальные функции безопасности](../../atl/reference/security-global-functions.md)
