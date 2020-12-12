---
description: 'Дополнительные сведения о: Иконнектионпоинтконтаинеримпл Class'
title: Класс Иконнектионпоинтконтаинеримпл
ms.date: 11/04/2016
f1_keywords:
- IConnectionPointContainerImpl
- ATLCOM/ATL::IConnectionPointContainerImpl
- ATLCOM/ATL::IConnectionPointContainerImpl::EnumConnectionPoints
- ATLCOM/ATL::IConnectionPointContainerImpl::FindConnectionPoint
helpviewer_keywords:
- connectable objects
- connection points [C++], container
- IConnectionPointContainerImpl class
ms.assetid: 10db5a8d-8be9-4d9d-8a82-8ab9ffe3e9d6
ms.openlocfilehash: 77499954f65b5a447d2f5773c0b4c1dbdbfc5c22
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139598"
---
# <a name="iconnectionpointcontainerimpl-class"></a>Класс Иконнектионпоинтконтаинеримпл

Этот класс реализует контейнер точек соединения для управления коллекцией объектов [иконнектионпоинтимпл](../../atl/reference/iconnectionpointimpl-class.md) .

## <a name="syntax"></a>Синтаксис

```
template<class T>
class ATL_NO_VTABLE IConnectionPointContainerImpl
   : public IConnectionPointContainer
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IConnectionPointContainerImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Иконнектионпоинтконтаинеримпл:: Енумконнектионпоинтс](#enumconnectionpoints)|Создает перечислитель для прохода по точкам соединения, поддерживаемым в подключаемом объекте.|
|[Иконнектионпоинтконтаинеримпл:: Финдконнектионпоинт](#findconnectionpoint)|Извлекает указатель интерфейса на точку соединения, которая поддерживает указанный IID.|

## <a name="remarks"></a>Комментарии

`IConnectionPointContainerImpl` реализует контейнер точек соединения для управления коллекцией объектов [иконнектионпоинтимпл](../../atl/reference/iconnectionpointimpl-class.md) . `IConnectionPointContainerImpl` предоставляет два метода, которые клиент может вызвать для получения дополнительных сведений о подключаемом объекте:

- `EnumConnectionPoints` позволяет клиенту определить, какие исходящие интерфейсы поддерживаются объектом.

- `FindConnectionPoint` позволяет клиенту определить, поддерживает ли объект определенный исходящий интерфейс.

Сведения об использовании точек подключения в ATL см. в статье [точки подключения](../../atl/atl-connection-points.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IConnectionPointContainer`

`IConnectionPointContainerImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="iconnectionpointcontainerimplenumconnectionpoints"></a><a name="enumconnectionpoints"></a> Иконнектионпоинтконтаинеримпл:: Енумконнектионпоинтс

Создает перечислитель для прохода по точкам соединения, поддерживаемым в подключаемом объекте.

```
STDMETHOD(EnumConnectionPoints)(IEnumConnectionPoints** ppEnum);
```

### <a name="remarks"></a>Комментарии

См. раздел [IConnectionPointContainer:: енумконнектионпоинтс](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints) в Windows SDK.

## <a name="iconnectionpointcontainerimplfindconnectionpoint"></a><a name="findconnectionpoint"></a> Иконнектионпоинтконтаинеримпл:: Финдконнектионпоинт

Извлекает указатель интерфейса на точку соединения, которая поддерживает указанный IID.

```
STDMETHOD(FindConnectionPoint)(REFIID riid, IConnectionPoint** ppCP);
```

### <a name="remarks"></a>Комментарии

См. раздел [IConnectionPointContainer:: финдконнектионпоинт](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
