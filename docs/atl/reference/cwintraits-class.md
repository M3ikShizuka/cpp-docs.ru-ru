---
description: 'Дополнительные сведения о: Квинтраитс Class'
title: Класс Квинтраитс
ms.date: 11/04/2016
f1_keywords:
- CWinTraits
- ATLWIN/ATL::CWinTraits
- ATLWIN/ATL::CWinTraits::GetWndExStyle
- ATLWIN/ATL::CWinTraits::GetWndStyle
helpviewer_keywords:
- CMDIChildWinTraits class
- window styles, default values for ATL
- CWinTraits class
- CFrameWinTraits class
- CControlWinTraits class
ms.assetid: f78f486e-6d9c-42c6-8e86-371e05aa7e59
ms.openlocfilehash: 3f23342cae58d70a602ebce1dcbe7efcddf36781
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140092"
---
# <a name="cwintraits-class"></a>Класс Квинтраитс

Этот класс предоставляет метод для стандартизации стилей, используемых при создании объекта Window.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template <DWORD t_dwStyle = 0, DWORD t_dwExStyle = 0>  class CWinTraits
```

#### <a name="parameters"></a>Параметры

*t_dwStyle*<br/>
Стандартные стили окна по умолчанию.

*t_dwExStyle*<br/>
Расширенные стили окна по умолчанию.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Квинтраитс:: Жетвндексстиле](#getwndexstyle)|Статически Извлекает расширенные стили для `CWinTraits` объекта.|
|[Квинтраитс:: Жетвндстиле](#getwndstyle)|Статически Возвращает стандартные стили для `CWinTraits` объекта.|

## <a name="remarks"></a>Комментарии

Этот класс признаков [окон](../../atl/understanding-window-traits.md) предоставляет простой метод стандартизации стилей, используемых для создания объекта окна ATL. Используйте специализацию этого класса в качестве параметра шаблона для [квиндовимпл](../../atl/reference/cwindowimpl-class.md) или другого класса окна ATL, чтобы указать стандартные и расширенные стили, используемые для экземпляров этого класса окон.

Используйте этот шаблон, если требуется предоставить стили окна по умолчанию, которые будут использоваться только в том случае, если в вызове [квиндовимпл:: Create](../../atl/reference/cwindowimpl-class.md#create)не указаны другие стили.

ATL предоставляет три предопределенные специализации этого шаблона для часто используемых сочетаний стилей окон:

- `CControlWinTraits`

   Предназначен для стандартного окна управления. Используются следующие стандартные стили: WS_CHILD, WS_VISIBLE, WS_CLIPCHILDREN и WS_CLIPSIBLINGS. Расширенные стили отсутствуют.

- `CFrameWinTraits`

   Предназначен для стандартного окна фрейма. К стандартным стилям относятся: WS_OVERLAPPEDWINDOW, WS_CLIPCHILDREN и WS_CLIPSIBLINGS. В число используемых расширенных стилей входят: WS_EX_APPWINDOW и WS_EX_WINDOWEDGE.

- `CMDIChildWinTraits`

   Предназначен для стандартного дочернего окна MDI. К стандартным стилям относятся: WS_OVERLAPPEDWINDOW, WS_CHILD, WS_VISIBLE, WS_CLIPCHILDREN и WS_CLIPSIBLINGS. В число используемых расширенных стилей входят: WS_EX_MDICHILD.

Если необходимо убедиться, что определенные стили заданы для всех экземпляров класса Window, при этом другие стили могут быть заданы для каждого экземпляра, используйте вместо него [квинтраитсор](../../atl/reference/cwintraitsor-class.md) .

## <a name="requirements"></a>Требования

**Заголовок:** atlwin. h

## <a name="cwintraitsgetwndstyle"></a><a name="getwndstyle"></a> Квинтраитс:: Жетвндстиле

Вызовите эту функцию, чтобы получить стандартные стили `CWinTraits` объекта.

```
static DWORD GetWndStyle(DWORD dwStyle);
```

### <a name="parameters"></a>Параметры

*двстиле*<br/>
Стандартные стили, используемые для создания окна. Если *двстиле* имеет значение 0, возвращаются значения стиля шаблона ( `t_dwStyle` ). Если *двстиле* имеет ненулевое значение, возвращается *двстиле* .

### <a name="return-value"></a>Возвращаемое значение

Стандартные стили окна объекта.

## <a name="cwintraitsgetwndexstyle"></a><a name="getwndexstyle"></a> Квинтраитс:: Жетвндексстиле

Вызовите эту функцию, чтобы получить расширенные стили `CWinTraits` объекта.

```
static DWORD GetWndExStyle(DWORD dwExStyle);
```

### <a name="parameters"></a>Параметры

*двексстиле*<br/>
Расширенные стили, используемые для создания окна. Если *двексстиле* имеет значение 0, возвращаются значения стиля шаблона ( `t_dwExStyle` ). Если *двексстиле* имеет ненулевое значение, возвращается *двексстиле* .

### <a name="return-value"></a>Возвращаемое значение

Расширенные стили окна объекта.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Основные сведения о характеристиках окна](../../atl/understanding-window-traits.md)
