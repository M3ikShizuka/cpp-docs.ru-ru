---
description: 'Дополнительные сведения: WM_ обработчики сообщений: L-M'
title: Обработчики сообщений WM_ L — M
ms.date: 11/04/2016
f1_keywords:
- ON_WM_MENUSELECT
- ON_WM_MBUTTONDBLCLK
- ON_WM_MOUSEACTIVATE
- ON_WM_MOUSEMOVE
- ON_WM_MOVING
- ON_WM_LBUTTONUP
- ON_WM_LBUTTONDBLCLK
- ON_WM_MEASUREITEM
- ON_WM_MDIACTIVATE
- ON_WM_MOVE
- ON_WM_LBUTTONDOWN
- ON_WM_MBUTTONDOWN
- ON_WM_MENUCHAR
- ON_WM_MBUTTONUP
helpviewer_keywords:
- ON_WM_MENUSELECT [MFC]
- ON_WM_MBUTTONDBLCLK [MFC]
- ON_WM_MOVE [MFC]
- ON_WM_MOUSEACTIVATE [MFC]
- ON_WM_MBUTTONUP [MFC]
- ON_WM_MOUSEMOVE [MFC]
- ON_WM_MENUCHAR [MFC]
- ON_WM_MBUTTONDOWN [MFC]
- ON_WM_MEASUREITEM [MFC]
- ON_WM_MOVING [MFC]
- ON_WM_LBUTTONDOWN [MFC]
- ON_WM_MDIACTIVATE [MFC]
- ON_WM_LBUTTONDBLCLK [MFC]
- ON_WM_LBUTTONUP [MFC]
- WM_ messages
ms.assetid: 96ecaaf1-6d13-4e12-a454-535635967489
ms.openlocfilehash: 2044f8eeb74c75f92f42c6e0199820528f7c10c7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97218333"
---
# <a name="wm_-message-handlers-l---m"></a>Обработчики сообщений WM_ L — M

Следующие записи карт слева соответствуют прототипам функций справа:

|Запись Map|Прототип функции|
|---------------|------------------------|
|ON_WM_LBUTTONDBLCLK ()|afx_msg void [онлбуттондблклк](../../mfc/reference/cwnd-class.md#onlbuttondblclk)(uint, CPoint);|
|ON_WM_LBUTTONDOWN ()|afx_msg void [онлбуттондовн](../../mfc/reference/cwnd-class.md#onlbuttondown)(uint, CPoint);|
|ON_WM_LBUTTONUP ()|afx_msg void [онлбуттонуп](../../mfc/reference/cwnd-class.md#onlbuttonup)(uint, CPoint);|
|ON_WM_MBUTTONDBLCLK ()|afx_msg void [онмбуттондблклк](../../mfc/reference/cwnd-class.md#onmbuttondblclk)(uint, CPoint);|
|ON_WM_MBUTTONDOWN ()|afx_msg void [онмбуттондовн](../../mfc/reference/cwnd-class.md#onmbuttondown)(uint, CPoint);|
|ON_WM_MBUTTONUP ()|afx_msg void [онмбуттонуп](../../mfc/reference/cwnd-class.md#onmbuttonup)(uint, CPoint);|
|ON_WM_MDIACTIVATE ()|afx_msg void [онмдиактивате](../../mfc/reference/cwnd-class.md#onmdiactivate)(bool, CWnd \* , CWnd \* );|
|ON_WM_MEASUREITEM ()|afx_msg void [онмеасуреитем](../../mfc/reference/cwnd-class.md#onmeasureitem)(лпмеасуреитемструкт);|
|ON_WM_MENUCHAR ()|afx_msg LONG [онменучар](../../mfc/reference/cwnd-class.md#onmenuchar)(UINT, uint, кмену \* );|
|ON_WM_MENUDRAG ()|afx_msg UINT [онменудраг](../../mfc/reference/cwnd-class.md#onmenudrag)(uint, кмену \* );|
|ON_WM_MENUGETOBJECT ()|afx_msg UINT [онменужетобжект](../../mfc/reference/cwnd-class.md#onmenugetobject)(менужетобжектинфо \* );|
|ON_WM_MENURBUTTONUP ()|afx_msg void [онменурбуттонуп](../../mfc/reference/cwnd-class.md#onmenurbuttonup)(uint, кмену \* );|
|ON_WM_MENUSELECT ()|afx_msg void [онменуселект](../../mfc/reference/cwnd-class.md#onmenuselect)(UINT, uint, HMENU);|
|ON_WM_MOUSEACTIVATE ()|afx_msg int [онмаусеактивате](../../mfc/reference/cwnd-class.md#onmouseactivate)(CWnd \* , uint, uint);|
|ON_WM_MOUSEHOVER ()|afx_msg void [онмаусеховер](../../mfc/reference/cwnd-class.md#onmousehover)(uint, CPoint);|
|ON_WM_MOUSEHWHEEL ()|afx_msg void [онмаусехвхил](../../mfc/reference/cwnd-class.md#onmousehwheel)(uint, Short, CPoint);|
|ON_WM_MOUSELEAVE ()|afx_msg void [онмауселеаве](../../mfc/reference/cwnd-class.md#onmouseleave)();|
|ON_WM_MOUSEMOVE ()|afx_msg void [OnMouseMove](../../mfc/reference/cwnd-class.md#onmousemove)(uint, CPoint);|
|ON_WM_MOUSEWHEEL ()|afx_msg BOOL [онмаусевхил](../../mfc/reference/cwnd-class.md#onmousewheel)(uint, Short, CPoint);|
|ON_WM_MOVE ()|afx_msg void [OnMove](../../mfc/reference/cwnd-class.md#onmove)(int, int);|
|ON_WM_MOVING ()|afx_msg void [onmoving](../../mfc/reference/cwnd-class.md#onmoving)(uint, лпрект);|

## <a name="see-also"></a>См. также раздел

[Схемы сообщений](../../mfc/reference/message-maps-mfc.md)<br/>
[Обработчики для сообщений WM_](../../mfc/reference/handlers-for-wm-messages.md)
