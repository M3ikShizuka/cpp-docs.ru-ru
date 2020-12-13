---
description: 'Дополнительные сведения о: Кмфктулбаринфо Class'
title: Класс Кмфктулбаринфо
ms.date: 11/04/2016
f1_keywords:
- CMFCToolBarInfo
- AFXTOOLBAR/CMFCToolBarInfo
- AFXTOOLBAR/CMFCToolBarInfo::m_uiColdResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiDisabledResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiHotResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiLargeColdResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiLargeDisabledResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiLargeHotResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiMenuDisabledResID
- AFXTOOLBAR/CMFCToolBarInfo::m_uiMenuResID
helpviewer_keywords:
- CMFCToolBarInfo [MFC], m_uiColdResID
- CMFCToolBarInfo [MFC], m_uiDisabledResID
- CMFCToolBarInfo [MFC], m_uiHotResID
- CMFCToolBarInfo [MFC], m_uiLargeColdResID
- CMFCToolBarInfo [MFC], m_uiLargeDisabledResID
- CMFCToolBarInfo [MFC], m_uiLargeHotResID
- CMFCToolBarInfo [MFC], m_uiMenuDisabledResID
- CMFCToolBarInfo [MFC], m_uiMenuResID
ms.assetid: 6dc84482-eaaa-491f-aa5d-dd7a57886b46
ms.openlocfilehash: 9b85ef4f39c8b42c35975a15836a21e7cc6dd6b1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331708"
---
# <a name="cmfctoolbarinfo-class"></a>Класс Кмфктулбаринфо

Содержит идентификаторы ресурса изображений панели инструментов в различных состояниях. `CMFCToolBarInfo` — Это вспомогательный класс, который используется в качестве параметра метода [CMFCToolBar:: лоадтулбарекс](../../mfc/reference/cmfctoolbar-class.md#loadtoolbarex) .

## <a name="syntax"></a>Синтаксис

```
class CMFCToolBarInfo
```

## <a name="members"></a>Члены

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|[Кмфктулбаринфо:: m_uiColdResID](#m_uicoldresid)|Идентификатор ресурса точечного рисунка панели инструментов, который содержит обычные (холодные) изображения панели инструментов.|
|[Кмфктулбаринфо:: m_uiDisabledResID](#m_uidisabledresid)|Идентификатор ресурса точечного рисунка панели инструментов, который содержит отключенные изображения панели инструментов.|
|[Кмфктулбаринфо:: m_uiHotResID](#m_uihotresid)|Идентификатор ресурса точечного рисунка панели инструментов, который содержит выбранные (горячие) изображения панели инструментов.|
|[Кмфктулбаринфо:: m_uiLargeColdResID](#m_uilargecoldresid)|Идентификатор ресурса точечного рисунка панели инструментов, который содержит крупные обычные изображения панели инструментов.|
|[Кмфктулбаринфо:: m_uiLargeDisabledResID](#m_uilargedisabledresid)|Идентификатор ресурса точечного рисунка панели инструментов, содержащего крупные, отключенные изображения панели инструментов.|
|[Кмфктулбаринфо:: m_uiLargeHotResID](#m_uilargehotresid)|Идентификатор ресурса точечного рисунка панели инструментов, содержащего крупные, выбранные изображения панели инструментов.|
|[Кмфктулбаринфо:: m_uiMenuDisabledResID](#m_uimenudisabledresid)|Идентификатор ресурса точечного рисунка панели инструментов, который содержит отключенные изображения меню.|
|[Кмфктулбаринфо:: m_uiMenuResID](#m_uimenuresid)|Идентификатор ресурса точечного рисунка панели инструментов, который содержит изображения меню.|

## <a name="remarks"></a>Комментарии

Полный точечный рисунок панели инструментов состоит из мелких изображений (кнопок) на панели инструментов фиксированного размера. Каждый идентификатор ресурса, хранящийся в `CMFCToolBarInfo` объекте, является точечным рисунком, содержащим полный набор изображений панелей инструментов в одном состоянии (например, выбранные, отключенные, крупные или изображения меню).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CMFCToolBarInfo](../../mfc/reference/cmfctoolbarinfo-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афкстулбар. h

## <a name="cmfctoolbarinfom_uicoldresid"></a><a name="m_uicoldresid"></a> Кмфктулбаринфо:: m_uiColdResID

Указывает идентификатор ресурса для всех изображений обычных кнопок панели инструментов.

```
UINT m_uiColdResID;
```

## <a name="cmfctoolbarinfom_uidisabledresid"></a><a name="m_uidisabledresid"></a> Кмфктулбаринфо:: m_uiDisabledResID

Указывает идентификатор ресурса для недоступных для кнопки изображений на панели инструментов.

```
UINT m_uiDisabledResID;
```

## <a name="cmfctoolbarinfom_uihotresid"></a><a name="m_uihotresid"></a> Кмфктулбаринфо:: m_uiHotResID

Указывает идентификатор ресурса для всех выделенных изображений кнопки панели инструментов.

```
UINT m_uiHotResID
```

## <a name="cmfctoolbarinfom_uilargecoldresid"></a><a name="m_uilargecoldresid"></a> Кмфктулбаринфо:: m_uiLargeColdResID

Указывает идентификатор ресурса для всех крупных изображений обычной кнопки панели инструментов.

```
UINT m_uiLargeColdResID
```

## <a name="cmfctoolbarinfom_uilargedisabledresid"></a><a name="m_uilargedisabledresid"></a> Кмфктулбаринфо:: m_uiLargeDisabledResID

Указывает идентификатор ресурса для всех крупных отключенных изображений кнопок панели инструментов.

```
UINT m_uiLargeDisabledResID;
```

## <a name="cmfctoolbarinfom_uilargehotresid"></a><a name="m_uilargehotresid"></a> Кмфктулбаринфо:: m_uiLargeHotResID

Указывает идентификатор ресурса для всех крупных выделенных изображений панели инструментов.

```
UINT m_uiLargeHotResID;
```

## <a name="cmfctoolbarinfom_uimenudisabledresid"></a><a name="m_uimenudisabledresid"></a> Кмфктулбаринфо:: m_uiMenuDisabledResID

Указывает идентификатор ресурса для недоступных для команды изображений на панели инструментов.

```
UINT m_uiMenuDisabledResID;
```

## <a name="cmfctoolbarinfom_uimenuresid"></a><a name="m_uimenuresid"></a> Кмфктулбаринфо:: m_uiMenuResID

Указывает идентификатор ресурса для всех стандартных изображений элементов меню на панели инструментов.

```
UINT m_uiMenuResID;
```

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md)
