---
description: 'Дополнительные сведения о: Кдефаултчартраитс Class'
title: Класс Кдефаултчартраитс
ms.date: 11/04/2016
f1_keywords:
- CDefaultCharTraits
- ATLCOLL/ATL::CDefaultCharTraits
- ATLCOLL/ATL::CDefaultCharTraits::CharToLower
- ATLCOLL/ATL::CDefaultCharTraits::CharToUpper
helpviewer_keywords:
- CDefaultCharTraits class
ms.assetid: f94a3934-597f-401d-8513-ed6924ae069a
ms.openlocfilehash: 6d98c6b6ffb527fef1e5b2320b46eda61ec3f670
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141964"
---
# <a name="cdefaultchartraits-class"></a>Класс Кдефаултчартраитс

Этот класс предоставляет две статические функции для преобразования символов между прописными и строчными буквами.

## <a name="syntax"></a>Синтаксис

```
template <typename T>
class CDefaultCharTraits
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных, сохраняемых в коллекции.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кдефаултчартраитс:: Чартоловер](#chartolower)|Статически Вызовите эту функцию, чтобы преобразовать символ в верхний регистр.|
|[Кдефаултчартраитс:: Чартауппер](#chartoupper)|Статически Вызовите эту функцию, чтобы преобразовать символ в нижний регистр.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет функции, используемые классом [кстринжелементтраитси](../../atl/reference/cstringelementtraitsi-class.md).

## <a name="requirements"></a>Требования

**Заголовок:** атлколл. h

## <a name="cdefaultchartraitschartolower"></a><a name="chartolower"></a> Кдефаултчартраитс:: Чартоловер

Вызовите эту функцию, чтобы преобразовать символ в нижний регистр.

```
static wchar_t CharToLower(wchar_t x);
static char CharToLower(char x);
```

### <a name="parameters"></a>Параметры

*x*<br/>
Знак для преобразования в нижний регистр.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#132](../../atl/codesnippet/cpp/cdefaultchartraits-class_1.cpp)]

## <a name="cdefaultchartraitschartoupper"></a><a name="chartoupper"></a> Кдефаултчартраитс:: Чартауппер

Вызовите эту функцию, чтобы преобразовать символ в верхний регистр.

```
static wchar_t CharToUpper(wchar_t x);
static char CharToUpper(char x);
```

### <a name="parameters"></a>Параметры

*x*<br/>
Знак для преобразования в верхний регистр.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
