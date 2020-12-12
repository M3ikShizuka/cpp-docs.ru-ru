---
description: 'Дополнительные сведения о: класс CListView'
title: Класс CListView
ms.date: 11/04/2016
f1_keywords:
- CListView
- AFXCVIEW/CListView
- AFXCVIEW/CListView::CListView
- AFXCVIEW/CListView::GetListCtrl
- AFXCVIEW/CListView::RemoveImageList
helpviewer_keywords:
- CListView [MFC], CListView
- CListView [MFC], GetListCtrl
- CListView [MFC], RemoveImageList
ms.assetid: 7626bdb2-a1b8-4eab-b631-6743710a8432
ms.openlocfilehash: 5576a0997c84e8f5639911a1120a6645e720a7cf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97259569"
---
# <a name="clistview-class"></a>Класс CListView

Упрощает использование элемента управления "список" и [CListCtrl](../../mfc/reference/clistctrl-class.md), класса, который инкапсулирует функции управления списком, с помощью архитектуры "документ-представление" MFC.

## <a name="syntax"></a>Синтаксис

```
class CListView : public CCtrlView
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CListView:: CListView](#clistview)|Формирует объект `CListView`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CListView:: Getlistctr](#getlistctrl)|Возвращает элемент управления "список", связанный с представлением.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[CListView:: Ремовеимажелист](#removeimagelist)|Удаляет указанный список изображений из представления списка.|

## <a name="remarks"></a>Комментарии

Дополнительные сведения об этой архитектуре см. в обзоре класса [CView](../../mfc/reference/cview-class.md) и перекрестных ссылок, указанных здесь.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CView](../../mfc/reference/cview-class.md)

[CCtrlView](../../mfc/reference/cctrlview-class.md)

`CListView`

## <a name="requirements"></a>Требования

**Заголовок:** афксквиев. h

## <a name="clistviewclistview"></a><a name="clistview"></a> CListView:: CListView

Формирует объект `CListView`.

```
CListView();
```

## <a name="clistviewgetlistctrl"></a><a name="getlistctrl"></a> CListView:: Getlistctr

Вызовите эту функцию-член, чтобы получить ссылку на элемент управления "список", связанный с представлением.

```
CListCtrl& GetListCtrl() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на элемент управления "список", связанный с представлением.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCListView#7](../../atl/reference/codesnippet/cpp/clistview-class_1.cpp)]

## <a name="clistviewremoveimagelist"></a><a name="removeimagelist"></a> CListView:: Ремовеимажелист

Удаляет указанный список изображений из представления списка.

```cpp
void RemoveImageList(int nImageList);
```

### <a name="parameters"></a>Параметры

*нимажелист*<br/>
Отсчитываемый от нуля индекс удаляемого изображения.

## <a name="see-also"></a>См. также раздел

[Пример РОВЛИСТ для MFC](../../overview/visual-cpp-samples.md)<br/>
[Класс Кктрлвиев](../../mfc/reference/cctrlview-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Кктрлвиев](../../mfc/reference/cctrlview-class.md)
