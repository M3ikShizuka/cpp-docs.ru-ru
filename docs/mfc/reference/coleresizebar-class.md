---
description: 'Дополнительные сведения о: Колересизебар Class'
title: Класс Колересизебар
ms.date: 11/04/2016
f1_keywords:
- COleResizeBar
- AFXOLE/COleResizeBar
- AFXOLE/COleResizeBar::COleResizeBar
- AFXOLE/COleResizeBar::Create
helpviewer_keywords:
- COleResizeBar [MFC], COleResizeBar
- COleResizeBar [MFC], Create
ms.assetid: 56a708d9-28c5-4eb0-9404-77b688d91c63
ms.openlocfilehash: bdd97e854257e2f858b52ed45f4066b26c71394d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226718"
---
# <a name="coleresizebar-class"></a>Класс Колересизебар

Тип панели элементов управления, который поддерживает изменение размера элементов OLE "на месте".

## <a name="syntax"></a>Синтаксис

```
class COleResizeBar : public CControlBar
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Колересизебар:: Колересизебар](#coleresizebar)|Формирует объект `COleResizeBar`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Колересизебар:: Create](#create)|Создает и инициализирует дочернее окно Windows и связывает его с `COleResizeBar` объектом.|

## <a name="remarks"></a>Комментарии

`COleResizeBar` объекты отображаются в виде [кректтраккер](../../mfc/reference/crecttracker-class.md) с заштрихованной границей и внешними маркерами изменения размера.

`COleResizeBar` объекты обычно являются внедренными элементами объектов окна кадров, производных от класса [COleIPFrameWnd](../../mfc/reference/coleipframewnd-class.md) .

Дополнительные сведения см. в статье [Активация](../../mfc/activation-cpp.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CControlBar](../../mfc/reference/ccontrolbar-class.md)

`COleResizeBar`

## <a name="requirements"></a>Требования

**Заголовок:** афксоле. h

## <a name="coleresizebarcoleresizebar"></a><a name="coleresizebar"></a> Колересизебар:: Колересизебар

Формирует объект `COleResizeBar`.

```
COleResizeBar();
```

### <a name="remarks"></a>Комментарии

Вызовите метод `Create` , чтобы создать объект Bar изменения размера.

## <a name="coleresizebarcreate"></a><a name="create"></a> Колересизебар:: Create

Создает дочернее окно и связывает его с `COleResizeBar` объектом.

```
virtual BOOL Create(
    CWnd* pParentWnd,
    DWORD dwStyle = WS_CHILD | WS_VISIBLE,
    UINT nID = AFX_IDW_RESIZE_BAR);
```

### <a name="parameters"></a>Параметры

*ппарентвнд*<br/>
Указатель на родительское окно строки изменения размера.

*двстиле*<br/>
Задает атрибуты [стиля окна](../../mfc/reference/styles-used-by-mfc.md#window-styles) .

*nID*<br/>
Идентификатор дочернего окна в строке изменения размера.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если была создана строка изменения размера; в противном случае — 0.

## <a name="see-also"></a>См. также раздел

[Пример SUPERPAD в MFC](../../overview/visual-cpp-samples.md)<br/>
[Класс CControlBar](../../mfc/reference/ccontrolbar-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Колесервердок](../../mfc/reference/coleserverdoc-class.md)
