---
description: 'Дополнительные сведения о: CD2DSolidColorBrush Class'
title: Класс CD2DSolidColorBrush
ms.date: 03/27/2019
f1_keywords:
- CD2DSolidColorBrush
- AFXRENDERTARGET/CD2DSolidColorBrush
- AFXRENDERTARGET/CD2DSolidColorBrush::CD2DSolidColorBrush
- AFXRENDERTARGET/CD2DSolidColorBrush::Attach
- AFXRENDERTARGET/CD2DSolidColorBrush::Create
- AFXRENDERTARGET/CD2DSolidColorBrush::Destroy
- AFXRENDERTARGET/CD2DSolidColorBrush::Detach
- AFXRENDERTARGET/CD2DSolidColorBrush::Get
- AFXRENDERTARGET/CD2DSolidColorBrush::GetColor
- AFXRENDERTARGET/CD2DSolidColorBrush::SetColor
- AFXRENDERTARGET/CD2DSolidColorBrush::m_colorSolid
- AFXRENDERTARGET/CD2DSolidColorBrush::m_pSolidColorBrush
helpviewer_keywords:
- CD2DSolidColorBrush [MFC], CD2DSolidColorBrush
- CD2DSolidColorBrush [MFC], Attach
- CD2DSolidColorBrush [MFC], Create
- CD2DSolidColorBrush [MFC], Destroy
- CD2DSolidColorBrush [MFC], Detach
- CD2DSolidColorBrush [MFC], Get
- CD2DSolidColorBrush [MFC], GetColor
- CD2DSolidColorBrush [MFC], SetColor
- CD2DSolidColorBrush [MFC], m_colorSolid
- CD2DSolidColorBrush [MFC], m_pSolidColorBrush
ms.assetid: d4506637-acce-4f74-8a9b-f0a45571a735
ms.openlocfilehash: 57df3732a3c4239af6d9121426aa272c6f58417d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97154608"
---
# <a name="cd2dsolidcolorbrush-class"></a>Класс CD2DSolidColorBrush

Оболочка для ID2D1SolidColorBrush.

## <a name="syntax"></a>Синтаксис

```
class CD2DSolidColorBrush : public CD2DBrush;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DSolidColorBrush::CD2DSolidColorBrush](#cd2dsolidcolorbrush)|Перегружен. Конструирует объект CD2DSolidColorBrush.|
|[CD2DSolidColorBrush:: ~ CD2DSolidColorBrush](#_dtorcd2dsolidcolorbrush)|Деструктор Вызывается при уничтожении твердого объекта кисти D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DSolidColorBrush:: Attach](#attach)|Присоединяет существующий интерфейс ресурсов к объекту|
|[CD2DSolidColorBrush:: Create](#create)|Создает CD2DSolidColorBrush. (Переопределяет [CD2DResource:: Create](../../mfc/reference/cd2dresource-class.md#create).)|
|[CD2DSolidColorBrush::D естрой](#destroy)|Уничтожает объект CD2DSolidColorBrush. (Переопределяет [CD2DBrush::D естрой](../../mfc/reference/cd2dbrush-class.md#destroy).)|
|[CD2DSolidColorBrush::D етач](#detach)|Отсоединяет интерфейс ресурса от объекта|
|[CD2DSolidColorBrush:: Get](#get)|Возвращает интерфейс ID2D1SolidColorBrush|
|[CD2DSolidColorBrush:: "Color"](#getcolor)|Получает цвет кисти сплошного цвета|
|[CD2DSolidColorBrush:: Сетколор](#setcolor)|Задает цвет кисти сплошного цвета|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DSolidColorBrush:: operator ID2D1SolidColorBrush *](#operator_id2d1solidcolorbrush_star)|Возвращает интерфейс ID2D1SolidColorBrush|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DSolidColorBrush:: m_colorSolid](#m_colorsolid)|Сплошной цвет кисти.|
|[CD2DSolidColorBrush:: m_pSolidColorBrush](#m_psolidcolorbrush)|Хранит указатель на объект ID2D1SolidColorBrush.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

[CD2DBrush](../../mfc/reference/cd2dbrush-class.md)

[CD2DSolidColorBrush](../../mfc/reference/cd2dsolidcolorbrush-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dsolidcolorbrushcd2dsolidcolorbrush"></a><a name="_dtorcd2dsolidcolorbrush"></a> CD2DSolidColorBrush:: ~ CD2DSolidColorBrush

Деструктор Вызывается при уничтожении твердого объекта кисти D2D.

```
virtual ~CD2DSolidColorBrush();
```

## <a name="cd2dsolidcolorbrushattach"></a><a name="attach"></a> CD2DSolidColorBrush:: Attach

Присоединяет существующий интерфейс ресурсов к объекту

```cpp
void Attach(ID2D1SolidColorBrush* pResource);
```

### <a name="parameters"></a>Параметры

*исходный код*<br/>
Существующий интерфейс ресурсов. Не может иметь значение NULL

## <a name="cd2dsolidcolorbrushcd2dsolidcolorbrush"></a><a name="cd2dsolidcolorbrush"></a> CD2DSolidColorBrush::CD2DSolidColorBrush

Конструирует объект CD2DSolidColorBrush.

```
CD2DSolidColorBrush(
    CRenderTarget* pParentTarget,
    D2D1_COLOR_F color,
    CD2DBrushProperties* pBrushProperties = NULL,
    BOOL bAutoDestroy = TRUE);

CD2DSolidColorBrush(
    CRenderTarget* pParentTarget,
    COLORREF color,
    int nAlpha = 255,
    CD2DBrushProperties* pBrushProperties = NULL,
    BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*color*<br/>
Красный, зеленый, синий и альфа-значения цвета кисти.

*пбрушпропертиес*<br/>
Указатель на непрозрачность и Преобразование кисти.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

*налфа*<br/>
Непрозрачность цвета кисти.

## <a name="cd2dsolidcolorbrushcreate"></a><a name="create"></a> CD2DSolidColorBrush:: Create

Создает CD2DSolidColorBrush.

```
virtual HRESULT Create(CRenderTarget* pRenderTarget);
```

### <a name="parameters"></a>Параметры

*прендертаржет*<br/>
Указатель на целевой объект прорисовки.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dsolidcolorbrushdestroy"></a><a name="destroy"></a> CD2DSolidColorBrush::D естрой

Уничтожает объект CD2DSolidColorBrush.

```
virtual void Destroy();
```

## <a name="cd2dsolidcolorbrushdetach"></a><a name="detach"></a> CD2DSolidColorBrush::D етач

Отсоединяет интерфейс ресурса от объекта

```
ID2D1SolidColorBrush* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный интерфейс ресурсов.

## <a name="cd2dsolidcolorbrushget"></a><a name="get"></a> CD2DSolidColorBrush:: Get

Возвращает интерфейс ID2D1SolidColorBrush

```
ID2D1SolidColorBrush* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1SolidColorBrush или значение NULL, если объект еще не инициализирован.

## <a name="cd2dsolidcolorbrushgetcolor"></a><a name="getcolor"></a> CD2DSolidColorBrush:: "Color"

Получает цвет кисти сплошного цвета

```
D2D1_COLOR_F GetColor() const;
```

### <a name="return-value"></a>Возвращаемое значение

Цвет кисти сплошного цвета

## <a name="cd2dsolidcolorbrushm_colorsolid"></a><a name="m_colorsolid"></a> CD2DSolidColorBrush:: m_colorSolid

Сплошной цвет кисти.

```
D2D1_COLOR_F m_colorSolid;
```

## <a name="cd2dsolidcolorbrushm_psolidcolorbrush"></a><a name="m_psolidcolorbrush"></a> CD2DSolidColorBrush:: m_pSolidColorBrush

Хранит указатель на объект ID2D1SolidColorBrush.

```
ID2D1SolidColorBrush* m_pSolidColorBrush;
```

## <a name="cd2dsolidcolorbrushoperator-id2d1solidcolorbrush"></a><a name="operator_id2d1solidcolorbrush_star"></a> CD2DSolidColorBrush:: operator ID2D1SolidColorBrush *

Возвращает интерфейс ID2D1SolidColorBrush

```
operator ID2D1SolidColorBrush*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1SolidColorBrush или значение NULL, если объект еще не инициализирован.

## <a name="cd2dsolidcolorbrushsetcolor"></a><a name="setcolor"></a> CD2DSolidColorBrush:: Сетколор

Задает цвет кисти сплошного цвета

```cpp
void SetColor(D2D1_COLOR_F color);
```

### <a name="parameters"></a>Параметры

*color*<br/>
Цвет кисти сплошного цвета

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
