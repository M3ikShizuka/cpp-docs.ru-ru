---
description: 'Дополнительные сведения о: Кдкрендертаржет Class'
title: Класс CDCRenderTarget
ms.date: 11/04/2016
f1_keywords:
- CDCRenderTarget
- AFXRENDERTARGET/CDCRenderTarget
- AFXRENDERTARGET/CDCRenderTarget::CDCRenderTarget
- AFXRENDERTARGET/CDCRenderTarget::Attach
- AFXRENDERTARGET/CDCRenderTarget::BindDC
- AFXRENDERTARGET/CDCRenderTarget::Create
- AFXRENDERTARGET/CDCRenderTarget::Detach
- AFXRENDERTARGET/CDCRenderTarget::GetDCRenderTarget
- AFXRENDERTARGET/CDCRenderTarget::m_pDCRenderTarget
helpviewer_keywords:
- CDCRenderTarget [MFC], CDCRenderTarget
- CDCRenderTarget [MFC], Attach
- CDCRenderTarget [MFC], BindDC
- CDCRenderTarget [MFC], Create
- CDCRenderTarget [MFC], Detach
- CDCRenderTarget [MFC], GetDCRenderTarget
- CDCRenderTarget [MFC], m_pDCRenderTarget
ms.assetid: aa8059c9-08e6-49e4-9b8c-00fa54077a61
ms.openlocfilehash: 3959321bbd6274c821b1f02be5962b23ec9dbc95
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185327"
---
# <a name="cdcrendertarget-class"></a>Класс CDCRenderTarget

Оболочка для ID2D1DCRenderTarget.

## <a name="syntax"></a>Синтаксис

```
class CDCRenderTarget : public CRenderTarget;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кдкрендертаржет:: Кдкрендертаржет](#cdcrendertarget)|Конструирует объект Кдкрендертаржет.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кдкрендертаржет:: Attach](#attach)|Присоединяет существующий интерфейс целевого объекта отрисовки к объекту|
|[Кдкрендертаржет:: Бинддк](#binddc)|Привязывает целевой объект отрисовки к контексту устройства, к которому он выдает команды рисования|
|[Кдкрендертаржет:: Create](#create)|Создает Кдкрендертаржет.|
|[Кдкрендертаржет::D етач](#detach)|Отсоединяет целевой интерфейс прорисовки от объекта|
|[Кдкрендертаржет:: Жетдкрендертаржет](#getdcrendertarget)|Возвращает интерфейс ID2D1DCRenderTarget|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Кдкрендертаржет:: operator ID2D1DCRenderTarget *](#operator_id2d1dcrendertarget_star)|Возвращает интерфейс ID2D1DCRenderTarget|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Кдкрендертаржет:: m_pDCRenderTarget](#m_pdcrendertarget)|Указатель на объект ID2D1DCRenderTarget.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[крендертаржет](../../mfc/reference/crendertarget-class.md)

[кдкрендертаржет](../../mfc/reference/cdcrendertarget-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cdcrendertargetattach"></a><a name="attach"></a> Кдкрендертаржет:: Attach

Присоединяет существующий интерфейс целевого объекта отрисовки к объекту

```cpp
void Attach(ID2D1DCRenderTarget* pTarget);
```

### <a name="parameters"></a>Параметры

*птаржет*<br/>
Существующий интерфейс целевого объекта рендеринга. Не может иметь значение NULL

## <a name="cdcrendertargetbinddc"></a><a name="binddc"></a> Кдкрендертаржет:: Бинддк

Привязывает целевой объект отрисовки к контексту устройства, к которому он выдает команды рисования

```
BOOL BindDC(
    const CDC& dc,
    const CRect& rect);
```

### <a name="parameters"></a>Параметры

*dc*<br/>
Контекст устройства, к которому команды прорисовки выдает проблемы

*rect*<br/>
Размеры маркера для контекста устройства (HDC), к которому привязан целевой объект прорисовки

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cdcrendertargetcdcrendertarget"></a><a name="cdcrendertarget"></a> Кдкрендертаржет:: Кдкрендертаржет

Конструирует объект Кдкрендертаржет.

```
CDCRenderTarget();
```

## <a name="cdcrendertargetcreate"></a><a name="create"></a> Кдкрендертаржет:: Create

Создает Кдкрендертаржет.

```
BOOL Create(const D2D1_RENDER_TARGET_PROPERTIES& props);
```

### <a name="parameters"></a>Параметры

*Props*<br/>
Режим рендеринга, формат пикселей, параметры удаленного взаимодействия, сведения о DPI и минимальная поддержка DirectX, необходимая для отрисовки оборудования.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cdcrendertargetdetach"></a><a name="detach"></a> Кдкрендертаржет::D етач

Отсоединяет целевой интерфейс прорисовки от объекта

```
ID2D1DCRenderTarget* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный целевой интерфейс рендеринга.

## <a name="cdcrendertargetgetdcrendertarget"></a><a name="getdcrendertarget"></a> Кдкрендертаржет:: Жетдкрендертаржет

Возвращает интерфейс ID2D1DCRenderTarget

```
ID2D1DCRenderTarget* GetDCRenderTarget();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1DCRenderTarget или значение NULL, если объект еще не инициализирован.

## <a name="cdcrendertargetm_pdcrendertarget"></a><a name="m_pdcrendertarget"></a> Кдкрендертаржет:: m_pDCRenderTarget

Указатель на объект ID2D1DCRenderTarget.

```
ID2D1DCRenderTarget* m_pDCRenderTarget;
```

## <a name="cdcrendertargetoperator-id2d1dcrendertarget"></a><a name="operator_id2d1dcrendertarget_star"></a> Кдкрендертаржет:: operator ID2D1DCRenderTarget *

Возвращает интерфейс ID2D1DCRenderTarget

```
operator ID2D1DCRenderTarget*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1DCRenderTarget или значение NULL, если объект еще не инициализирован.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
