---
description: 'Дополнительные сведения о: Иобжектсафетимпл Class'
title: Класс Иобжектсафетимпл
ms.date: 11/04/2016
f1_keywords:
- IObjectSafetyImpl
- ATLCTL/ATL::IObjectSafetyImpl
- ATLCTL/ATL::IObjectSafetyImpl::GetInterfaceSafetyOptions
- ATLCTL/ATL::IObjectSafetyImpl::SetInterfaceSafetyOptions
- ATLCTL/ATL::IObjectSafetyImpl::m_dwCurrentSafety
helpviewer_keywords:
- controls [ATL], safe
- safe for scripting and initialization (controls)
- IObjectSafety, ATL implementation
- IObjectSafetyImpl class
ms.assetid: 64e32082-d910-4a8a-a5bf-ebed9145359d
ms.openlocfilehash: ac19fe24d12d7d09968b3e2d76f77741e83e1f81
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139468"
---
# <a name="iobjectsafetyimpl-class"></a>Класс Иобжектсафетимпл

Этот класс предоставляет реализацию интерфейса по умолчанию, позволяющую `IObjectSafety` клиенту получать и устанавливать уровни безопасности объекта.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template <class T,DWORD dwSupportedSafety>
class IObjectSafetyImpl
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IObjectSafetyImpl` .

*двсуппортедсафети*<br/>
Задает поддерживаемые параметры безопасности для элемента управления. Может иметь одно из следующих значений:

- INTERFACESAFE_FOR_UNTRUSTED_CALLER интерфейс, определяемый параметром [сетинтерфацесафетйоптионс](#setinterfacesafetyoptions) , `riid` должен быть защищен для создания скриптов.

- INTERFACESAFE_FOR_UNTRUSTED_DATA интерфейс, определяемый `SetInterfaceSafetyOptions` параметром, `riid` должен быть защищен для ненадежных данных во время инициализации.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Иобжектсафетимпл:: Жетинтерфацесафетйоптионс](#getinterfacesafetyoptions)|Извлекает параметры безопасности, поддерживаемые объектом, а также параметры безопасности, установленные для объекта.|
|[Иобжектсафетимпл:: Сетинтерфацесафетйоптионс](#setinterfacesafetyoptions)|Делает объект надежным для инициализации или создания скриптов.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Иобжектсафетимпл:: m_dwCurrentSafety](#m_dwcurrentsafety)|Сохраняет текущий уровень безопасности объекта.|

## <a name="remarks"></a>Комментарии

Класс `IObjectSafetyImpl` предоставляет реализацию по умолчанию `IObjectSafety` . `IObjectSafety`Интерфейс позволяет клиенту извлекать и устанавливать уровни безопасности объекта. Например, веб-браузер может вызвать `IObjectSafety::SetInterfaceSafetyOptions` , чтобы сделать элемент управления надежным для инициализации или обеспечения безопасности при написании сценариев.

Обратите внимание, что использование макроса [IMPLEMENTED_CATEGORY](category-macros.md#implemented_category) с категориями компонентов CATID_SafeForScripting и CATID_SafeForInitializing предоставляет альтернативный способ указания того, что компонент является надежным.

Руководство по **сопутствующим статьям** [ATL](../../atl/active-template-library-atl-tutorial.md), [Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IObjectSafety`

`IObjectSafetyImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлктл. h

## <a name="iobjectsafetyimplgetinterfacesafetyoptions"></a><a name="getinterfacesafetyoptions"></a> Иобжектсафетимпл:: Жетинтерфацесафетйоптионс

Извлекает параметры безопасности, поддерживаемые объектом, а также параметры безопасности, установленные для объекта.

```
HRESULT GetInterfaceSafetyOptions(
    REFIID riid,
    DWORD* pdwSupportedOptions,
    DWORD* pdwEnabledOptions);
```

### <a name="remarks"></a>Комментарии

Реализация возвращает соответствующие значения для любого интерфейса, поддерживаемого реализацией объекта `IUnknown::QueryInterface` .

> [!IMPORTANT]
> Любой объект, который поддерживает, `IObjectSafety` отвечает за собственную безопасность, а также на все объекты, которые он делегирует. Программист должен учитывать проблемы, возникающие из-за выполнения кода в контексте пользователя, межсайтовые сценарии и выполнять подходящую проверку зоны.

См. раздел [иобжектсафети:: жетинтерфацесафетйоптионс](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768223\(v=vs.85\)) в Windows SDK.

## <a name="iobjectsafetyimplm_dwcurrentsafety"></a><a name="m_dwcurrentsafety"></a> Иобжектсафетимпл:: m_dwCurrentSafety

Сохраняет текущий уровень безопасности объекта.

```
DWORD m_dwCurrentSafety;
```

## <a name="iobjectsafetyimplsetinterfacesafetyoptions"></a><a name="setinterfacesafetyoptions"></a> Иобжектсафетимпл:: Сетинтерфацесафетйоптионс

Делает объект надежным для инициализации или создания скриптов, устанавливая для элемента [m_dwCurrentSafety](#m_dwcurrentsafety) соответствующее значение.

```
HRESULT SetInterfaceSafetyOptions(
    REFIID riid,
    DWORD dwOptionsSetMask,
    DWORD dwEnabledOptions);
```

### <a name="remarks"></a>Комментарии

Реализация возвращает E_NOINTERFACE для любого интерфейса, не поддерживаемого реализацией объекта `IUnknown::QueryInterface` .

> [!IMPORTANT]
> Любой объект, который поддерживает, `IObjectSafety` отвечает за собственную безопасность, а также на все объекты, которые он делегирует. Программист должен учитывать проблемы, возникающие из-за выполнения кода в контексте пользователя, межсайтовые сценарии и выполнять подходящую проверку зоны.

См. раздел [иобжектсафети:: сетинтерфацесафетйоптионс](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225\(v=vs.85\)) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Интерфейс Иобжектсафети](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768224\(v=vs.85\))<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
