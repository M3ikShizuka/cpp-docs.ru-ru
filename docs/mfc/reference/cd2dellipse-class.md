---
description: 'Дополнительные сведения о: CD2DEllipse Class'
title: Класс CD2DEllipse
ms.date: 08/29/2019
f1_keywords:
- CD2DEllipse
- AFXRENDERTARGET/CD2DEllipse
- AFXRENDERTARGET/CD2DEllipse::CD2DEllipse
helpviewer_keywords:
- CD2DEllipse [MFC], CD2DEllipse
ms.assetid: e9f02f54-acf2-427e-b349-db50cd9a77df
ms.openlocfilehash: 827ba5515cb4b20cb8e5b10012590a001e01c08f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97313064"
---
# <a name="cd2dellipse-class"></a>Класс CD2DEllipse

Программа-оболочка для `D2D1_ELLIPSE`.

## <a name="syntax"></a>Синтаксис

```
class CD2DEllipse : public D2D1_ELLIPSE;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DEllipse::CD2DEllipse](#cd2dellipse)|Перегружен. Конструирует `CD2DEllipse` объект из `D2D1_ELLIPSE` объекта.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`D2D1_ELLIPSE`

`CD2DEllipse`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dellipsecd2dellipse"></a><a name="cd2dellipse"></a> CD2DEllipse::CD2DEllipse

Конструирует объект CD2DEllipse из объекта CD2DRectF.

```
CD2DEllipse(const CD2DRectF& rect);
CD2DEllipse(const D2D1_ELLIPSE& ellipse);
CD2DEllipse(const D2D1_ELLIPSE* ellipse);

CD2DEllipse(
    const CD2DPointF& ptCenter,
    const CD2DSizeF& sizeRadius);
```

### <a name="parameters"></a>Параметры

*rect*<br/>
Исходный прямоугольник

*эллипс*<br/>
Источник эллипса

*птцентер*<br/>
Центральная точка эллипса.

*сизерадиус*<br/>
X-радиус и Y-радиус эллипса.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
