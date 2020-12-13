---
description: 'Дополнительные сведения о: Иперпропертибровсингимпл Class'
title: Класс Иперпропертибровсингимпл
ms.date: 11/04/2016
f1_keywords:
- IPerPropertyBrowsingImpl
- ATLCTL/ATL::IPerPropertyBrowsingImpl
- ATLCTL/ATL::IPerPropertyBrowsingImpl::GetDisplayString
- ATLCTL/ATL::IPerPropertyBrowsingImpl::GetPredefinedStrings
- ATLCTL/ATL::IPerPropertyBrowsingImpl::GetPredefinedValue
- ATLCTL/ATL::IPerPropertyBrowsingImpl::MapPropertyToPage
helpviewer_keywords:
- IPerPropertyBrowsingImpl class
- property pages, accessing information
- IPerPropertyBrowsing, ATL implementation
ms.assetid: 0b1a9be3-d242-4767-be69-663a21e4b728
ms.openlocfilehash: eba17c0011343f50f586b13086dc76229f08ba3c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139351"
---
# <a name="iperpropertybrowsingimpl-class"></a>Класс Иперпропертибровсингимпл

Этот класс реализует `IUnknown` и позволяет клиенту обращаться к данным на страницах свойств объекта.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```

template <class T>
class ATL_NO_VTABLE IPerPropertyBrowsingImpl :
    public IPerPropertyBrowsing
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IPerPropertyBrowsingImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Иперпропертибровсингимпл:: Жетдисплайстринг](#getdisplaystring)|Извлекает строку, описывающую заданное свойство.|
|[Иперпропертибровсингимпл:: Жетпредефинедстрингс](#getpredefinedstrings)|Извлекает массив строк, соответствующий значениям, которые может принимать данное свойство.|
|[Иперпропертибровсингимпл:: Жетпредефинедвалуе](#getpredefinedvalue)|Извлекает объект типа VARIANT, содержащий значение свойства, идентифицируемого по заданному идентификатору DISPID. Идентификатор DISPID связан с именем строки, полученным из `GetPredefinedStrings` . Реализация ATL возвращает E_NOTIMPL.|
|[Иперпропертибровсингимпл:: Маппропертитопаже](#mappropertytopage)|Извлекает идентификатор CLSID страницы свойств, связанной с данным свойством.|

## <a name="remarks"></a>Комментарии

Интерфейс [иперпропертибровсинг](/windows/win32/api/ocidl/nn-ocidl-iperpropertybrowsing) позволяет клиенту получить доступ к информации на страницах свойств объекта. Класс `IPerPropertyBrowsingImpl` предоставляет реализацию этого интерфейса по умолчанию и реализует `IUnknown` , отправляя сведения в устройство дампа в отладочных сборках.

> [!NOTE]
> Если вы используете Microsoft Access в качестве приложения контейнера, необходимо создать класс, производный от `IPerPropertyBrowsingImpl` . В противном случае Access не будет загружать элемент управления.

Руководство по **сопутствующим статьям** [ATL](../../atl/active-template-library-atl-tutorial.md), [Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IPerPropertyBrowsing`

`IPerPropertyBrowsingImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлктл. h

## <a name="iperpropertybrowsingimplgetdisplaystring"></a><a name="getdisplaystring"></a> Иперпропертибровсингимпл:: Жетдисплайстринг

Извлекает строку, описывающую заданное свойство.

```
STDMETHOD(GetDisplayString)(
    DISPID dispID,
    BSTR* pBstr);
```

### <a name="remarks"></a>Комментарии

См. раздел [иперпропертибровсинг:: жетдисплайстринг](/windows/win32/api/ocidl/nf-ocidl-iperpropertybrowsing-getdisplaystring) в Windows SDK.

## <a name="iperpropertybrowsingimplgetpredefinedstrings"></a><a name="getpredefinedstrings"></a> Иперпропертибровсингимпл:: Жетпредефинедстрингс

Заполняет каждый массив нулевыми элементами.

```
STDMETHOD(GetPredefinedStrings)(
    DISPID dispID,
    CALPOLESTR* pCaStringsOut,
    CADWORD* pCaCookiesOut);
```

### <a name="return-value"></a>Возвращаемое значение

Реализация [жетпредефинедвалуе](#getpredefinedvalue) ВОЗВРАЩАЕТ в ATL E_NOTIMPL.

### <a name="remarks"></a>Комментарии

См. раздел [иперпропертибровсинг:: жетпредефинедстрингс](/windows/win32/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings) в Windows SDK.

## <a name="iperpropertybrowsingimplgetpredefinedvalue"></a><a name="getpredefinedvalue"></a> Иперпропертибровсингимпл:: Жетпредефинедвалуе

Извлекает объект типа VARIANT, содержащий значение свойства, идентифицируемого по заданному идентификатору DISPID. Идентификатор DISPID связан с именем строки, полученным из `GetPredefinedStrings` .

```
STDMETHOD(GetPredefinedValue)(
    DISPID dispID,
    DWORD dwCookie,
    VARIANT* pVarOut);
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает E_NOTIMPL.

### <a name="remarks"></a>Комментарии

Реализация [жетпредефинедстрингс](#getpredefinedstrings) библиотеки ATL не извлекает соответствующие строки.

См. раздел [иперпропертибровсинг:: жетпредефинедвалуе](/windows/win32/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue) в Windows SDK.

## <a name="iperpropertybrowsingimplmappropertytopage"></a><a name="mappropertytopage"></a> Иперпропертибровсингимпл:: Маппропертитопаже

Извлекает идентификатор CLSID страницы свойств, связанной с указанным свойством.

```
STDMETHOD(MapPropertyToPage)(
    DISPID dispID,
    CLSID* pClsid);
```

### <a name="remarks"></a>Комментарии

Для получения этих сведений в ATL используется схема свойств объекта.

См. раздел [иперпропертибровсинг:: маппропертитопаже](/windows/win32/api/ocidl/nf-ocidl-iperpropertybrowsing-mappropertytopage) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Класс Ипропертипажеимпл](../../atl/reference/ipropertypageimpl-class.md)<br/>
[Класс ИспеЦифипропертипажесимпл](../../atl/reference/ispecifypropertypagesimpl-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
