---
description: 'Дополнительные сведения о: структура Кмфктабтултипинфо'
title: Структура Кмфктабтултипинфо
ms.date: 11/04/2016
f1_keywords:
- CMFCTabToolTipInfo
helpviewer_keywords:
- CMFCTabToolTipInfo struct
ms.assetid: 9c3b3fb9-1497-4d59-932b-0da9348dd5e2
ms.openlocfilehash: ce9e9f4fdbcf367921e7f0559a4d04e66f4303dc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97164072"
---
# <a name="cmfctabtooltipinfo-structure"></a>Структура Кмфктабтултипинфо

Эта структура предоставляет сведения о вкладке MDI, на которую наводится пользователь.

## <a name="syntax"></a>Синтаксис

```
struct CMFCTabToolTipInfo
```

## <a name="members"></a>Члены

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|[Кмфктабтултипинфо:: m_nTabIndex](#m_ntabindex)|Задает индекс элемента управления "Вкладка".|
|[Кмфктабтултипинфо:: m_pTabWnd](#m_ptabwnd)|Указатель на элемент управления Tab.|
|[Кмфктабтултипинфо:: m_strText](#m_strtext)|Текст подсказки.|

## <a name="remarks"></a>Комментарии

Указатель на `CMFCTabToolTipInfo` структуру передается в качестве параметра сообщения AFX_WM_ON_GET_TAB_TOOLTIP. Это сообщение создается, когда вкладки MDI включены и пользователь наводит указатель мыши на элемент управления Tab.

## <a name="example"></a>Пример

В следующем примере показано `CMFCTabToolTipInfo` , как используется в [примере Мдитабсдемо: приложение для MDI с вкладками MFC](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_MDITabsDemo#2](../../mfc/reference/codesnippet/cpp/cmfctabtooltipinfo-structure_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CMFCTabToolTipInfo](../../mfc/reference/cmfctabtooltipinfo-structure.md)

## <a name="requirements"></a>Требования

**Заголовок:** afxbasetabctrl.h

## <a name="cmfctabtooltipinfom_ntabindex"></a><a name="m_ntabindex"></a> Кмфктабтултипинфо:: m_nTabIndex

Задает индекс элемента управления "Вкладка".

```
int m_nTabIndex;
```

### <a name="remarks"></a>Комментарии

Индекс вкладки, над которой наводится пользователь.

### <a name="example"></a>Пример

В следующем примере показано `m_nTabIndex` , как используется в [примере Мдитабсдемо: приложение для MDI с вкладками MFC](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_MDITabsDemo#2](../../mfc/reference/codesnippet/cpp/cmfctabtooltipinfo-structure_1.cpp)]

## <a name="cmfctabtooltipinfom_ptabwnd"></a><a name="m_ptabwnd"></a> Кмфктабтултипинфо:: m_pTabWnd

Указатель на элемент управления Tab.

```
CMFCBaseTabCtrl* m_pTabWnd;
```

### <a name="example"></a>Пример

В следующем примере показано `m_pTabWnd` , как используется в [примере Мдитабсдемо: приложение для MDI с вкладками MFC](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_MDITabsDemo#2](../../mfc/reference/codesnippet/cpp/cmfctabtooltipinfo-structure_1.cpp)]

## <a name="cmfctabtooltipinfom_strtext"></a><a name="m_strtext"></a> Кмфктабтултипинфо:: m_strText

Текст подсказки.

```
CString m_strText;
```

### <a name="remarks"></a>Комментарии

Если строка пуста, подсказка не отображается.

### <a name="example"></a>Пример

В следующем примере показано `m_strText` , как используется в [примере Мдитабсдемо: приложение для MDI с вкладками MFC](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_MDITabsDemo#2](../../mfc/reference/codesnippet/cpp/cmfctabtooltipinfo-structure_1.cpp)]

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)
