---
description: 'Дополнительные сведения о: CD2DPointU Class'
title: Класс CD2DPointU
ms.date: 08/29/2019
f1_keywords:
- CD2DPointU
- AFXRENDERTARGET/CD2DPointU
- AFXRENDERTARGET/CD2DPointU::CD2DPointU
helpviewer_keywords:
- CD2DPointU [MFC], CD2DPointU
ms.assetid: 04733f96-b6de-4a89-82e3-caad1e8087a9
ms.openlocfilehash: 04c1c366f3026e4a621892fc1c7617707c33d23d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97251002"
---
# <a name="cd2dpointu-class"></a>Класс CD2DPointU

Программа-оболочка для `D2D1_POINT_2U`.

## <a name="syntax"></a>Синтаксис

```
class CD2DPointU : public D2D1_POINT_2U;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DPointU::CD2DPointU](#cd2dpointu)|Перегружен. Конструирует объект `CD2DPointU` из `D2D1_POINT_2U` объекта.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DPointU:: operator CPoint](#operator_cpoint)|Преобразует `CD2DPointU` в `CPoint` объект.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`D2D1_POINT_2U`

`CD2DPointU`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dpointucd2dpointu"></a><a name="cd2dpointu"></a> CD2DPointU::CD2DPointU

Конструирует объект CD2DPointU из объекта CPoint.

```
CD2DPointU(const CPoint& pt);
CD2DPointU(const D2D1_POINT_2U& pt);
CD2DPointU(const D2D1_POINT_2U* pt);
CD2DPointU(UINT32 uX = 0, UINT32 uY = 0);
```

### <a name="parameters"></a>Параметры

*пт*<br/>
Исходная точка

*Взаимодействия*<br/>
Источник X

*uY*<br/>
Источник Y

## <a name="cd2dpointuoperator-cpoint"></a><a name="operator_cpoint"></a> CD2DPointU:: operator CPoint

Преобразует CD2DPointU в объект CPoint.

```
operator CPoint();
```

### <a name="return-value"></a>Возвращаемое значение

Текущее значение точки D2D.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
