---
description: 'Дополнительные сведения о: CD2DGradientBrush Class'
title: Класс CD2DGradientBrush
ms.date: 03/27/2019
f1_keywords:
- CD2DGradientBrush
- AFXRENDERTARGET/CD2DGradientBrush
- AFXRENDERTARGET/CD2DGradientBrush::CD2DGradientBrush
- AFXRENDERTARGET/CD2DGradientBrush::Destroy
- AFXRENDERTARGET/CD2DGradientBrush::m_arGradientStops
- AFXRENDERTARGET/CD2DGradientBrush::m_colorInterpolationGamma
- AFXRENDERTARGET/CD2DGradientBrush::m_extendMode
- AFXRENDERTARGET/CD2DGradientBrush::m_pGradientStops
helpviewer_keywords:
- CD2DGradientBrush [MFC], CD2DGradientBrush
- CD2DGradientBrush [MFC], Destroy
- CD2DGradientBrush [MFC], m_arGradientStops
- CD2DGradientBrush [MFC], m_colorInterpolationGamma
- CD2DGradientBrush [MFC], m_extendMode
- CD2DGradientBrush [MFC], m_pGradientStops
ms.assetid: 5bf133e6-16b7-4e3a-845d-0ce63fafe5ec
ms.openlocfilehash: c1af08ae27bd2cbee48c4abe22f413ffeb85cd1c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193400"
---
# <a name="cd2dgradientbrush-class"></a>Класс CD2DGradientBrush

Базовый класс классов CD2DLinearGradientBrush и CD2DRadialGradientBrush.

## <a name="syntax"></a>Синтаксис

```
class CD2DGradientBrush : public CD2DBrush;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DGradientBrush::CD2DGradientBrush](#cd2dgradientbrush)|Конструирует объект CD2DGradientBrush.|
|[CD2DGradientBrush:: ~ CD2DGradientBrush](#_dtorcd2dgradientbrush)|Деструктор Вызывается при уничтожении объекта кисти градиента D2D.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[CD2DGradientBrush::D естрой](#destroy)|Уничтожает объект CD2DGradientBrush. (Переопределяет [CD2DBrush::D естрой](../../mfc/reference/cd2dbrush-class.md#destroy).)|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DGradientBrush:: m_arGradientStops](#m_argradientstops)|Массив структур D2D1_GRADIENT_STOP.|
|[CD2DGradientBrush:: m_colorInterpolationGamma](#m_colorinterpolationgamma)|Пространство, в котором выполняется интерполяция цветов между преостановками градиента.|
|[CD2DGradientBrush:: m_extendMode](#m_extendmode)|Поведение градиента за пределами нормализованного диапазона [0, 1].|
|[CD2DGradientBrush:: m_pGradientStops](#m_pgradientstops)|Указатель на массив структур D2D1_GRADIENT_STOP.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

[CD2DBrush](../../mfc/reference/cd2dbrush-class.md)

`CD2DGradientBrush`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dgradientbrushcd2dgradientbrush"></a><a name="_dtorcd2dgradientbrush"></a> CD2DGradientBrush:: ~ CD2DGradientBrush

Деструктор Вызывается при уничтожении объекта кисти градиента D2D.

```
virtual ~CD2DGradientBrush();
```

## <a name="cd2dgradientbrushcd2dgradientbrush"></a><a name="cd2dgradientbrush"></a> CD2DGradientBrush::CD2DGradientBrush

Конструирует объект CD2DGradientBrush.

```
CD2DGradientBrush(
    CRenderTarget* pParentTarget,
    const D2D1_GRADIENT_STOP* gradientStops,
    UINT gradientStopsCount,
    D2D1_GAMMA colorInterpolationGamma = D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE extendMode = D2D1_EXTEND_MODE_CLAMP,
    CD2DBrushProperties* pBrushProperties = NULL,
    BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*градиентстопс*<br/>
Указатель на массив структур D2D1_GRADIENT_STOP.

*градиентстопскаунт*<br/>
Значение, большее или равное 1, которое указывает количество ограничителей градиента в массиве Градиентстопс.

*колоринтерполатионгамма*<br/>
Пространство, в котором выполняется интерполяция цветов между преостановками градиента.

*екстендмоде*<br/>
Поведение градиента за пределами нормализованного диапазона [0, 1].

*пбрушпропертиес*<br/>
Указатель на непрозрачность и Преобразование кисти.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

## <a name="cd2dgradientbrushdestroy"></a><a name="destroy"></a> CD2DGradientBrush::D естрой

Уничтожает объект CD2DGradientBrush.

```
virtual void Destroy();
```

## <a name="cd2dgradientbrushm_argradientstops"></a><a name="m_argradientstops"></a> CD2DGradientBrush:: m_arGradientStops

Массив структур D2D1_GRADIENT_STOP.

```
CArray<D2D1_GRADIENT_STOP, D2D1_GRADIENT_STOP> m_arGradientStops;
```

## <a name="cd2dgradientbrushm_colorinterpolationgamma"></a><a name="m_colorinterpolationgamma"></a> CD2DGradientBrush:: m_colorInterpolationGamma

Пространство, в котором выполняется интерполяция цветов между преостановками градиента.

```
D2D1_GAMMA m_colorInterpolationGamma;
```

## <a name="cd2dgradientbrushm_extendmode"></a><a name="m_extendmode"></a> CD2DGradientBrush:: m_extendMode

Поведение градиента за пределами нормализованного диапазона [0, 1].

```
D2D1_EXTEND_MODE m_extendMode;
```

## <a name="cd2dgradientbrushm_pgradientstops"></a><a name="m_pgradientstops"></a> CD2DGradientBrush:: m_pGradientStops

Указатель на массив структур D2D1_GRADIENT_STOP.

```
ID2D1GradientStopCollection* m_pGradientStops;
```

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
