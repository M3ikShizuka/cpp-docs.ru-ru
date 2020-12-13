---
description: 'Дополнительные сведения о: Чвндрендертаржет Class'
title: Класс CHwndRenderTarget
ms.date: 11/04/2016
f1_keywords:
- CHwndRenderTarget
- AFXRENDERTARGET/CHwndRenderTarget
- AFXRENDERTARGET/CHwndRenderTarget::CHwndRenderTarget
- AFXRENDERTARGET/CHwndRenderTarget::Attach
- AFXRENDERTARGET/CHwndRenderTarget::CheckWindowState
- AFXRENDERTARGET/CHwndRenderTarget::Create
- AFXRENDERTARGET/CHwndRenderTarget::Detach
- AFXRENDERTARGET/CHwndRenderTarget::GetHwnd
- AFXRENDERTARGET/CHwndRenderTarget::GetHwndRenderTarget
- AFXRENDERTARGET/CHwndRenderTarget::ReCreate
- AFXRENDERTARGET/CHwndRenderTarget::Resize
- AFXRENDERTARGET/CHwndRenderTarget::m_pHwndRenderTarget
helpviewer_keywords:
- CHwndRenderTarget [MFC], CHwndRenderTarget
- CHwndRenderTarget [MFC], Attach
- CHwndRenderTarget [MFC], CheckWindowState
- CHwndRenderTarget [MFC], Create
- CHwndRenderTarget [MFC], Detach
- CHwndRenderTarget [MFC], GetHwnd
- CHwndRenderTarget [MFC], GetHwndRenderTarget
- CHwndRenderTarget [MFC], ReCreate
- CHwndRenderTarget [MFC], Resize
- CHwndRenderTarget [MFC], m_pHwndRenderTarget
ms.assetid: aa65b69f-7202-46ea-af81-ef325da0b840
ms.openlocfilehash: 3a3058105fff5e5ac304f2cc980cd93f2bac70a4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97143641"
---
# <a name="chwndrendertarget-class"></a>Класс CHwndRenderTarget

Оболочка для ID2D1HwndRenderTarget.

## <a name="syntax"></a>Синтаксис

```
class CHwndRenderTarget : public CRenderTarget;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Чвндрендертаржет:: Чвндрендертаржет](#chwndrendertarget)|Конструирует объект Чвндрендертаржет из HWND.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Чвндрендертаржет:: Attach](#attach)|Присоединяет существующий интерфейс целевого объекта отрисовки к объекту|
|[Чвндрендертаржет:: Чекквиндовстате](#checkwindowstate)|Указывает, является ли HWND, связанный с данным объектом прорисовки, перекрыто.|
|[Чвндрендертаржет:: Create](#create)|Создает целевой объект прорисовки, связанный с окном|
|[Чвндрендертаржет::D етач](#detach)|Отсоединяет целевой интерфейс прорисовки от объекта|
|[Чвндрендертаржет:: "HWND"](#gethwnd)|Возвращает HWND, связанный с этим целевым объектом прорисовки.|
|[Чвндрендертаржет:: Жесвндрендертаржет](#gethwndrendertarget)|Возвращает интерфейс ID2D1HwndRenderTarget.|
|[Чвндрендертаржет:: повторное создание](#recreate)|Повторное создание целевого объекта прорисовки, связанного с окном|
|[Чвндрендертаржет:: изменение размера](#resize)|Изменяет размер целевого объекта отрисовки на указанный размер в пикселях|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Чвндрендертаржет:: operator ID2D1HwndRenderTarget *](#operator_id2d1hwndrendertarget_star)|Возвращает интерфейс ID2D1HwndRenderTarget.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Чвндрендертаржет:: m_pHwndRenderTarget](#m_phwndrendertarget)|Указатель на объект ID2D1HwndRenderTarget.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[крендертаржет](../../mfc/reference/crendertarget-class.md)

[чвндрендертаржет](../../mfc/reference/chwndrendertarget-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="chwndrendertargetattach"></a><a name="attach"></a> Чвндрендертаржет:: Attach

Присоединяет существующий интерфейс целевого объекта отрисовки к объекту

```cpp
void Attach(ID2D1HwndRenderTarget* pTarget);
```

### <a name="parameters"></a>Параметры

*птаржет*<br/>
Существующий интерфейс целевого объекта рендеринга. Не может иметь значение NULL

## <a name="chwndrendertargetcheckwindowstate"></a><a name="checkwindowstate"></a> Чвндрендертаржет:: Чекквиндовстате

Указывает, является ли HWND, связанный с данным объектом прорисовки, перекрыто.

```
D2D1_WINDOW_STATE CheckWindowState() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение, указывающее, является ли HWND, связанный с данным объектом прорисовки, перекрыто.

## <a name="chwndrendertargetchwndrendertarget"></a><a name="chwndrendertarget"></a> Чвндрендертаржет:: Чвндрендертаржет

Конструирует объект Чвндрендертаржет из HWND.

```
CHwndRenderTarget(HWND hwnd = NULL);
```

### <a name="parameters"></a>Параметры

*HWND*<br/>
HWND, связанный с этим целевым объектом прорисовки

## <a name="chwndrendertargetcreate"></a><a name="create"></a> Чвндрендертаржет:: Create

Создает целевой объект прорисовки, связанный с окном

```
BOOL Create(HWND hWnd);
```

### <a name="parameters"></a>Параметры

*hWnd*<br/>
HWND, связанный с этим целевым объектом прорисовки

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="chwndrendertargetdetach"></a><a name="detach"></a> Чвндрендертаржет::D етач

Отсоединяет целевой интерфейс прорисовки от объекта

```
ID2D1HwndRenderTarget* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный целевой интерфейс рендеринга.

## <a name="chwndrendertargetgethwnd"></a><a name="gethwnd"></a> Чвндрендертаржет:: "HWND"

Возвращает HWND, связанный с этим целевым объектом прорисовки.

```
HWND GetHwnd() const;
```

### <a name="return-value"></a>Возвращаемое значение

HWND, связанный с этим целевым объектом рендеринга.

## <a name="chwndrendertargetgethwndrendertarget"></a><a name="gethwndrendertarget"></a> Чвндрендертаржет:: Жесвндрендертаржет

Возвращает интерфейс ID2D1HwndRenderTarget.

```
ID2D1HwndRenderTarget* GetHwndRenderTarget();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1HwndRenderTarget или значение NULL, если объект еще не инициализирован.

## <a name="chwndrendertargetm_phwndrendertarget"></a><a name="m_phwndrendertarget"></a> Чвндрендертаржет:: m_pHwndRenderTarget

Указатель на объект ID2D1HwndRenderTarget.

```
ID2D1HwndRenderTarget* m_pHwndRenderTarget;
```

## <a name="chwndrendertargetoperator-id2d1hwndrendertarget"></a><a name="operator_id2d1hwndrendertarget_star"></a> Чвндрендертаржет:: operator ID2D1HwndRenderTarget *

Возвращает интерфейс ID2D1HwndRenderTarget.

```
operator ID2D1HwndRenderTarget*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1HwndRenderTarget или значение NULL, если объект еще не инициализирован.

## <a name="chwndrendertargetrecreate"></a><a name="recreate"></a> Чвндрендертаржет:: повторное создание

Повторное создание целевого объекта прорисовки, связанного с окном

```
BOOL ReCreate(HWND hWnd);
```

### <a name="parameters"></a>Параметры

*hWnd*<br/>
HWND, связанный с этим целевым объектом прорисовки

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="chwndrendertargetresize"></a><a name="resize"></a> Чвндрендертаржет:: изменение размера

Изменяет размер целевого объекта отрисовки на указанный размер в пикселях

```
BOOL Resize(const CD2DSizeU& size);
```

### <a name="parameters"></a>Параметры

*size*<br/>
Новый размер целевого объекта отрисовки в пикселях устройства

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
