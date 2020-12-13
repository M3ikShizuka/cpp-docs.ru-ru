---
description: 'Дополнительные сведения о: Ипоинтеринактивеимпл Class'
title: Класс Ипоинтеринактивеимпл
ms.date: 11/04/2016
f1_keywords:
- IPointerInactiveImpl
- ATLCTL/ATL::IPointerInactiveImpl
- ATLCTL/ATL::IPointerInactiveImpl::GetActivationPolicy
- ATLCTL/ATL::IPointerInactiveImpl::OnInactiveMouseMove
- ATLCTL/ATL::IPointerInactiveImpl::OnInactiveSetCursor
helpviewer_keywords:
- IPointerInactive ATL implementation
- inactive objects
- IPointerInactiveImpl class
ms.assetid: e1fe9ea6-d38a-4527-9112-eb344771e0b7
ms.openlocfilehash: 0ee5c103582ff68c80edd36316179b47a1b7931d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139312"
---
# <a name="ipointerinactiveimpl-class"></a>Класс Ипоинтеринактивеимпл

Этот класс реализует `IUnknown` методы интерфейса [интерфейс IPointerInactive](/windows/win32/api/ocidl/nn-ocidl-ipointerinactive) и.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class T>
class IPointerInactiveImpl
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IPointerInactiveImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ипоинтеринактивеимпл:: Жетактиватионполици](#getactivationpolicy)|Извлекает текущую политику активации для объекта. Реализация ATL возвращает E_NOTIMPL.|
|[Ипоинтеринактивеимпл:: Онинактивемаусемове](#oninactivemousemove)|Уведомляет объект о том, что указатель мыши переместился на него, указывая, что объект может вызывать события мыши. Реализация ATL возвращает E_NOTIMPL.|
|[Ипоинтеринактивеимпл:: Онинактивесеткурсор](#oninactivesetcursor)|Задает указатель мыши для неактивного объекта. Реализация ATL возвращает E_NOTIMPL.|

## <a name="remarks"></a>Комментарии

Неактивным является объект, который просто загружается или выполняется. В отличие от активного объекта, неактивный объект не может принимать сообщения мыши и клавиатуры Windows. Таким способом, неактивные объекты используют меньше ресурсов и, как правило, более эффективны.

Интерфейс [интерфейс IPointerInactive](/windows/win32/api/ocidl/nn-ocidl-ipointerinactive) позволяет объекту поддерживать минимальный уровень взаимодействия мыши, пока остается неактивным. Эта функция особенно полезна для элементов управления.

Класс `IPointerInactiveImpl` реализует `IPointerInactive` методы, просто возвращая E_NOTIMPL. Однако он реализуется `IUnknown` путем отправки информации в устройство дампа в отладочных сборках.

Руководство по **сопутствующим статьям** [ATL](../../atl/active-template-library-atl-tutorial.md), [Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IPointerInactive`

`IPointerInactiveImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлктл. h

## <a name="ipointerinactiveimplgetactivationpolicy"></a><a name="getactivationpolicy"></a> Ипоинтеринактивеимпл:: Жетактиватионполици

Извлекает текущую политику активации для объекта.

```
HRESULT GetActivationPolicy(DWORD* pdwPolicy);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает E_NOTIMPL.

### <a name="remarks"></a>Комментарии

См. раздел [интерфейс IPointerInactive:: жетактиватионполици](/windows/win32/api/ocidl/nf-ocidl-ipointerinactive-getactivationpolicy) в Windows SDK.

## <a name="ipointerinactiveimploninactivemousemove"></a><a name="oninactivemousemove"></a> Ипоинтеринактивеимпл:: Онинактивемаусемове

Уведомляет объект о том, что указатель мыши переместился на него, указывая, что объект может вызывать события мыши.

```
HRESULT OnInactiveMouseMove(
    LPCRECT pRectBounds,
    long x,
    long y,
    DWORD dwMouseMsg);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает E_NOTIMPL.

### <a name="remarks"></a>Комментарии

См. раздел [интерфейс IPointerInactive:: онинактивемаусемове](/windows/win32/api/ocidl/nf-ocidl-ipointerinactive-oninactivemousemove) в Windows SDK.

## <a name="ipointerinactiveimploninactivesetcursor"></a><a name="oninactivesetcursor"></a> Ипоинтеринактивеимпл:: Онинактивесеткурсор

Задает указатель мыши для неактивного объекта.

```
HRESULT OnInactiveSetCursor(
    LPCRECT pRectBounds,
    long x,
    long y,
    DWORD dwMouseMsg,
    BOOL fSetAlways);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает E_NOTIMPL.

### <a name="remarks"></a>Комментарии

См. раздел [интерфейс IPointerInactive:: онинактивесеткурсор](/windows/win32/api/ocidl/nf-ocidl-ipointerinactive-oninactivesetcursor) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
