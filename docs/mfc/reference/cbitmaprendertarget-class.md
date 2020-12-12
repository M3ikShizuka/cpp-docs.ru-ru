---
description: 'Дополнительные сведения о: Кбитмапрендертаржет Class'
title: Класс CBitmapRenderTarget
ms.date: 11/04/2016
f1_keywords:
- CBitmapRenderTarget
- AFXRENDERTARGET/CBitmapRenderTarget
- AFXRENDERTARGET/CBitmapRenderTarget::CBitmapRenderTarget
- AFXRENDERTARGET/CBitmapRenderTarget::Attach
- AFXRENDERTARGET/CBitmapRenderTarget::Detach
- AFXRENDERTARGET/CBitmapRenderTarget::GetBitmap
- AFXRENDERTARGET/CBitmapRenderTarget::GetBitmapRenderTarget
- AFXRENDERTARGET/CBitmapRenderTarget::m_pBitmapRenderTarget
helpviewer_keywords:
- CBitmapRenderTarget [MFC], CBitmapRenderTarget
- CBitmapRenderTarget [MFC], Attach
- CBitmapRenderTarget [MFC], Detach
- CBitmapRenderTarget [MFC], GetBitmap
- CBitmapRenderTarget [MFC], GetBitmapRenderTarget
- CBitmapRenderTarget [MFC], m_pBitmapRenderTarget
ms.assetid: c89a4437-812e-4943-acb2-b429a04cc4d2
ms.openlocfilehash: a7987651c988dcf7fcd4c4decf4a2bd474ab8619
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97122685"
---
# <a name="cbitmaprendertarget-class"></a>Класс CBitmapRenderTarget

Оболочка для ID2D1BitmapRenderTarget.

## <a name="syntax"></a>Синтаксис

```
class CBitmapRenderTarget : public CRenderTarget;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кбитмапрендертаржет:: Кбитмапрендертаржет](#cbitmaprendertarget)|Конструирует объект Кбитмапрендертаржет.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кбитмапрендертаржет:: Attach](#attach)|Присоединяет существующий интерфейс целевого объекта отрисовки к объекту|
|[Кбитмапрендертаржет::D етач](#detach)|Отсоединяет целевой интерфейс прорисовки от объекта|
|[Кбитмапрендертаржет::/Bitmap](#getbitmap)|Извлекает точечный рисунок для этого целевого объекта прорисовки. Возвращаемый точечный рисунок можно использовать для операций рисования.|
|[Кбитмапрендертаржет:: Жетбитмапрендертаржет](#getbitmaprendertarget)|Возвращает интерфейс ID2D1BitmapRenderTarget|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Кбитмапрендертаржет:: operator ID2D1BitmapRenderTarget *](#operator_id2d1bitmaprendertarget_star)|Возвращает интерфейс ID2D1BitmapRenderTarget|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Кбитмапрендертаржет:: m_pBitmapRenderTarget](#m_pbitmaprendertarget)|Указатель на объект ID2D1BitmapRenderTarget.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[крендертаржет](../../mfc/reference/crendertarget-class.md)

`CBitmapRenderTarget`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cbitmaprendertargetattach"></a><a name="attach"></a> Кбитмапрендертаржет:: Attach

Присоединяет существующий интерфейс целевого объекта отрисовки к объекту

```cpp
void Attach(ID2D1BitmapRenderTarget* pTarget);
```

### <a name="parameters"></a>Параметры

*птаржет*<br/>
Существующий интерфейс целевого объекта рендеринга. Не может иметь значение NULL

## <a name="cbitmaprendertargetcbitmaprendertarget"></a><a name="cbitmaprendertarget"></a> Кбитмапрендертаржет:: Кбитмапрендертаржет

Конструирует объект Кбитмапрендертаржет.

```
CBitmapRenderTarget();
```

## <a name="cbitmaprendertargetdetach"></a><a name="detach"></a> Кбитмапрендертаржет::D етач

Отсоединяет целевой интерфейс прорисовки от объекта

```
ID2D1BitmapRenderTarget* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный целевой интерфейс рендеринга.

## <a name="cbitmaprendertargetgetbitmap"></a><a name="getbitmap"></a> Кбитмапрендертаржет::/Bitmap

Извлекает точечный рисунок для этого целевого объекта прорисовки. Возвращаемый точечный рисунок можно использовать для операций рисования.

```
BOOL GetBitmap(CD2DBitmap& bitmap);
```

### <a name="parameters"></a>Параметры

*bitmap*<br/>
При возврате из этого метода содержит допустимый точечный рисунок для этого целевого объекта отрисовки. Это растровое изображение можно использовать для операций рисования.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cbitmaprendertargetgetbitmaprendertarget"></a><a name="getbitmaprendertarget"></a> Кбитмапрендертаржет:: Жетбитмапрендертаржет

Возвращает интерфейс ID2D1BitmapRenderTarget

```
ID2D1BitmapRenderTarget* GetBitmapRenderTarget();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1BitmapRenderTarget или значение NULL, если объект еще не инициализирован.

## <a name="cbitmaprendertargetm_pbitmaprendertarget"></a><a name="m_pbitmaprendertarget"></a> Кбитмапрендертаржет:: m_pBitmapRenderTarget

Указатель на объект ID2D1BitmapRenderTarget.

```
ID2D1BitmapRenderTarget* m_pBitmapRenderTarget;
```

## <a name="cbitmaprendertargetoperator-id2d1bitmaprendertarget"></a><a name="operator_id2d1bitmaprendertarget_star"></a> Кбитмапрендертаржет:: operator ID2D1BitmapRenderTarget *

Возвращает интерфейс ID2D1BitmapRenderTarget

```
operator ID2D1BitmapRenderTarget*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1BitmapRenderTarget или значение NULL, если объект еще не инициализирован.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
