---
description: 'Дополнительные сведения о: CD2DBitmapBrush Class'
title: Класс CD2DBitmapBrush
ms.date: 11/04/2016
f1_keywords:
- CD2DBitmapBrush
- AFXRENDERTARGET/CD2DBitmapBrush
- AFXRENDERTARGET/CD2DBitmapBrush::CD2DBitmapBrush
- AFXRENDERTARGET/CD2DBitmapBrush::Attach
- AFXRENDERTARGET/CD2DBitmapBrush::Create
- AFXRENDERTARGET/CD2DBitmapBrush::Destroy
- AFXRENDERTARGET/CD2DBitmapBrush::Detach
- AFXRENDERTARGET/CD2DBitmapBrush::Get
- AFXRENDERTARGET/CD2DBitmapBrush::GetBitmap
- AFXRENDERTARGET/CD2DBitmapBrush::GetExtendModeX
- AFXRENDERTARGET/CD2DBitmapBrush::GetExtendModeY
- AFXRENDERTARGET/CD2DBitmapBrush::GetInterpolationMode
- AFXRENDERTARGET/CD2DBitmapBrush::SetBitmap
- AFXRENDERTARGET/CD2DBitmapBrush::SetExtendModeX
- AFXRENDERTARGET/CD2DBitmapBrush::SetExtendModeY
- AFXRENDERTARGET/CD2DBitmapBrush::SetInterpolationMode
- AFXRENDERTARGET/CD2DBitmapBrush::CommonInit
- AFXRENDERTARGET/CD2DBitmapBrush::m_pBitmap
- AFXRENDERTARGET/CD2DBitmapBrush::m_pBitmapBrush
- AFXRENDERTARGET/CD2DBitmapBrush::m_pBitmapBrushProperties
helpviewer_keywords:
- CD2DBitmapBrush [MFC], CD2DBitmapBrush
- CD2DBitmapBrush [MFC], Attach
- CD2DBitmapBrush [MFC], Create
- CD2DBitmapBrush [MFC], Destroy
- CD2DBitmapBrush [MFC], Detach
- CD2DBitmapBrush [MFC], Get
- CD2DBitmapBrush [MFC], GetBitmap
- CD2DBitmapBrush [MFC], GetExtendModeX
- CD2DBitmapBrush [MFC], GetExtendModeY
- CD2DBitmapBrush [MFC], GetInterpolationMode
- CD2DBitmapBrush [MFC], SetBitmap
- CD2DBitmapBrush [MFC], SetExtendModeX
- CD2DBitmapBrush [MFC], SetExtendModeY
- CD2DBitmapBrush [MFC], SetInterpolationMode
- CD2DBitmapBrush [MFC], CommonInit
- CD2DBitmapBrush [MFC], m_pBitmap
- CD2DBitmapBrush [MFC], m_pBitmapBrush
- CD2DBitmapBrush [MFC], m_pBitmapBrushProperties
ms.assetid: 46ebbe34-66e0-44c8-af1d-d129e851de5e
ms.openlocfilehash: a9d4c1955b1318ecb273482cd49025090bf97d3d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227589"
---
# <a name="cd2dbitmapbrush-class"></a>Класс CD2DBitmapBrush

Оболочка для ID2D1BitmapBrush.

## <a name="syntax"></a>Синтаксис

```
class CD2DBitmapBrush : public CD2DBrush;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DBitmapBrush:: CD2DBitmapBrush](#cd2dbitmapbrush)|Перегружен. Конструирует объект CD2DBitmapBrush из файла.|
|[CD2DBitmapBrush:: ~ CD2DBitmapBrush](#dtor)|Деструктор Вызывается при уничтожении объекта кисти точечного рисунка D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DBitmapBrush:: Attach](#attach)|Присоединяет существующий интерфейс ресурсов к объекту|
|[CD2DBitmapBrush:: Create](#create)|Создает CD2DBitmapBrush. (Переопределяет [CD2DResource:: Create](../../mfc/reference/cd2dresource-class.md#create).)|
|[CD2DBitmapBrush::D естрой](#destroy)|Уничтожает объект CD2DBitmapBrush. (Переопределяет [CD2DBrush::D естрой](../../mfc/reference/cd2dbrush-class.md#destroy).)|
|[CD2DBitmapBrush::D етач](#detach)|Отсоединяет интерфейс ресурса от объекта|
|[CD2DBitmapBrush:: Get](#get)|Возвращает интерфейс ID2D1BitmapBrush|
|[CD2DBitmapBrush::/Bitmap](#getbitmap)|Возвращает источник точечного рисунка, используемый этой кистью для рисования|
|[CD2DBitmapBrush:: Жетекстендмодекс](#getextendmodex)|Возвращает метод, с помощью которого кисть располагается по горизонтали в области, которые выходят за пределы его растрового изображения.|
|[CD2DBitmapBrush:: Жетекстендмодэй](#getextendmodey)|Возвращает метод, по которому кисть накладывается на вертикальное расположение областей, которые выходят за пределы его битового рисунка.|
|[CD2DBitmapBrush:: Жетинтерполатионмоде](#getinterpolationmode)|Возвращает метод интерполяции, используемый при масштабировании или повороте растрового изображения кисти.|
|[CD2DBitmapBrush:: Сетбитмап](#setbitmap)|Указывает источник точечного рисунка, используемый этой кистью для рисования|
|[CD2DBitmapBrush:: Сетекстендмодекс](#setextendmodex)|Указывает, как кисть горизонтально мозаики размещает области, которые выходят за пределы его растрового изображения|
|[CD2DBitmapBrush:: Сетекстендмодэй](#setextendmodey)|Указывает, как кисть накладывается на вертикальную плитку областей, которые выходят за пределы ее битов|
|[CD2DBitmapBrush:: Сетинтерполатионмоде](#setinterpolationmode)|Задает режим интерполяции, используемый при масштабировании или повороте растрового изображения кисти|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[CD2DBitmapBrush:: Коммонинит](#commoninit)|Инициализирует объект|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DBitmapBrush:: operator ID2D1BitmapBrush *](#operator_id2d1bitmapbrush_star)|Возвращает интерфейс ID2D1BitmapBrush|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DBitmapBrush:: m_pBitmap](#m_pbitmap)|Хранит указатель на объект CD2DBitmap.|
|[CD2DBitmapBrush:: m_pBitmapBrush](#m_pbitmapbrush)|Хранит указатель на объект ID2D1BitmapBrush.|
|[CD2DBitmapBrush:: m_pBitmapBrushProperties](#m_pbitmapbrushproperties)|Свойства кисти растрового изображения.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

[CD2DBrush](../../mfc/reference/cd2dbrush-class.md)

`CD2DBitmapBrush`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dbitmapbrushcd2dbitmapbrush"></a><a name="dtor"></a> CD2DBitmapBrush:: ~ CD2DBitmapBrush

Деструктор Вызывается при уничтожении объекта кисти точечного рисунка D2D.

```
virtual ~CD2DBitmapBrush();
```

## <a name="cd2dbitmapbrushattach"></a><a name="attach"></a> CD2DBitmapBrush:: Attach

Присоединяет существующий интерфейс ресурсов к объекту

```cpp
void Attach(ID2D1BitmapBrush* pResource);
```

### <a name="parameters"></a>Параметры

*исходный код*<br/>
Существующий интерфейс ресурсов. Не может иметь значение NULL

## <a name="cd2dbitmapbrushcd2dbitmapbrush"></a><a name="cd2dbitmapbrush"></a> CD2DBitmapBrush:: CD2DBitmapBrush

Конструирует объект CD2DBitmapBrush.

```
CD2DBitmapBrush(
    CRenderTarget* pParentTarget,
    D2D1_BITMAP_BRUSH_PROPERTIES* pBitmapBrushProperties = NULL,
    CD2DBrushProperties* pBrushProperties = NULL,
    BOOL bAutoDestroy = TRUE);

CD2DBitmapBrush(
    CRenderTarget* pParentTarget,
    UINT uiResID,
    LPCTSTR lpszType = NULL,
    CD2DSizeU sizeDest = CD2DSizeU(0, 0),
    D2D1_BITMAP_BRUSH_PROPERTIES* pBitmapBrushProperties = NULL,
    CD2DBrushProperties* pBrushProperties = NULL,
    BOOL bAutoDestroy = TRUE);

CD2DBitmapBrush(
    CRenderTarget* pParentTarget,
    LPCTSTR lpszImagePath,
    CD2DSizeU sizeDest = CD2DSizeU(0, 0),
    D2D1_BITMAP_BRUSH_PROPERTIES* pBitmapBrushProperties = NULL,
    CD2DBrushProperties* pBrushProperties = NULL,
    BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*пбитмапбрушпропертиес*<br/>
Указатель на режимы расширения и режим интерполяции для растровой кисти.

*пбрушпропертиес*<br/>
Указатель на непрозрачность и Преобразование кисти.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

*уиресид*<br/>
ИДЕНТИФИКАЦИОНный номер ресурса.

*лпсзтипе*<br/>
Указатель на строку, завершающуюся нулем, которая содержит тип ресурса.

*самый заданный размер*<br/>
Целевой размер точечного рисунка.

*лпсзимажепас*<br/>
Указатель на строку, завершающуюся нулем, которая содержит имя файла.

## <a name="cd2dbitmapbrushcommoninit"></a><a name="commoninit"></a> CD2DBitmapBrush:: Коммонинит

Инициализирует объект

```cpp
void CommonInit(D2D1_BITMAP_BRUSH_PROPERTIES* pBitmapBrushProperties);
```

### <a name="parameters"></a>Параметры

*пбитмапбрушпропертиес*<br/>
Указатель на свойства кисти растрового изображения.

## <a name="cd2dbitmapbrushcreate"></a><a name="create"></a> CD2DBitmapBrush:: Create

Создает CD2DBitmapBrush.

```
virtual HRESULT Create(CRenderTarget* pRenderTarget);
```

### <a name="parameters"></a>Параметры

*прендертаржет*<br/>
Указатель на целевой объект прорисовки.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dbitmapbrushdestroy"></a><a name="destroy"></a> CD2DBitmapBrush::D естрой

Уничтожает объект CD2DBitmapBrush.

```
virtual void Destroy();
```

## <a name="cd2dbitmapbrushdetach"></a><a name="detach"></a> CD2DBitmapBrush::D етач

Отсоединяет интерфейс ресурса от объекта

```
ID2D1BitmapBrush* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный интерфейс ресурсов.

## <a name="cd2dbitmapbrushget"></a><a name="get"></a> CD2DBitmapBrush:: Get

Возвращает интерфейс ID2D1BitmapBrush

```
ID2D1BitmapBrush* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1BitmapBrush или значение NULL, если объект еще не инициализирован.

## <a name="cd2dbitmapbrushgetbitmap"></a><a name="getbitmap"></a> CD2DBitmapBrush::/Bitmap

Возвращает источник точечного рисунка, используемый этой кистью для рисования

```
CD2DBitmap* GetBitmap();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на объект CD2DBitmap или значение NULL, если объект еще не инициализирован.

## <a name="cd2dbitmapbrushgetextendmodex"></a><a name="getextendmodex"></a> CD2DBitmapBrush:: Жетекстендмодекс

Возвращает метод, с помощью которого кисть располагается по горизонтали в области, которые выходят за пределы его растрового изображения.

```
D2D1_EXTEND_MODE GetExtendModeX() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение, указывающее, как кисть горизонтально мозаично отображает области, которые выходят за пределы его растрового изображения

## <a name="cd2dbitmapbrushgetextendmodey"></a><a name="getextendmodey"></a> CD2DBitmapBrush:: Жетекстендмодэй

Возвращает метод, по которому кисть накладывается на вертикальное расположение областей, которые выходят за пределы его битового рисунка.

```
D2D1_EXTEND_MODE GetExtendModeY() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение, указывающее, как кисть накладывается на вертикальное расположение областей, которые выходят за пределы его растрового изображения

## <a name="cd2dbitmapbrushgetinterpolationmode"></a><a name="getinterpolationmode"></a> CD2DBitmapBrush:: Жетинтерполатионмоде

Возвращает метод интерполяции, используемый при масштабировании или повороте растрового изображения кисти.

```
D2D1_BITMAP_INTERPOLATION_MODE GetInterpolationMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

Метод интерполяции, используемый при масштабировании или повороте растрового изображения кисти

## <a name="cd2dbitmapbrushm_pbitmap"></a><a name="m_pbitmap"></a> CD2DBitmapBrush:: m_pBitmap

Хранит указатель на объект CD2DBitmap.

```
CD2DBitmap* m_pBitmap;
```

## <a name="cd2dbitmapbrushm_pbitmapbrush"></a><a name="m_pbitmapbrush"></a> CD2DBitmapBrush:: m_pBitmapBrush

Хранит указатель на объект ID2D1BitmapBrush.

```
ID2D1BitmapBrush* m_pBitmapBrush;
```

## <a name="cd2dbitmapbrushm_pbitmapbrushproperties"></a><a name="m_pbitmapbrushproperties"></a> CD2DBitmapBrush:: m_pBitmapBrushProperties

Свойства кисти растрового изображения.

```
D2D1_BITMAP_BRUSH_PROPERTIES* m_pBitmapBrushProperties;
```

## <a name="cd2dbitmapbrushoperator-id2d1bitmapbrush"></a><a name="operator_id2d1bitmapbrush_star"></a> CD2DBitmapBrush:: operator ID2D1BitmapBrush *

Возвращает интерфейс ID2D1BitmapBrush

```
operator ID2D1BitmapBrush*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1BitmapBrush или значение NULL, если объект еще не инициализирован.

## <a name="cd2dbitmapbrushsetbitmap"></a><a name="setbitmap"></a> CD2DBitmapBrush:: Сетбитмап

Указывает источник точечного рисунка, используемый этой кистью для рисования

```cpp
void SetBitmap(CD2DBitmap* pBitmap);
```

### <a name="parameters"></a>Параметры

*пбитмап*<br/>
Источник точечного рисунка, используемый кистью

## <a name="cd2dbitmapbrushsetextendmodex"></a><a name="setextendmodex"></a> CD2DBitmapBrush:: Сетекстендмодекс

Указывает, как кисть горизонтально мозаики размещает области, которые выходят за пределы его растрового изображения

```cpp
void SetExtendModeX(D2D1_EXTEND_MODE extendModeX);
```

### <a name="parameters"></a>Параметры

*екстендмодекс*<br/>
Значение, указывающее, как кисть горизонтально мозаично отображает области, которые выходят за пределы его растрового изображения

## <a name="cd2dbitmapbrushsetextendmodey"></a><a name="setextendmodey"></a> CD2DBitmapBrush:: Сетекстендмодэй

Указывает, как кисть накладывается на вертикальную плитку областей, которые выходят за пределы ее битов

```cpp
void SetExtendModeY(D2D1_EXTEND_MODE extendModeY);
```

### <a name="parameters"></a>Параметры

*екстендмодэй*<br/>
Значение, указывающее, как кисть накладывается на вертикальное расположение областей, которые выходят за пределы его растрового изображения

## <a name="cd2dbitmapbrushsetinterpolationmode"></a><a name="setinterpolationmode"></a> CD2DBitmapBrush:: Сетинтерполатионмоде

Задает режим интерполяции, используемый при масштабировании или повороте растрового изображения кисти

```cpp
void SetInterpolationMode(D2D1_BITMAP_INTERPOLATION_MODE interpolationMode);
```

### <a name="parameters"></a>Параметры

*интерполатионмоде*<br/>
Режим интерполяции, используемый при масштабировании или повороте растрового изображения кисти

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
