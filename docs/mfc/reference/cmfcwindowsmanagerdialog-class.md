---
description: 'Дополнительные сведения о: Кмфквиндовсманажердиалог Class'
title: Класс Кмфквиндовсманажердиалог
ms.date: 11/04/2016
f1_keywords:
- CMFCWindowsManagerDialog
- AFXWINDOWSMANAGERDIALOG/CMFCWindowsManagerDialog
- AFXWINDOWSMANAGERDIALOG/CMFCWindowsManagerDialog::CMFCWindowsManagerDialog
helpviewer_keywords:
- CMFCWindowsManagerDialog [MFC], CMFCWindowsManagerDialog
ms.assetid: 35b4b0db-33c4-4b22-94d8-5e3396341340
ms.openlocfilehash: 526cf731e049ffd267382b0c3895b5d29792dcb0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331619"
---
# <a name="cmfcwindowsmanagerdialog-class"></a>Класс Кмфквиндовсманажердиалог

`CMFCWindowsManagerDialog`Объект позволяет пользователю управлять дочерними ОКНАМИ MDI в приложении MDI.

## <a name="syntax"></a>Синтаксис

```
class CMFCWindowsManagerDialog : public CDialog
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфквиндовсманажердиалог:: Кмфквиндовсманажердиалог](#cmfcwindowsmanagerdialog)|Формирует объект `CMFCWindowsManagerDialog`.|

## <a name="remarks"></a>Комментарии

`CMFCWindowsManagerDialog`Содержит список дочерних окон MDI, которые в данный момент открыты в приложении. Пользователь может вручную управлять состоянием дочерних окон MDI с помощью этого диалогового окна.

`CMFCWindowsManagerDialog` внедряется в [класс CMDIFrameWndEx](../../mfc/reference/cmdiframewndex-class.md). `CMFCWindowsManagerDialog`Не является классом, который необходимо создать вручную. Вместо этого вызовите функцию [CMDIFrameWndEx:: шоввиндовсдиалог](../../mfc/reference/cmdiframewndex-class.md#showwindowsdialog), и она создаст и отобразит `CMFCWindowsManagerDialog` объект.

## <a name="example"></a>Пример

В следующем примере показано, как создать `CMFCWindowsManagerDialog` объект путем вызова `CMDIFrameWndEx::ShowWindowsDialog` . Этот фрагмент кода является частью [демонстрационного примера Visual Studio](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_VisualStudioDemo#18](../../mfc/codesnippet/cpp/cmfcwindowsmanagerdialog-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CDialog](../../mfc/reference/cdialog-class.md)

[CMFCWindowsManagerDialog](../../mfc/reference/cmfcwindowsmanagerdialog-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксвиндовсманажердиалог. h

## <a name="cmfcwindowsmanagerdialogcmfcwindowsmanagerdialog"></a><a name="cmfcwindowsmanagerdialog"></a> Кмфквиндовсманажердиалог:: Кмфквиндовсманажердиалог

Конструирует объект [кмфквиндовсманажердиалог](../../mfc/reference/cmfcwindowsmanagerdialog-class.md) .

```
CMFCWindowsManagerDialog(
    CMDIFrameWndEx* pMDIFrame,
    BOOL bHelpButton = FALSE);
```

### <a name="parameters"></a>Параметры

*пмдифраме*<br/>
окне Указатель на родительское или окно-владелец.

*бхелпбуттон*<br/>
окне Логический параметр, указывающий, отображает ли платформа кнопку " **Справка** ".

### <a name="remarks"></a>Комментарии

Дополнительные сведения о визуальных диспетчерах см. в разделе [Диспетчер визуализации](../../mfc/visualization-manager.md).

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CMDIFrameWndEx](../../mfc/reference/cmdiframewndex-class.md)
