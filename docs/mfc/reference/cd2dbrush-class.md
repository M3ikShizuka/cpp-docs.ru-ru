---
description: 'Дополнительные сведения о: CD2DBrush Class'
title: Класс CD2DBrush
ms.date: 11/04/2016
f1_keywords:
- CD2DBrush
- AFXRENDERTARGET/CD2DBrush
- AFXRENDERTARGET/CD2DBrush::CD2DBrush
- AFXRENDERTARGET/CD2DBrush::Attach
- AFXRENDERTARGET/CD2DBrush::Destroy
- AFXRENDERTARGET/CD2DBrush::Detach
- AFXRENDERTARGET/CD2DBrush::Get
- AFXRENDERTARGET/CD2DBrush::GetOpacity
- AFXRENDERTARGET/CD2DBrush::GetTransform
- AFXRENDERTARGET/CD2DBrush::IsValid
- AFXRENDERTARGET/CD2DBrush::SetOpacity
- AFXRENDERTARGET/CD2DBrush::SetTransform
- AFXRENDERTARGET/CD2DBrush::m_pBrush
- AFXRENDERTARGET/CD2DBrush::m_pBrushProperties
helpviewer_keywords:
- CD2DBrush [MFC], CD2DBrush
- CD2DBrush [MFC], Attach
- CD2DBrush [MFC], Destroy
- CD2DBrush [MFC], Detach
- CD2DBrush [MFC], Get
- CD2DBrush [MFC], GetOpacity
- CD2DBrush [MFC], GetTransform
- CD2DBrush [MFC], IsValid
- CD2DBrush [MFC], SetOpacity
- CD2DBrush [MFC], SetTransform
- CD2DBrush [MFC], m_pBrush
- CD2DBrush [MFC], m_pBrushProperties
ms.assetid: 0d2c0857-2261-48a8-8ee0-a88cbf08499a
ms.openlocfilehash: 6d19601258951a297a734aa304e2a22c98baf5c9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227576"
---
# <a name="cd2dbrush-class"></a>Класс CD2DBrush

Оболочка для ID2D1Brush.

## <a name="syntax"></a>Синтаксис

```
class CD2DBrush : public CD2DResource;
```

## <a name="members"></a>Члены

### <a name="protected-constructors"></a>Защищенные конструкторы

|Имя|Описание|
|----------|-----------------|
|[CD2DBrush::CD2DBrush](#cd2dbrush)|Конструирует объект CD2DBrush.|
|[CD2DBrush:: ~ CD2DBrush](#_dtorcd2dbrush)|Деструктор Вызывается при уничтожении объекта кисти D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DBrush:: Attach](#attach)|Присоединяет существующий интерфейс ресурсов к объекту|
|[CD2DBrush::D естрой](#destroy)|Уничтожает объект CD2DBrush. (Переопределяет [CD2DResource::D естрой](../../mfc/reference/cd2dresource-class.md#destroy).)|
|[CD2DBrush::D етач](#detach)|Отсоединяет интерфейс ресурса от объекта|
|[CD2DBrush:: Get](#get)|Возвращает интерфейс ID2D1Brush|
|[CD2DBrush:: Opacity](#getopacity)|Возвращает степень прозрачности этой кисти|
|[CD2DBrush:: Transform](#gettransform)|Возвращает текущее преобразование целевого объекта прорисовки|
|[CD2DBrush:: IsValid](#isvalid)|Проверяет допустимость ресурса (переопределяет [CD2DResource:: IsValid](../../mfc/reference/cd2dresource-class.md#isvalid).)|
|[CD2DBrush:: СетопаЦити](#setopacity)|Задает степень прозрачности этой кисти|
|[CD2DBrush:: Сеттрансформ](#settransform)|Применяет указанное преобразование к целевому объекту прорисовки, заменяя существующее преобразование. Все последующие операции рисования происходят в преобразованном пространстве|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DBrush:: operator ID2D1Brush *](#operator_id2d1brush_star)|Возвращает интерфейс ID2D1Brush|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DBrush:: m_pBrush](#m_pbrush)|Хранит указатель на объект ID2D1Brush.|
|[CD2DBrush:: m_pBrushProperties](#m_pbrushproperties)|Свойства кисти.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

`CD2DBrush`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dbrushcd2dbrush"></a><a name="_dtorcd2dbrush"></a> CD2DBrush:: ~ CD2DBrush

Деструктор Вызывается при уничтожении объекта кисти D2D.

```
virtual ~CD2DBrush();
```

## <a name="cd2dbrushattach"></a><a name="attach"></a> CD2DBrush:: Attach

Присоединяет существующий интерфейс ресурсов к объекту.

```cpp
void Attach(ID2D1Brush* pResource);
```

### <a name="parameters"></a>Параметры

*исходный код*<br/>
Существующий интерфейс ресурсов. Не может быть NULL.

## <a name="cd2dbrushcd2dbrush"></a><a name="cd2dbrush"></a> CD2DBrush::CD2DBrush

Конструирует объект CD2DBrush.

```
CD2DBrush(
    CRenderTarget* pParentTarget,
    CD2DBrushProperties* pBrushProperties = NULL,
    BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*пбрушпропертиес*<br/>
Указатель на непрозрачность и Преобразование кисти.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

## <a name="cd2dbrushdestroy"></a><a name="destroy"></a> CD2DBrush::D естрой

Уничтожает объект CD2DBrush.

```
virtual void Destroy();
```

## <a name="cd2dbrushdetach"></a><a name="detach"></a> CD2DBrush::D етач

Отсоединяет интерфейс ресурса от объекта.

```
ID2D1Brush* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный интерфейс ресурсов.

## <a name="cd2dbrushget"></a><a name="get"></a> CD2DBrush:: Get

Возвращает интерфейс ID2D1Brush

```
ID2D1Brush* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1Brush или значение NULL, если объект еще не инициализирован.

## <a name="cd2dbrushgetopacity"></a><a name="getopacity"></a> CD2DBrush:: Opacity

Возвращает степень прозрачности этой кисти

```
FLOAT GetOpacity() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение от 0 до 1, указывающее на непрозрачность кисти. Это значение является постоянным множителем, который линейно масштабирует альфа-значение всех пикселов, заполненных кистью. Значения непрозрачности записываются в диапазоне от 0 до 1, прежде чем они будут умножены вместе.

## <a name="cd2dbrushgettransform"></a><a name="gettransform"></a> CD2DBrush:: Transform

Возвращает текущее преобразование целевого объекта прорисовки

```cpp
void GetTransform(D2D1_MATRIX_3X2_F* transform) const;
```

### <a name="parameters"></a>Параметры

*Преобразует*<br/>
При возврате содержит текущее преобразование целевого объекта отрисовки. Этот параметр передается неинициализированным.

## <a name="cd2dbrushisvalid"></a><a name="isvalid"></a> CD2DBrush:: IsValid

Проверка действительности ресурсов

```
virtual BOOL IsValid() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если ресурс является допустимым; в противном случае — FALSE.

## <a name="cd2dbrushm_pbrush"></a><a name="m_pbrush"></a> CD2DBrush:: m_pBrush

Хранит указатель на объект ID2D1Brush.

```
ID2D1Brush* m_pBrush;
```

## <a name="cd2dbrushm_pbrushproperties"></a><a name="m_pbrushproperties"></a> CD2DBrush:: m_pBrushProperties

Свойства кисти.

```
CD2DBrushProperties* m_pBrushProperties;
```

## <a name="cd2dbrushoperator-id2d1brush"></a><a name="operator_id2d1brush_star"></a> CD2DBrush:: operator ID2D1Brush *

Возвращает интерфейс ID2D1Brush

```
operator ID2D1Brush*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1Brush или значение NULL, если объект еще не инициализирован.

## <a name="cd2dbrushsetopacity"></a><a name="setopacity"></a> CD2DBrush:: СетопаЦити

Задает степень прозрачности этой кисти

```cpp
void SetOpacity(FLOAT opacity);
```

### <a name="parameters"></a>Параметры

*данной*<br/>
Значение от 0 до 1, указывающее на непрозрачность кисти. Это значение является постоянным множителем, который линейно масштабирует альфа-значение всех пикселов, заполненных кистью. Значения непрозрачности записываются в диапазоне от 0 до 1, прежде чем они будут умножены вместе.

## <a name="cd2dbrushsettransform"></a><a name="settransform"></a> CD2DBrush:: Сеттрансформ

Применяет указанное преобразование к целевому объекту прорисовки, заменяя существующее преобразование. Все последующие операции рисования происходят в преобразованном пространстве.

```cpp
void SetTransform(const D2D1_MATRIX_3X2_F* transform);
```

### <a name="parameters"></a>Параметры

*Преобразует*<br/>
Преобразование, применяемое к целевому объекту прорисовки

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
