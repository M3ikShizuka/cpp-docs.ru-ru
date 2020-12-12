---
description: 'Дополнительные сведения о: CD2DLinearGradientBrush Class'
title: Класс CD2DLinearGradientBrush
ms.date: 11/04/2016
f1_keywords:
- CD2DLinearGradientBrush
- AFXRENDERTARGET/CD2DLinearGradientBrush
- AFXRENDERTARGET/CD2DLinearGradientBrush::CD2DLinearGradientBrush
- AFXRENDERTARGET/CD2DLinearGradientBrush::Attach
- AFXRENDERTARGET/CD2DLinearGradientBrush::Create
- AFXRENDERTARGET/CD2DLinearGradientBrush::Destroy
- AFXRENDERTARGET/CD2DLinearGradientBrush::Detach
- AFXRENDERTARGET/CD2DLinearGradientBrush::Get
- AFXRENDERTARGET/CD2DLinearGradientBrush::GetEndPoint
- AFXRENDERTARGET/CD2DLinearGradientBrush::GetStartPoint
- AFXRENDERTARGET/CD2DLinearGradientBrush::SetEndPoint
- AFXRENDERTARGET/CD2DLinearGradientBrush::SetStartPoint
- AFXRENDERTARGET/CD2DLinearGradientBrush::m_LinearGradientBrushProperties
- AFXRENDERTARGET/CD2DLinearGradientBrush::m_pLinearGradientBrush
helpviewer_keywords:
- CD2DLinearGradientBrush [MFC], CD2DLinearGradientBrush
- CD2DLinearGradientBrush [MFC], Attach
- CD2DLinearGradientBrush [MFC], Create
- CD2DLinearGradientBrush [MFC], Destroy
- CD2DLinearGradientBrush [MFC], Detach
- CD2DLinearGradientBrush [MFC], Get
- CD2DLinearGradientBrush [MFC], GetEndPoint
- CD2DLinearGradientBrush [MFC], GetStartPoint
- CD2DLinearGradientBrush [MFC], SetEndPoint
- CD2DLinearGradientBrush [MFC], SetStartPoint
- CD2DLinearGradientBrush [MFC], m_LinearGradientBrushProperties
- CD2DLinearGradientBrush [MFC], m_pLinearGradientBrush
ms.assetid: d4be9ff9-0ea8-45e6-9b8d-f3bc5673cbac
ms.openlocfilehash: b133abe796e609a44d1ebe35a6e6e969c8ee2a68
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97180336"
---
# <a name="cd2dlineargradientbrush-class"></a>Класс CD2DLinearGradientBrush

Оболочка для ID2D1LinearGradientBrush.

## <a name="syntax"></a>Синтаксис

```
class CD2DLinearGradientBrush : public CD2DGradientBrush;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DLinearGradientBrush:: CD2DLinearGradientBrush](#cd2dlineargradientbrush)|Конструирует объект CD2DLinearGradientBrush.|
|[CD2DLinearGradientBrush:: ~ CD2DLinearGradientBrush](#_dtorcd2dlineargradientbrush)|Деструктор Вызывается при уничтожении объекта кисти линейного градиента D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DLinearGradientBrush:: Attach](#attach)|Присоединяет существующий интерфейс ресурсов к объекту|
|[CD2DLinearGradientBrush:: Create](#create)|Создает CD2DLinearGradientBrush. (Переопределяет [CD2DResource:: Create](../../mfc/reference/cd2dresource-class.md#create).)|
|[CD2DLinearGradientBrush::D естрой](#destroy)|Уничтожает объект CD2DLinearGradientBrush. (Переопределяет [CD2DGradientBrush::D естрой](../../mfc/reference/cd2dgradientbrush-class.md#destroy).)|
|[CD2DLinearGradientBrush::D етач](#detach)|Отсоединяет интерфейс ресурса от объекта|
|[CD2DLinearGradientBrush:: Get](#get)|Возвращает интерфейс ID2D1LinearGradientBrush|
|[CD2DLinearGradientBrush:: наendpoint](#getendpoint)|Получает конечные координаты линейного градиента|
|[CD2DLinearGradientBrush:: Жетстартпоинт](#getstartpoint)|Получает начальные координаты линейного градиента|
|[CD2DLinearGradientBrush:: Сетендпоинт](#setendpoint)|Задает конечные координаты линейного градиента в пространстве координат кисти|
|[CD2DLinearGradientBrush:: Сетстартпоинт](#setstartpoint)|Задает начальные координаты линейного градиента в пространстве координат кисти|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DLinearGradientBrush:: operator ID2D1LinearGradientBrush *](#operator_id2d1lineargradientbrush_star)|Возвращает интерфейс ID2D1LinearGradientBrush|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DLinearGradientBrush:: m_LinearGradientBrushProperties](#m_lineargradientbrushproperties)|Начальная и конечная точки градиента.|
|[CD2DLinearGradientBrush:: m_pLinearGradientBrush](#m_plineargradientbrush)|Указатель на ID2D1LinearGradientBrush.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

[CD2DBrush](../../mfc/reference/cd2dbrush-class.md)

[CD2DGradientBrush](../../mfc/reference/cd2dgradientbrush-class.md)

`CD2DLinearGradientBrush`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dlineargradientbrushcd2dlineargradientbrush"></a><a name="_dtorcd2dlineargradientbrush"></a> CD2DLinearGradientBrush:: ~ CD2DLinearGradientBrush

Деструктор Вызывается при уничтожении объекта кисти линейного градиента D2D.

```
virtual ~CD2DLinearGradientBrush();
```

## <a name="cd2dlineargradientbrushattach"></a><a name="attach"></a> CD2DLinearGradientBrush:: Attach

Присоединяет существующий интерфейс ресурсов к объекту

```cpp
void Attach(ID2D1LinearGradientBrush* pResource);
```

### <a name="parameters"></a>Параметры

*исходный код*<br/>
Существующий интерфейс ресурсов. Не может иметь значение NULL

## <a name="cd2dlineargradientbrushcd2dlineargradientbrush"></a><a name="cd2dlineargradientbrush"></a> CD2DLinearGradientBrush:: CD2DLinearGradientBrush

Конструирует объект CD2DLinearGradientBrush.

```
CD2DLinearGradientBrush(
    CRenderTarget* pParentTarget,
    const D2D1_GRADIENT_STOP* gradientStops,
    UINT gradientStopsCount,
    D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES LinearGradientBrushProperties,
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

*линеарградиентбрушпропертиес*<br/>
Начальная и конечная точки градиента.

*колоринтерполатионгамма*<br/>
Пространство, в котором выполняется интерполяция цветов между преостановками градиента.

*екстендмоде*<br/>
Поведение градиента за пределами нормализованного диапазона [0, 1].

*пбрушпропертиес*<br/>
Указатель на непрозрачность и Преобразование кисти.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

## <a name="cd2dlineargradientbrushcreate"></a><a name="create"></a> CD2DLinearGradientBrush:: Create

Создает CD2DLinearGradientBrush.

```
virtual HRESULT Create(CRenderTarget* pRenderTarget);
```

### <a name="parameters"></a>Параметры

*прендертаржет*<br/>
Указатель на целевой объект прорисовки.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dlineargradientbrushdestroy"></a><a name="destroy"></a> CD2DLinearGradientBrush::D естрой

Уничтожает объект CD2DLinearGradientBrush.

```
virtual void Destroy();
```

## <a name="cd2dlineargradientbrushdetach"></a><a name="detach"></a> CD2DLinearGradientBrush::D етач

Отсоединяет интерфейс ресурса от объекта

```
ID2D1LinearGradientBrush* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный интерфейс ресурсов.

## <a name="cd2dlineargradientbrushget"></a><a name="get"></a> CD2DLinearGradientBrush:: Get

Возвращает интерфейс ID2D1LinearGradientBrush

```
ID2D1LinearGradientBrush* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1LinearGradientBrush или значение NULL, если объект еще не инициализирован.

## <a name="cd2dlineargradientbrushgetendpoint"></a><a name="getendpoint"></a> CD2DLinearGradientBrush:: наendpoint

Получает конечные координаты линейного градиента

```
CD2DPointF GetEndPoint() const;
```

### <a name="return-value"></a>Возвращаемое значение

Завершающие двухмерные координаты линейного градиента в пространстве координат кисти

## <a name="cd2dlineargradientbrushgetstartpoint"></a><a name="getstartpoint"></a> CD2DLinearGradientBrush:: Жетстартпоинт

Получает начальные координаты линейного градиента

```
CD2DPointF GetStartPoint() const;
```

### <a name="return-value"></a>Возвращаемое значение

Начальные двухмерные координаты линейного градиента в пространстве координат кисти

## <a name="cd2dlineargradientbrushm_lineargradientbrushproperties"></a><a name="m_lineargradientbrushproperties"></a> CD2DLinearGradientBrush:: m_LinearGradientBrushProperties

Начальная и конечная точки градиента.

```
D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES m_LinearGradientBrushProperties;
```

## <a name="cd2dlineargradientbrushm_plineargradientbrush"></a><a name="m_plineargradientbrush"></a> CD2DLinearGradientBrush:: m_pLinearGradientBrush

Указатель на ID2D1LinearGradientBrush.

```
ID2D1LinearGradientBrush* m_pLinearGradientBrush;
```

## <a name="cd2dlineargradientbrushoperator-id2d1lineargradientbrush"></a><a name="operator_id2d1lineargradientbrush_star"></a> CD2DLinearGradientBrush:: operator ID2D1LinearGradientBrush *

Возвращает интерфейс ID2D1LinearGradientBrush

```
operator ID2D1LinearGradientBrush*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1LinearGradientBrush или значение NULL, если объект еще не инициализирован.

## <a name="cd2dlineargradientbrushsetendpoint"></a><a name="setendpoint"></a> CD2DLinearGradientBrush:: Сетендпоинт

Задает конечные координаты линейного градиента в пространстве координат кисти

```cpp
void SetEndPoint(CD2DPointF point);
```

### <a name="parameters"></a>Параметры

*точки*<br/>
Завершающие двухмерные координаты линейного градиента в пространстве координат кисти

## <a name="cd2dlineargradientbrushsetstartpoint"></a><a name="setstartpoint"></a> CD2DLinearGradientBrush:: Сетстартпоинт

Задает начальные координаты линейного градиента в пространстве координат кисти

```cpp
void SetStartPoint(CD2DPointF point);
```

### <a name="parameters"></a>Параметры

*точки*<br/>
Начальные двухмерные координаты линейного градиента в пространстве координат кисти

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
