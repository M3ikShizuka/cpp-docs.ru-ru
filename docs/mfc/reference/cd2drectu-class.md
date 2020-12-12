---
description: 'Дополнительные сведения о: CD2DRectU Class'
title: Класс CD2DRectU
ms.date: 11/04/2016
f1_keywords:
- CD2DRectU
- AFXRENDERTARGET/CD2DRectU
- AFXRENDERTARGET/CD2DRectU::CD2DRectU
- AFXRENDERTARGET/CD2DRectU::IsNull
helpviewer_keywords:
- CD2DRectU [MFC], CD2DRectU
- CD2DRectU [MFC], IsNull
ms.assetid: a62f17d1-011d-4867-8f51-fd7e7c00561d
ms.openlocfilehash: dadbaf37f1ed11f96f29c7e4cf78eebf8095590d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97301624"
---
# <a name="cd2drectu-class"></a>Класс CD2DRectU

Программа-оболочка для `D2D1_RECT_U`.

## <a name="syntax"></a>Синтаксис

```
class CD2DRectU : public D2D1_RECT_U;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DRectU::CD2DRectU](#cd2drectu)|Перегружен. Конструирует `CD2DRectU` объект из `D2D1_RECT_U` объекта.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DRectU:: IsNull](#isnull)|Возвращает **логическое** значение, указывающее, содержит ли выражение допустимые данные (null).|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DRectU:: operator Крект](#operator_crect)|Преобразует `CD2DRectU` в `CRect` объект.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`D2D1_RECT_U`

`CD2DRectU`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2drectucd2drectu"></a><a name="cd2drectu"></a> CD2DRectU::CD2DRectU

Конструирует объект CD2DRectU из объекта Крект.

```
CD2DRectU(const CRect& rect);
CD2DRectU(const D2D1_RECT_U& rect);
CD2DRectU(const D2D1_RECT_U* rect);

CD2DRectU(
    UINT32 uLeft = 0,
    UINT32 uTop = 0,
    UINT32 uRight = 0,
    UINT32 uBottom = 0);
```

### <a name="parameters"></a>Параметры

*rect*<br/>
Исходный прямоугольник

*улефт*<br/>
Координата слева источника

*утоп*<br/>
Координата вершины источника

*уригхт*<br/>
Координата справа источника

*уботтом*<br/>
координата нижней части источника

## <a name="cd2drectuisnull"></a><a name="isnull"></a> CD2DRectU:: IsNull

Возвращает логическое значение, указывающее, содержит ли выражение допустимые данные (null).

```
BOOL IsNull() const;
```

### <a name="return-value"></a>Возвращаемое значение

TRUE, если значения верхнего, левого, нижнего и правого прямоугольника равны 0; в противном случае — FALSE.

## <a name="cd2drectuoperator-crect"></a><a name="operator_crect"></a> CD2DRectU:: operator Крект

Преобразует CD2DRectU в объект Крект.

```
operator CRect();
```

### <a name="return-value"></a>Возвращаемое значение

Текущее значение прямоугольника D2D.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
