---
description: 'Дополнительные сведения о: Катлмодулет Class'
title: Класс Катлмодулет
ms.date: 11/04/2016
f1_keywords:
- CAtlModuleT
- ATLBASE/ATL::CAtlModuleT
- ATLBASE/ATL::CAtlModuleT::CAtlModuleT
- ATLBASE/ATL::CAtlModuleT::InitLibId
- ATLBASE/ATL::CAtlModuleT::RegisterAppId
- ATLBASE/ATL::CAtlModuleT::RegisterServer
- ATLBASE/ATL::CAtlModuleT::UnregisterAppId
- ATLBASE/ATL::CAtlModuleT::UnregisterServer
- ATLBASE/ATL::CAtlModuleT::UpdateRegistryAppId
helpviewer_keywords:
- CAtlModuleT class
ms.assetid: 9b74d02f-9117-47b1-a05e-c5945f83dd2b
ms.openlocfilehash: 841d4a41b7df818d9e966af1050fd9e376d89447
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97147229"
---
# <a name="catlmodulet-class"></a>Класс Катлмодулет

Этот класс реализует модуль ATL.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
class ATL_NO_VTABLE CAtlModuleT : public CAtlModule
```

### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `CAtlModuleT` .

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Катлмодулет:: Катлмодулет](#catlmodulet)|Конструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Катлмодулет:: Инитлибид](#initlibid)|Инициализирует элемент данных, содержащий идентификатор GUID текущего модуля.|
|[Катлмодулет:: Регистераппид](#registerappid)|Добавляет EXE в реестр.|
|[Катлмодулет:: Регистерсервер](#registerserver)|Добавляет службу в реестр.|
|[Катлмодулет:: Унрегистераппид](#unregisterappid)|Удаляет исполняемый файл из реестра.|
|[Катлмодулет:: Унрегистерсервер](#unregisterserver)|Удаляет службу из реестра.|
|[Катлмодулет:: Упдатерегистряппид](#updateregistryappid)|Обновляет сведения о EXE в реестре.|

## <a name="remarks"></a>Комментарии

`CAtlModuleT`, производный от [катлмодуле](../../atl/reference/catlmodule-class.md), реализует исполняемый (exe) или сервисный (exe) модуль ATL. Исполняемый модуль — это локальный сервер вне процесса, в то время как модуль службы — это приложение Windows, которое запускается в фоновом режиме при запуске Windows.

`CAtlModuleT` обеспечивает поддержку инициализации, регистрации и отмены регистрации модуля.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[_ATL_MODULE](atl-typedefs.md#_atl_module)

[катлмодуле](../../atl/reference/catlmodule-class.md)

`CAtlModuleT`

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="catlmoduletcatlmodulet"></a><a name="catlmodulet"></a> Катлмодулет:: Катлмодулет

Конструктор.

```cpp
CAtlModuleT() throw();
```

### <a name="remarks"></a>Комментарии

Вызывает [катлмодулет:: инитлибид](#initlibid).

## <a name="catlmoduletinitlibid"></a><a name="initlibid"></a> Катлмодулет:: Инитлибид

Инициализирует элемент данных, содержащий идентификатор GUID текущего модуля.

```cpp
static void InitLibId() throw();
```

### <a name="remarks"></a>Комментарии

Вызывается конструктором [катлмодулет:: катлмодулет](#catlmodulet).

## <a name="catlmoduletregisterappid"></a><a name="registerappid"></a> Катлмодулет:: Регистераппид

Добавляет EXE в реестр.

```cpp
HRESULT RegisterAppId() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK при успешном выполнении или ошибку HRESULT при сбое.

## <a name="catlmoduletregisterserver"></a><a name="registerserver"></a> Катлмодулет:: Регистерсервер

Добавляет службу в реестр.

```cpp
HRESULT RegisterServer(
    BOOL bRegTypeLib = FALSE,
    const CLSID* pCLSID = NULL) throw();
```

### <a name="parameters"></a>Параметры

*брегтипелиб*<br/>
Значение TRUE, если библиотека типов должна быть зарегистрирована. Значение по умолчанию — FALSE.

*пклсид*<br/>
Указывает на идентификатор CLSID регистрируемого объекта. При значении NULL (значение по умолчанию) будут зарегистрированы все объекты в сопоставлении объектов.

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK при успешном выполнении или ошибку HRESULT при сбое.

## <a name="catlmoduletunregisterappid"></a><a name="unregisterappid"></a> Катлмодулет:: Унрегистераппид

Удаляет исполняемый файл из реестра.

```cpp
HRESULT UnregisterAppId() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK при успешном выполнении или ошибку HRESULT при сбое.

## <a name="catlmoduletunregisterserver"></a><a name="unregisterserver"></a> Катлмодулет:: Унрегистерсервер

Удаляет службу из реестра.

```cpp
HRESULT UnregisterServer(
    BOOL bUnRegTypeLib,
    const CLSID* pCLSID = NULL) throw();
```

### <a name="parameters"></a>Параметры

*бунрегтипелиб*<br/>
Значение TRUE, если для библиотеки типов также требуется отменить регистрацию.

*пклсид*<br/>
Указывает на CLSID объекта, регистрация которого будет отменена. Если NULL (значение по умолчанию), регистрация всех объектов в сопоставлении объектов будет отменена.

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK при успешном выполнении или ошибку HRESULT при сбое.

## <a name="catlmoduletupdateregistryappid"></a><a name="updateregistryappid"></a> Катлмодулет:: Упдатерегистряппид

Обновляет сведения о EXE в реестре.

```cpp
static HRESULT WINAPI UpdateRegistryAppId(BOOL /* bRegister*/) throw();
```

### <a name="parameters"></a>Параметры

*брегистер*<br/>
Зарезервировано.

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK при успешном выполнении или ошибку HRESULT при сбое.

## <a name="see-also"></a>См. также раздел

[Класс Катлмодуле](../../atl/reference/catlmodule-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Классы модулей](../../atl/atl-module-classes.md)
