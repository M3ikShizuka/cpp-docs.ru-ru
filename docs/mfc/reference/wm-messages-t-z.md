---
description: 'Дополнительные сведения: WM_ сообщения: T-Z'
title: Сообщения WM_ T — Z
ms.date: 11/04/2016
f1_keywords:
- ON_WM_TCARD
- ON_WM_WININICHANGE
- ON_WM_VSCROLLCLIPBOARD
- ON_WM_VSCROLL
- ON_WM_WINDOWPOSCHANGED
- ON_WM_TIMECHANGE
- ON_WM_TIMER
- ON_WM_VKEYTOITEM
- ON_WM_WINDOWPOSCHANGING
helpviewer_keywords:
- ON_WM_VSCROLLCLIPBOARD [MFC]
- ON_WM_WININICHANGE [MFC]
- ON_WM_WINDOWPOSCHANGED [MFC]
- ON_WM_TCARD [MFC]
- ON_WM_TIMECHANGE [MFC]
- ON_WM_TIMER [MFC]
- WM_ messages [MFC]
- ON_WM_WINDOWPOSCHANGING [MFC]
- ON_WM_VKEYTOITEM [MFC]
- ON_WM_VSCROLL
ms.assetid: c528bb2e-ddb5-4da6-b652-432a387408b8
ms.openlocfilehash: 3d564c94c8b8d75840e6291b4024159acb7becbc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97218229"
---
# <a name="wm_-messages-t---z"></a>Сообщения WM_ T — Z

Следующие записи Map соответствуют прототипам функций:

|Запись Map|Прототип функции|
|---------------|------------------------|
|ON_WM_TCARD ()|afx_msg void [онткард](../../mfc/reference/cwnd-class.md#ontcard)(uint, DWORD);|
|ON_WM_TIMECHANGE ()|afx_msg void [онтимечанже](../../mfc/reference/cwnd-class.md#ontimechange)();|
|ON_WM_TIMER ()|afx_msg void [OnTime](../../mfc/reference/cwnd-class.md#ontimer)(UINT_PTR);|
|ON_WM_UNICHAR ()|afx_msg void [онуничар](../../mfc/reference/cwnd-class.md#onunichar)(UINT, UINT, uint);|
|ON_WM_UNINITMENUPOPUP ()|afx_msg void [онунинитменупопуп](../../mfc/reference/cwnd-class.md#onuninitmenupopup)(кмену *, uint);|
|ON_WM_USERCHANGED ()|afx_msg void [онусерчанжед](../../mfc/reference/cwnd-class.md#onuserchanged)();|
|ON_WM_VKEYTOITEM ()|afx_msg int [онвкэйтоитем](../../mfc/reference/cwnd-class.md#onvkeytoitem)(uint, CWnd *, uint);|
|ON_WM_VSCROLL ()|afx_msg void [онвскролл](../../mfc/reference/cwnd-class.md#onvscroll)(UINT, uint, CWnd *);|
|ON_WM_VSCROLLCLIPBOARD ()|afx_msg void [онвскроллклипбоард](../../mfc/reference/cwnd-class.md#onvscrollclipboard)(CWnd *, UINT, uint);|
|ON_WM_WINDOWPOSCHANGED ()|afx_msg void [онвиндовпосчанжед](../../mfc/reference/cwnd-class.md#onwindowposchanged)(WINDOWPOS *);|
|ON_WM_WINDOWPOSCHANGING ()|afx_msg void [онвиндовпосчангинг](../../mfc/reference/cwnd-class.md#onwindowposchanging)(WINDOWPOS *);|
|ON_WM_WININICHANGE ()|afx_msg void [онвининичанже](../../mfc/reference/cwnd-class.md#onwininichange)(LPStr);|
|ON_WM_WTSSESSION_CHANGE ()|afx_msg void [онсессиончанже](../../mfc/reference/cwnd-class.md#onsessionchange)(UINT, uint);|
|ON_WM_XBUTTONDBLCLK ()|afx_msg void [онксбуттондблклк](../../mfc/reference/cwnd-class.md#onxbuttondblclk)(UINT, uint, CPoint);|
|ON_WM_XBUTTONDOWN ()|afx_msg void [онксбуттондовн](../../mfc/reference/cwnd-class.md#onxbuttondown)(UINT, uint, CPoint);|
|ON_WM_XBUTTONUP ()|afx_msg void [онксбуттонуп](../../mfc/reference/cwnd-class.md#onxbuttonup)(UINT, uint, CPoint);|

## <a name="see-also"></a>См. также раздел

[Схемы сообщений](../../mfc/reference/message-maps-mfc.md)<br/>
[Обработчики для сообщений WM_](../../mfc/reference/handlers-for-wm-messages.md)
