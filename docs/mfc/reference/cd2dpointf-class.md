---
description: 'Дополнительные сведения о: CD2DPointF Class'
title: Класс CD2DPointF
ms.date: 11/04/2016
f1_keywords:
- CD2DPointF
- AFXRENDERTARGET/CD2DPointF
- AFXRENDERTARGET/CD2DPointF::CD2DPointF
helpviewer_keywords:
- CD2DPointF [MFC], CD2DPointF
ms.assetid: 30f72083-1c8a-4f50-adb2-72dbbe3522d4
ms.openlocfilehash: 0f63aa35acb33504c96316b67ecc4f885f4f0247
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193361"
---
# <a name="cd2dpointf-class"></a>Класс CD2DPointF

Программа-оболочка для `D2D1_POINT_2F`.

## <a name="syntax"></a>Синтаксис

```
class CD2DPointF : public D2D1_POINT_2F;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DPointF::CD2DPointF](#cd2dpointf)|Перегружен. Конструирует `CD2DPointF` объект из `D2D1_POINT_2F` объекта.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DPointF:: operator CPoint](#operator_cpoint)|Преобразует `CD2DPointF` в `CPoint` объект.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`D2D1_POINT_2F`

`CD2DPointF`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dpointfcd2dpointf"></a><a name="cd2dpointf"></a> CD2DPointF::CD2DPointF

Конструирует объект CD2DPointF из объекта CPoint.

```
CD2DPointF(const CPoint& pt);
CD2DPointF(const D2D1_POINT_2F& pt);
CD2DPointF(const D2D1_POINT_2F* pt);
CD2DPointF(FLOAT fX = 0., FLOAT fY = 0.);
```

### <a name="parameters"></a>Параметры

*пт*<br/>
Исходная точка

*fX*<br/>
Источник X

*Обозначения*<br/>
Источник Y

## <a name="cd2dpointfoperator-cpoint"></a><a name="operator_cpoint"></a> CD2DPointF:: operator CPoint

Преобразует CD2DPointF в объект CPoint.

```
operator CPoint();
```

### <a name="return-value"></a>Возвращаемое значение

Текущее значение точки D2D.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
