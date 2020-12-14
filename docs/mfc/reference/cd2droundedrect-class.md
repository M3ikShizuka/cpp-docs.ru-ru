---
description: 'Дополнительные сведения о: CD2DRoundedRect Class'
title: Класс CD2DRoundedRect
ms.date: 11/04/2016
f1_keywords:
- CD2DRoundedRect
- AFXRENDERTARGET/CD2DRoundedRect
- AFXRENDERTARGET/CD2DRoundedRect::CD2DRoundedRect
helpviewer_keywords:
- CD2DRoundedRect [MFC], CD2DRoundedRect
ms.assetid: 06207fb5-e92b-41c0-bceb-b45d8f466531
ms.openlocfilehash: 13c1b0910c9d78f615d64e3eecba8bb813916413
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97240667"
---
# <a name="cd2droundedrect-class"></a>Класс CD2DRoundedRect

Программа-оболочка для `D2D1_ROUNDED_RECT`.

## <a name="syntax"></a>Синтаксис

```
class CD2DRoundedRect : public D2D1_ROUNDED_RECT;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DRoundedRect::CD2DRoundedRect](#cd2droundedrect)|Перегружен. Конструирует `CD2DRoundedRect` объект из `D2D1_ROUNDED_RECT` объекта.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`D2D1_ROUNDED_RECT`

[CD2DRoundedRect](../../mfc/reference/cd2droundedrect-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2droundedrectcd2droundedrect"></a><a name="cd2droundedrect"></a> CD2DRoundedRect::CD2DRoundedRect

Конструирует объект CD2DRoundedRect из объекта CD2DRectF.

```
CD2DRoundedRect(
    const CD2DRectF& rectIn,
    const CD2DSizeF& sizeRadius);

CD2DRoundedRect(const D2D1_ROUNDED_RECT& rectIn);
CD2DRoundedRect(const D2D1_ROUNDED_RECT* rectIn);
```

### <a name="parameters"></a>Параметры

*Rect*<br/>
Исходный прямоугольник

*сизерадиус*<br/>
Размер RADIUS

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
