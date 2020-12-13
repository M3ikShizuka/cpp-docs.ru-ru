---
description: 'Дополнительные сведения о: ISupportErrorInfoImpl Class'
title: Класс ISupportErrorInfoImpl
ms.date: 06/13/2019
f1_keywords:
- ISupportErrorInfoImpl
- ATLCOM/ATL::ISupportErrorInfoImpl
- ATLCOM/ATL::ISupportErrorInfoImpl::InterfaceSupportsErrorInfo
helpviewer_keywords:
- ISupportErrorInfo ATL implementation
- ISupportErrorInfoImpl class
- error information, ATL
ms.assetid: e33a4b11-a123-41cf-bcea-7b19743902af
ms.openlocfilehash: 182f55f7d7c288e4c8679c3e8cc1df7bb5cd79bd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139143"
---
# <a name="isupporterrorinfoimpl-class"></a>Класс ISupportErrorInfoImpl

Этот класс предоставляет реализацию [интерфейса ISupportErrorInfo](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) по умолчанию и может использоваться, когда только один интерфейс создает ошибки для объекта.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```cpp
template<const IID* piid>
class ATL_NO_VTABLE ISupportErrorInfoImpl
   : public ISupportErrorInfo
```

### <a name="parameters"></a>Параметры

*пиид*<br/>
Указатель на идентификатор IID интерфейса, который поддерживает [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo).

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[ISupportErrorInfoImpl:: Интерфацесуппортсерроринфо](#interfacesupportserrorinfo)|Указывает, поддерживает ли интерфейс, определенный с помощью, `riid` интерфейс [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .|

## <a name="remarks"></a>Комментарии

[Интерфейс ISupportErrorInfo](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) гарантирует, что сведения об ошибке могут быть возвращены клиенту. Объекты, использующие, `IErrorInfo` должны реализовывать `ISupportErrorInfo` .

Класс `ISupportErrorInfoImpl` предоставляет реализацию по умолчанию `ISupportErrorInfo` и может использоваться, когда только один интерфейс создает ошибки для объекта. Пример:

[!code-cpp[NVC_ATL_COM#48](../../atl/codesnippet/cpp/isupporterrorinfoimpl-class_1.h)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`ISupportErrorInfo`

`ISupportErrorInfoImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="isupporterrorinfoimplinterfacesupportserrorinfo"></a><a name="interfacesupportserrorinfo"></a> ISupportErrorInfoImpl:: Интерфацесуппортсерроринфо

Указывает, поддерживает ли интерфейс, определенный с помощью, `riid` интерфейс [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .

```cpp
STDMETHOD(InterfaceSupportsErrorInfo)(REFIID riid);
```

### <a name="remarks"></a>Комментарии

См. раздел [ISupportErrorInfo:: интерфацесуппортсерроринфо](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
