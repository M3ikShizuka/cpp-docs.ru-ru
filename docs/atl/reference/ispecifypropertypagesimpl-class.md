---
description: 'Дополнительные сведения о: ИспеЦифипропертипажесимпл Class'
title: Класс ИспеЦифипропертипажесимпл
ms.date: 11/04/2016
f1_keywords:
- ISpecifyPropertyPagesImpl
- ATLCOM/ATL::ISpecifyPropertyPagesImpl
- ATLCOM/ATL::ISpecifyPropertyPagesImpl::GetPages
helpviewer_keywords:
- property pages, CLSIDs associated with
- ISpecifyPropertyPages
- ISpecifyPropertyPagesImpl class
ms.assetid: 4e4b9795-b656-4d56-9b8c-85941e7731f9
ms.openlocfilehash: 528fafa0473a4aa803e1c1d17a24b2d27584c33a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158053"
---
# <a name="ispecifypropertypagesimpl-class"></a>Класс ИспеЦифипропертипажесимпл

Этот класс реализует `IUnknown` интерфейс [испеЦифипропертипажес](/windows/win32/api/ocidl/nn-ocidl-ispecifypropertypages) и предоставляет реализацию по умолчанию.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class T>
class ATL_NO_VTABLE ISpecifyPropertyPagesImpl
   : public ISpecifyPropertyPages
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `ISpecifyPropertyPagesImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[ИспеЦифипропертипажесимпл::-выстр.](#getpages)|Заполняет считанный массив значений UUID. Каждый UUID соответствует CLSID для одной из страниц свойств, которые могут отображаться на странице свойств объекта.|

## <a name="remarks"></a>Комментарии

Интерфейс [испеЦифипропертипажес](/windows/win32/api/ocidl/nn-ocidl-ispecifypropertypages) позволяет клиенту получить список идентификаторов CLSID для страниц свойств, поддерживаемых объектом. Класс `ISpecifyPropertyPagesImpl` предоставляет реализацию этого интерфейса по умолчанию и реализует `IUnknown` , отправляя сведения в устройство дампа в отладочных сборках.

> [!NOTE]
> Не предоставляйте интерфейс, `ISpecifyPropertyPages` Если объект не поддерживает страницы свойств.

Руководство по **сопутствующим статьям** [ATL](../../atl/active-template-library-atl-tutorial.md), [Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`ISpecifyPropertyPages`

`ISpecifyPropertyPagesImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ispecifypropertypagesimplgetpages"></a><a name="getpages"></a> ИспеЦифипропертипажесимпл::-выстр.

Заполняет массив в структуре [КАУУИД](/windows/win32/api/ocidl/ns-ocidl-cauuid) идентификаторами CLSID для страниц свойств, которые могут отображаться на странице свойств объекта.

```
STDMETHOD(GetPages)(CAUUID* pPages);
```

### <a name="remarks"></a>Комментарии

ATL использует карту свойств объекта для получения каждого идентификатора CLSID.

См. раздел [испеЦифипропертипажес::-Pages](/windows/win32/api/ocidl/nf-ocidl-ispecifypropertypages-getpages) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Класс Ипропертипажеимпл](../../atl/reference/ipropertypageimpl-class.md)<br/>
[Класс Иперпропертибровсингимпл](../../atl/reference/iperpropertybrowsingimpl-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
