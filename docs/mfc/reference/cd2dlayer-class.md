---
description: 'Дополнительные сведения о: CD2DLayer Class'
title: Класс CD2DLayer
ms.date: 11/04/2016
f1_keywords:
- CD2DLayer
- AFXRENDERTARGET/CD2DLayer
- AFXRENDERTARGET/CD2DLayer::CD2DLayer
- AFXRENDERTARGET/CD2DLayer::Attach
- AFXRENDERTARGET/CD2DLayer::Create
- AFXRENDERTARGET/CD2DLayer::Destroy
- AFXRENDERTARGET/CD2DLayer::Detach
- AFXRENDERTARGET/CD2DLayer::Get
- AFXRENDERTARGET/CD2DLayer::GetSize
- AFXRENDERTARGET/CD2DLayer::IsValid
- AFXRENDERTARGET/CD2DLayer::m_pLayer
helpviewer_keywords:
- CD2DLayer [MFC], CD2DLayer
- CD2DLayer [MFC], Attach
- CD2DLayer [MFC], Create
- CD2DLayer [MFC], Destroy
- CD2DLayer [MFC], Detach
- CD2DLayer [MFC], Get
- CD2DLayer [MFC], GetSize
- CD2DLayer [MFC], IsValid
- CD2DLayer [MFC], m_pLayer
ms.assetid: 2f96378e-66bb-40d1-9661-6afe324de3c1
ms.openlocfilehash: bd41cd591e6422c9434cd84d20cb6e5d778410bd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97306954"
---
# <a name="cd2dlayer-class"></a>Класс CD2DLayer

Оболочка для ID2D1Layer.

## <a name="syntax"></a>Синтаксис

```
class CD2DLayer : public CD2DResource;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DLayer::CD2DLayer](#cd2dlayer)|Конструирует объект CD2DLayer.|
|[CD2DLayer:: ~ CD2DLayer](#_dtorcd2dlayer)|Деструктор Вызывается при уничтожении объекта уровня D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DLayer:: Attach](#attach)|Присоединяет существующий интерфейс ресурсов к объекту|
|[CD2DLayer:: Create](#create)|Создает CD2DLayer. (Переопределяет [CD2DResource:: Create](../../mfc/reference/cd2dresource-class.md#create).)|
|[CD2DLayer::D естрой](#destroy)|Уничтожает объект CD2DLayer. (Переопределяет [CD2DResource::D естрой](../../mfc/reference/cd2dresource-class.md#destroy).)|
|[CD2DLayer::D етач](#detach)|Отсоединяет интерфейс ресурса от объекта|
|[CD2DLayer:: Get](#get)|Возвращает интерфейс ID2D1Layer|
|[CD2DLayer:: DataSize](#getsize)|Возвращает размер целевого объекта отрисовки в аппаратно-независимых пикселях|
|[CD2DLayer:: IsValid](#isvalid)|Проверяет допустимость ресурса (переопределяет [CD2DResource:: IsValid](../../mfc/reference/cd2dresource-class.md#isvalid).)|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DLayer:: operator ID2D1Layer *](#operator_id2d1layer_star)|Возвращает интерфейс ID2D1Layer|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DLayer:: m_pLayer](#m_player)|Хранит указатель на объект ID2D1Layer.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

`CD2DLayer`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dlayercd2dlayer"></a><a name="_dtorcd2dlayer"></a> CD2DLayer:: ~ CD2DLayer

Деструктор Вызывается при уничтожении объекта уровня D2D.

```
virtual ~CD2DLayer();
```

## <a name="cd2dlayerattach"></a><a name="attach"></a> CD2DLayer:: Attach

Присоединяет существующий интерфейс ресурсов к объекту

```cpp
void Attach(ID2D1Layer* pResource);
```

### <a name="parameters"></a>Параметры

*исходный код*<br/>
Существующий интерфейс ресурсов. Не может иметь значение NULL

## <a name="cd2dlayercd2dlayer"></a><a name="cd2dlayer"></a> CD2DLayer::CD2DLayer

Конструирует объект CD2DLayer.

```
CD2DLayer(
    CRenderTarget* pParentTarget,
    BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

## <a name="cd2dlayercreate"></a><a name="create"></a> CD2DLayer:: Create

Создает CD2DLayer.

```
virtual HRESULT Create(CRenderTarget* pRenderTarget);
```

### <a name="parameters"></a>Параметры

*прендертаржет*<br/>
Указатель на целевой объект прорисовки.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dlayerdestroy"></a><a name="destroy"></a> CD2DLayer::D естрой

Уничтожает объект CD2DLayer.

```
virtual void Destroy();
```

## <a name="cd2dlayerdetach"></a><a name="detach"></a> CD2DLayer::D етач

Отсоединяет интерфейс ресурса от объекта

```
ID2D1Layer* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный интерфейс ресурсов.

## <a name="cd2dlayerget"></a><a name="get"></a> CD2DLayer:: Get

Возвращает интерфейс ID2D1Layer

```
ID2D1Layer* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1Layer или значение NULL, если объект еще не инициализирован.

## <a name="cd2dlayergetsize"></a><a name="getsize"></a> CD2DLayer:: DataSize

Возвращает размер целевого объекта отрисовки в аппаратно-независимых пикселях

```
CD2DSizeF GetSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Текущий размер целевого объекта отрисовки в аппаратно-независимых пикселях

## <a name="cd2dlayerisvalid"></a><a name="isvalid"></a> CD2DLayer:: IsValid

Проверка действительности ресурсов

```
virtual BOOL IsValid() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если ресурс является допустимым; в противном случае — FALSE.

## <a name="cd2dlayerm_player"></a><a name="m_player"></a> CD2DLayer:: m_pLayer

Хранит указатель на объект ID2D1Layer.

```
ID2D1Layer* m_pLayer;
```

## <a name="cd2dlayeroperator-id2d1layer"></a><a name="operator_id2d1layer_star"></a> CD2DLayer:: operator ID2D1Layer *

Возвращает интерфейс ID2D1Layer

```
operator ID2D1Layer* ();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1Layer или значение NULL, если объект еще не инициализирован.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
