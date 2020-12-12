---
description: 'Дополнительные сведения о: CTreeView Class'
title: Класс CTreeView
ms.date: 11/04/2016
f1_keywords:
- CTreeView
- AFXCVIEW/CTreeView
- AFXCVIEW/CTreeView::CTreeView
- AFXCVIEW/CTreeView::GetTreeCtrl
helpviewer_keywords:
- CTreeView [MFC], CTreeView
- CTreeView [MFC], GetTreeCtrl
ms.assetid: 5df583a6-d69f-42ca-9d8d-57e04558afff
ms.openlocfilehash: 3e50f912f03d5214e8ec238844b3288691a4f326
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318524"
---
# <a name="ctreeview-class"></a>Класс CTreeView

Упрощает использование элемента управления "дерево" и [CTreeCtrl](../../mfc/reference/ctreectrl-class.md), класса, который инкапсулирует функции управления деревом, с архитектурой "документ-представление" MFC.

## <a name="syntax"></a>Синтаксис

```
class CTreeView : public CCtrlView
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CTreeView:: CTreeView](#ctreeview)|Формирует объект `CTreeView`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CTreeView:: GetTreeCtrl](#gettreectrl)|Возвращает элемент управления "дерево", связанный с представлением.|

## <a name="remarks"></a>Комментарии

Дополнительные сведения об этой архитектуре см. в обзоре класса [CView](../../mfc/reference/cview-class.md) и перекрестных ссылок, указанных здесь.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CView](../../mfc/reference/cview-class.md)

[CCtrlView](../../mfc/reference/cctrlview-class.md)

`CTreeView`

## <a name="requirements"></a>Требования

**Заголовок:** афксквиев. h

## <a name="ctreeviewctreeview"></a><a name="ctreeview"></a> CTreeView:: CTreeView

Формирует объект `CTreeView`.

```
CTreeView();
```

## <a name="ctreeviewgettreectrl"></a><a name="gettreectrl"></a> CTreeView:: GetTreeCtrl

Возвращает ссылку на элемент управления "дерево", связанный с представлением.

```
CTreeCtrl& GetTreeCtrl() const;
```

## <a name="see-also"></a>См. также раздел

[Класс Кктрлвиев](../../mfc/reference/cctrlview-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CView](../../mfc/reference/cview-class.md)<br/>
[Класс Кктрлвиев](../../mfc/reference/cctrlview-class.md)<br/>
[Класс CTreeCtrl](../../mfc/reference/ctreectrl-class.md)
