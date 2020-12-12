---
description: 'Дополнительные сведения о: Квинтраитсор Class'
title: Класс Квинтраитсор
ms.date: 11/04/2016
f1_keywords:
- CWinTraitsOR
- ATLWIN/ATL::CWinTraitsOR
- ATLWIN/ATL::CWinTraitsOR::GetWndExStyle
- ATLWIN/ATL::CWinTraitsOR::GetWndStyle
helpviewer_keywords:
- CWinTraitsOR class
- window styles, default values for ATL
ms.assetid: 1eb7b1e8-a9bd-411b-a30a-35a8a10af989
ms.openlocfilehash: 1d0a7ff8a78ebbdc416bdace2a1ea1f0199c292f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140066"
---
# <a name="cwintraitsor-class"></a>Класс Квинтраитсор

Этот класс предоставляет метод для стандартизации стилей, используемых при создании объекта Window.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template <DWORD t_dwStyle = 0,
          DWORD t_dwExStyle = 0,
          class TWinTraits = CControlWinTraits>
class CWinTraitsOR
```

#### <a name="parameters"></a>Параметры

*t_dwStyle*<br/>
Стили окна по умолчанию.

*t_dwExStyle*<br/>
Расширенные стили окна по умолчанию.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Квинтраитсор:: Жетвндексстиле](#getwndexstyle)|Извлекает расширенные стили для `CWinTraitsOR` объекта.|
|[Квинтраитсор:: Жетвндстиле](#getwndstyle)|Возвращает стандартные стили для `CWinTraitsOR` объекта.|

## <a name="remarks"></a>Комментарии

Этот класс признаков [окон](../../atl/understanding-window-traits.md) предоставляет простой метод стандартизации стилей, используемых для создания объекта окна ATL. Используйте специализацию этого класса в качестве параметра шаблона для [квиндовимпл](../../atl/reference/cwindowimpl-class.md) или другого класса окна ATL, чтобы указать минимальный набор стандартных и расширенных стилей, которые будут использоваться для экземпляров этого класса окна.

Используйте специализацию этого шаблона, если нужно убедиться, что определенные стили заданы для всех экземпляров класса Window, при этом другие стили могут быть заданы для каждого экземпляра в вызове метода [квиндовимпл:: Create](../../atl/reference/cwindowimpl-class.md#create).

Если необходимо предоставить стили окна по умолчанию, которые будут использоваться только в том случае, если в вызове не указаны другие стили `CWindowImpl::Create` , используйте вместо него [квинтраитс](../../atl/reference/cwintraits-class.md) .

## <a name="requirements"></a>Требования

**Заголовок:** atlwin. h

## <a name="cwintraitsorgetwndstyle"></a><a name="getwndstyle"></a> Квинтраитсор:: Жетвндстиле

Вызовите эту функцию, чтобы получить сочетание (с помощью логического оператора OR) стандартных стилей `CWinTraits` объекта и стилей по умолчанию, заданных *t_dwStyle*.

```
static DWORD GetWndStyle(DWORD dwStyle);
```

### <a name="parameters"></a>Параметры

*двстиле*<br/>
Стили, используемые для создания окна.

### <a name="return-value"></a>Возвращаемое значение

Сочетание стилей, передаваемых в *двстиле* , и значений по умолчанию, заданных с `t_dwStyle` помощью логического оператора или.

## <a name="cwintraitsorgetwndexstyle"></a><a name="getwndexstyle"></a> Квинтраитсор:: Жетвндексстиле

Вызывайте эту функцию для получения сочетания (с помощью логического оператора OR) расширенных стилей `CWinTraits` объекта и стилей по умолчанию, заданных параметром `t_dwStyle` .

```
static DWORD GetWndExStyle(DWORD dwExStyle);
```

### <a name="parameters"></a>Параметры

*двексстиле*<br/>
Расширенные стили, используемые для создания окна.

### <a name="return-value"></a>Возвращаемое значение

Сочетание расширенных стилей, передаваемых в *двексстиле* и значений по умолчанию, заданных с `t_dwExStyle` помощью логического оператора или

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Основные сведения о характеристиках окна](../../atl/understanding-window-traits.md)
