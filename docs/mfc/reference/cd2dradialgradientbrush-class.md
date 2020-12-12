---
description: 'Дополнительные сведения о: CD2DRadialGradientBrush Class'
title: Класс CD2DRadialGradientBrush
ms.date: 11/04/2016
f1_keywords:
- CD2DRadialGradientBrush
- AFXRENDERTARGET/CD2DRadialGradientBrush
- AFXRENDERTARGET/CD2DRadialGradientBrush::CD2DRadialGradientBrush
- AFXRENDERTARGET/CD2DRadialGradientBrush::Attach
- AFXRENDERTARGET/CD2DRadialGradientBrush::Create
- AFXRENDERTARGET/CD2DRadialGradientBrush::Destroy
- AFXRENDERTARGET/CD2DRadialGradientBrush::Detach
- AFXRENDERTARGET/CD2DRadialGradientBrush::Get
- AFXRENDERTARGET/CD2DRadialGradientBrush::GetCenter
- AFXRENDERTARGET/CD2DRadialGradientBrush::GetGradientOriginOffset
- AFXRENDERTARGET/CD2DRadialGradientBrush::GetRadiusX
- AFXRENDERTARGET/CD2DRadialGradientBrush::GetRadiusY
- AFXRENDERTARGET/CD2DRadialGradientBrush::SetCenter
- AFXRENDERTARGET/CD2DRadialGradientBrush::SetGradientOriginOffset
- AFXRENDERTARGET/CD2DRadialGradientBrush::SetRadiusX
- AFXRENDERTARGET/CD2DRadialGradientBrush::SetRadiusY
- AFXRENDERTARGET/CD2DRadialGradientBrush::m_pRadialGradientBrush
- AFXRENDERTARGET/CD2DRadialGradientBrush::m_RadialGradientBrushProperties
helpviewer_keywords:
- CD2DRadialGradientBrush [MFC], CD2DRadialGradientBrush
- CD2DRadialGradientBrush [MFC], Attach
- CD2DRadialGradientBrush [MFC], Create
- CD2DRadialGradientBrush [MFC], Destroy
- CD2DRadialGradientBrush [MFC], Detach
- CD2DRadialGradientBrush [MFC], Get
- CD2DRadialGradientBrush [MFC], GetCenter
- CD2DRadialGradientBrush [MFC], GetGradientOriginOffset
- CD2DRadialGradientBrush [MFC], GetRadiusX
- CD2DRadialGradientBrush [MFC], GetRadiusY
- CD2DRadialGradientBrush [MFC], SetCenter
- CD2DRadialGradientBrush [MFC], SetGradientOriginOffset
- CD2DRadialGradientBrush [MFC], SetRadiusX
- CD2DRadialGradientBrush [MFC], SetRadiusY
- CD2DRadialGradientBrush [MFC], m_pRadialGradientBrush
- CD2DRadialGradientBrush [MFC], m_RadialGradientBrushProperties
ms.assetid: 6c76d84a-d831-4ee2-96f1-82c1f5b0d6a9
ms.openlocfilehash: c5e169a5d608edd246d5c7269c94e3b225fdd491
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97118749"
---
# <a name="cd2dradialgradientbrush-class"></a>Класс CD2DRadialGradientBrush

Оболочка для ID2D1RadialGradientBrush.

## <a name="syntax"></a>Синтаксис

```
class CD2DRadialGradientBrush : public CD2DGradientBrush;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DRadialGradientBrush::CD2DRadialGradientBrush](#cd2dradialgradientbrush)|Конструирует объект CD2DLinearGradientBrush.|
|[CD2DRadialGradientBrush:: ~ CD2DRadialGradientBrush](#_dtorcd2dradialgradientbrush)|Деструктор Вызывается при уничтожении объекта кисти радиального градиента D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DRadialGradientBrush:: Attach](#attach)|Присоединяет существующий интерфейс ресурсов к объекту|
|[CD2DRadialGradientBrush:: Create](#create)|Создает CD2DRadialGradientBrush. (Переопределяет [CD2DResource:: Create](../../mfc/reference/cd2dresource-class.md#create).)|
|[CD2DRadialGradientBrush::D естрой](#destroy)|Уничтожает объект CD2DRadialGradientBrush. (Переопределяет [CD2DGradientBrush::D естрой](../../mfc/reference/cd2dgradientbrush-class.md#destroy).)|
|[CD2DRadialGradientBrush::D етач](#detach)|Отсоединяет интерфейс ресурса от объекта|
|[CD2DRadialGradientBrush:: Get](#get)|Возвращает интерфейс ID2D1RadialGradientBrush|
|[CD2DRadialGradientBrush:: выровнять](#getcenter)|Получает центр эллипса градиента|
|[CD2DRadialGradientBrush:: Жетградиенторигиноффсет](#getgradientoriginoffset)|Получает смещение начала градиента относительно центра эллипса.|
|[CD2DRadialGradientBrush:: Жетрадиускс](#getradiusx)|Получает x-радиус эллипса|
|[CD2DRadialGradientBrush:: радиус](#getradiusy)|Получает y-радиус эллипса|
|[CD2DRadialGradientBrush:: Сетцентер](#setcenter)|Задает центр эллипса градиента в пространстве координат кисти|
|[CD2DRadialGradientBrush:: Сетградиенторигиноффсет](#setgradientoriginoffset)|Задает смещение начала градиента относительно центра эллипса|
|[CD2DRadialGradientBrush:: Сетрадиускс](#setradiusx)|Задает радиус эллипса по оси x в пространстве координат кисти|
|[CD2DRadialGradientBrush:: Сетрадиуси](#setradiusy)|Задает y-радиус эллипса в пространстве координат кисти|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DRadialGradientBrush:: operator ID2D1RadialGradientBrush *](#operator_id2d1radialgradientbrush_star)|Возвращает интерфейс ID2D1RadialGradientBrush|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DRadialGradientBrush:: m_pRadialGradientBrush](#m_pradialgradientbrush)|Указатель на ID2D1RadialGradientBrush.|
|[CD2DRadialGradientBrush:: m_RadialGradientBrushProperties](#m_radialgradientbrushproperties)|Центр, смещение источника градиента и x-радиус и y-радиус градиента кисти.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

[CD2DBrush](../../mfc/reference/cd2dbrush-class.md)

[CD2DGradientBrush](../../mfc/reference/cd2dgradientbrush-class.md)

`CD2DRadialGradientBrush`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dradialgradientbrushcd2dradialgradientbrush"></a><a name="_dtorcd2dradialgradientbrush"></a> CD2DRadialGradientBrush:: ~ CD2DRadialGradientBrush

Деструктор Вызывается при уничтожении объекта кисти радиального градиента D2D.

```
virtual ~CD2DRadialGradientBrush();
```

## <a name="cd2dradialgradientbrushattach"></a><a name="attach"></a> CD2DRadialGradientBrush:: Attach

Присоединяет существующий интерфейс ресурсов к объекту

```cpp
void Attach(ID2D1RadialGradientBrush* pResource);
```

### <a name="parameters"></a>Параметры

*исходный код*<br/>
Существующий интерфейс ресурсов. Не может иметь значение NULL

## <a name="cd2dradialgradientbrushcd2dradialgradientbrush"></a><a name="cd2dradialgradientbrush"></a> CD2DRadialGradientBrush::CD2DRadialGradientBrush

Конструирует объект CD2DLinearGradientBrush.

```
CD2DRadialGradientBrush(
    CRenderTarget* pParentTarget,
    const D2D1_GRADIENT_STOP* gradientStops,
    UINT gradientStopsCount,
    D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES RadialGradientBrushProperties,
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

*радиалградиентбрушпропертиес*<br/>
Центр, смещение источника градиента и x-радиус и y-радиус градиента кисти.

*колоринтерполатионгамма*<br/>
Пространство, в котором выполняется интерполяция цветов между преостановками градиента.

*екстендмоде*<br/>
Поведение градиента за пределами нормализованного диапазона [0, 1].

*пбрушпропертиес*<br/>
Указатель на непрозрачность и Преобразование кисти.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

## <a name="cd2dradialgradientbrushcreate"></a><a name="create"></a> CD2DRadialGradientBrush:: Create

Создает CD2DRadialGradientBrush.

```
virtual HRESULT Create(CRenderTarget* pRenderTarget);
```

### <a name="parameters"></a>Параметры

*прендертаржет*<br/>
Указатель на целевой объект прорисовки.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dradialgradientbrushdestroy"></a><a name="destroy"></a> CD2DRadialGradientBrush::D естрой

Уничтожает объект CD2DRadialGradientBrush.

```
virtual void Destroy();
```

## <a name="cd2dradialgradientbrushdetach"></a><a name="detach"></a> CD2DRadialGradientBrush::D етач

Отсоединяет интерфейс ресурса от объекта

```
ID2D1RadialGradientBrush* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный интерфейс ресурсов.

## <a name="cd2dradialgradientbrushget"></a><a name="get"></a> CD2DRadialGradientBrush:: Get

Возвращает интерфейс ID2D1RadialGradientBrush

```
ID2D1RadialGradientBrush* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1RadialGradientBrush или значение NULL, если объект еще не инициализирован.

## <a name="cd2dradialgradientbrushgetcenter"></a><a name="getcenter"></a> CD2DRadialGradientBrush:: выровнять

Получает центр эллипса градиента

```
CD2DPointF GetCenter() const;
```

### <a name="return-value"></a>Возвращаемое значение

Центр эллипса градиента. Это значение выражается в пространстве координат кисти.

## <a name="cd2dradialgradientbrushgetgradientoriginoffset"></a><a name="getgradientoriginoffset"></a> CD2DRadialGradientBrush:: Жетградиенторигиноффсет

Получает смещение начала градиента относительно центра эллипса.

```
CD2DPointF GetGradientOriginOffset() const;
```

### <a name="return-value"></a>Возвращаемое значение

Смещение начала градиента от центра эллипса градиента. Это значение выражается в пространстве координат кисти.

## <a name="cd2dradialgradientbrushgetradiusx"></a><a name="getradiusx"></a> CD2DRadialGradientBrush:: Жетрадиускс

Получает x-радиус эллипса

```
FLOAT GetRadiusX() const;
```

### <a name="return-value"></a>Возвращаемое значение

Радиус эллипса по оси x. Это значение выражается в пространстве координат кисти.

## <a name="cd2dradialgradientbrushgetradiusy"></a><a name="getradiusy"></a> CD2DRadialGradientBrush:: радиус

Получает y-радиус эллипса

```
FLOAT GetRadiusY() const;
```

### <a name="return-value"></a>Возвращаемое значение

Y-радиус эллипса градиента. Это значение выражается в пространстве координат кисти.

## <a name="cd2dradialgradientbrushm_pradialgradientbrush"></a><a name="m_pradialgradientbrush"></a> CD2DRadialGradientBrush:: m_pRadialGradientBrush

Указатель на ID2D1RadialGradientBrush.

```
ID2D1RadialGradientBrush* m_pRadialGradientBrush;
```

## <a name="cd2dradialgradientbrushm_radialgradientbrushproperties"></a><a name="m_radialgradientbrushproperties"></a> CD2DRadialGradientBrush:: m_RadialGradientBrushProperties

Центр, смещение источника градиента и x-радиус и y-радиус градиента кисти.

```
D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES m_RadialGradientBrushProperties;
```

## <a name="cd2dradialgradientbrushoperator-id2d1radialgradientbrush"></a><a name="operator_id2d1radialgradientbrush_star"></a> CD2DRadialGradientBrush:: operator ID2D1RadialGradientBrush *

Возвращает интерфейс ID2D1RadialGradientBrush

```
operator ID2D1RadialGradientBrush*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1RadialGradientBrush или значение NULL, если объект еще не инициализирован.

## <a name="cd2dradialgradientbrushsetcenter"></a><a name="setcenter"></a> CD2DRadialGradientBrush:: Сетцентер

Задает центр эллипса градиента в пространстве координат кисти

```cpp
void SetCenter(CD2DPointF point);
```

### <a name="parameters"></a>Параметры

*точки*<br/>
Центр эллипса градиента в пространстве координат кисти

## <a name="cd2dradialgradientbrushsetgradientoriginoffset"></a><a name="setgradientoriginoffset"></a> CD2DRadialGradientBrush:: Сетградиенторигиноффсет

Задает смещение начала градиента относительно центра эллипса

```cpp
void SetGradientOriginOffset(CD2DPointF gradientOriginOffset);
```

### <a name="parameters"></a>Параметры

*градиенторигиноффсет*<br/>
Смещение начала градиента от центра эллипса

## <a name="cd2dradialgradientbrushsetradiusx"></a><a name="setradiusx"></a> CD2DRadialGradientBrush:: Сетрадиускс

Задает радиус эллипса по оси x в пространстве координат кисти

```cpp
void SetRadiusX(FLOAT radiusX);
```

### <a name="parameters"></a>Параметры

*radiusX*<br/>
Радиус эллипса по оси x. Это значение находится в координатной области кисти

## <a name="cd2dradialgradientbrushsetradiusy"></a><a name="setradiusy"></a> CD2DRadialGradientBrush:: Сетрадиуси

Задает y-радиус эллипса в пространстве координат кисти

```cpp
void SetRadiusY(FLOAT radiusY);
```

### <a name="parameters"></a>Параметры

*radiusY*<br/>
Y-радиус эллипса градиента. Это значение находится в координатной области кисти

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
