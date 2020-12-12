---
description: 'Дополнительные сведения о: Кмфкбасетулбар Class'
title: Класс Кмфкбасетулбар
ms.date: 11/04/2016
f1_keywords:
- CMFCBaseToolBar
- AFXBASETOOLBAR/CMFCBaseToolBar
- AFXBASETOOLBAR/CMFCBaseToolBar::GetDockingMode
- AFXBASETOOLBAR/CMFCBaseToolBar::GetMinSize
- AFXBASETOOLBAR/CMFCBaseToolBar::OnAfterChangeParent
helpviewer_keywords:
- CMFCBaseToolBar [MFC], GetDockingMode
- CMFCBaseToolBar [MFC], GetMinSize
- CMFCBaseToolBar [MFC], OnAfterChangeParent
ms.assetid: 5d79206d-55e4-46f8-b1b8-042e34d7f9da
ms.openlocfilehash: 37597e4cb300e0d6d16c92f105e332c18c5beda7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97247921"
---
# <a name="cmfcbasetoolbar-class"></a>Класс Кмфкбасетулбар

Базовый класс для панелей инструментов.

## <a name="syntax"></a>Синтаксис

```
class CMFCBaseToolBar : public CPane
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CMFCBaseToolBar::CMFCBaseToolBar`|Конструктор по умолчанию.|
|`CMFCBaseToolBar::~CMFCBaseToolBar`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|`CMFCBaseToolBar::CreateObject`|Используется платформой для создания динамического экземпляра этого типа класса.|
|[Кмфкбасетулбар:: Жетдоккингмоде](#getdockingmode)|Возвращает режим закрепления. (Переопределяет [CBasePane:: жетдоккингмоде](../../mfc/reference/cbasepane-class.md#getdockingmode).)|
|[Кмфкбасетулбар:: Жетминсизе](#getminsize)|Возвращает минимальный размер панели инструментов. (Переопределяет [CPane:: жетминсизе](../../mfc/reference/cpane-class.md#getminsize).)|
|[Кмфкбасетулбар:: Онафтерчанжепарент](#onafterchangeparent)|Вызвано структурой после изменения родительского элемента панели. (Переопределяет [CBasePane:: онафтерчанжепарент](../../mfc/reference/cbasepane-class.md#onafterchangeparent).)|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CBasePane](../../mfc/reference/cbasepane-class.md)

[CPane](../../mfc/reference/cpane-class.md)

[кмфкбасетулбар](../../mfc/reference/cmfcbasetoolbar-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксбасетулбар. h

## <a name="cmfcbasetoolbargetdockingmode"></a><a name="getdockingmode"></a> Кмфкбасетулбар:: Жетдоккингмоде

Возвращает режим закрепления.

```
virtual AFX_DOCK_TYPE GetDockingMode() const;
```

### <a name="return-value"></a>Возвращаемое значение

Режим закрепления.

## <a name="cmfcbasetoolbargetminsize"></a><a name="getminsize"></a> Кмфкбасетулбар:: Жетминсизе

Возвращает минимальный размер панели инструментов.

```
virtual void GetMinSize(CSize& size) const;
```

### <a name="parameters"></a>Параметры

*size*<br/>
заполняет Минимальный размер панели инструментов.

## <a name="cmfcbasetoolbaronafterchangeparent"></a><a name="onafterchangeparent"></a> Кмфкбасетулбар:: Онафтерчанжепарент

Вызвано структурой после изменения родительского элемента панели.

```
virtual void OnAfterChangeParent(CWnd* pWndOldParent);
```

### <a name="parameters"></a>Параметры

*пвндолдпарент*<br/>
окне Указатель на предыдущее родительское окно.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)
