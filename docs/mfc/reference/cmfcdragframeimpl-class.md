---
description: 'Дополнительные сведения о: Кмфкдрагфрамеимпл Class'
title: Класс Кмфкдрагфрамеимпл
ms.date: 10/18/2018
f1_keywords:
- CMFCDragFrameImpl
helpviewer_keywords:
- CMFCDragFrameImpl class [MFC]
ms.assetid: 500cd824-8188-43c2-8754-b7bb46b5648a
ms.openlocfilehash: 9885b750ace86d11ca573f23c7ee1c03d8926921
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97294058"
---
# <a name="cmfcdragframeimpl-class"></a>Класс Кмфкдрагфрамеимпл

`CMFCDragFrameImpl`Класс рисует прямоугольник перетаскивания, который появляется, когда пользователь перетаскивает панель в стандартном режиме закрепления.
Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```
class CMFCDragFrameImpl
```

## <a name="remarks"></a>Remarks

Объект этого класса внедряется в каждый объект [класса CPane](../../mfc/reference/cpane-class.md) . Таким способом, каждая панель, использующая `CanFloat` метод, отображает прямоугольник перетаскивания, когда пользователь перетаскивает его.

Толщиной прямоугольника перетаскивания можно управлять с помощью [AFX_GLOBAL_DATA:: m_nDragFrameThicknessFloat](afx-global-data-structure.md#m_ndragframethicknessfloat) и [AFX_GLOBAL_DATA:: m_nDragFrameThicknessDock](afx-global-data-structure.md#m_ndragframethicknessdock).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CMFCDragFrameImpl](../../mfc/reference/cmfcdragframeimpl-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксдрагфрамеимпл. h

## <a name="cmfcdragframeimplenddrawdragframe"></a><a name="enddrawdragframe"></a> Кмфкдрагфрамеимпл:: Енддравдрагфраме

```cpp
void EndDrawDragFrame(BOOL bClearInternalRects = TRUE);
```

### <a name="parameters"></a>Параметры

окне *бклеаринтерналректс*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcdragframeimplinit"></a><a name="init"></a> Кмфкдрагфрамеимпл:: init

```cpp
void Init(CWnd* pDraggedWnd);
```

### <a name="parameters"></a>Параметры

окне *пдрагжедвнд*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcdragframeimplmovedragframe"></a><a name="movedragframe"></a> Кмфкдрагфрамеимпл:: Моведрагфраме

```cpp
void MoveDragFrame(BOOL bForceMove = FALSE);
```

### <a name="parameters"></a>Параметры

окне *бфорцемове*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcdragframeimplplacetabpredocking"></a><a name="placetabpredocking"></a> Кмфкдрагфрамеимпл::P Лацетабпредоккинг

```cpp
void PlaceTabPreDocking(
    CBaseTabbedPane* pTabbedBar,
    BOOL bFirstTime);

void PlaceTabPreDocking(CWnd* pCBarToPlaceOn);
```

### <a name="parameters"></a>Параметры

окне *птаббедбар*<br/>

окне *бфирсттиме*<br/>

окне *пкбартоплацеон*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcdragframeimplremovetabpredocking"></a><a name="removetabpredocking"></a> Кмфкдрагфрамеимпл:: Ремоветабпредоккинг

```cpp
void RemoveTabPreDocking(CDockablePane* pOldTargetBar = NULL);
```

### <a name="parameters"></a>Параметры

окне *полдтаржетбар*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmfcdragframeimplresetstate"></a><a name="resetstate"></a> Кмфкдрагфрамеимпл:: ResetState

```cpp
void ResetState();
```

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CPane](../../mfc/reference/cpane-class.md)
