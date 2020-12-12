---
description: 'Дополнительные сведения: WM_ обработчики сообщений: N-O'
title: Обработчики сообщений WM_ N — O
ms.date: 11/04/2016
f1_keywords:
- ON_WM_NCHITTEST
- ON_WM_NCLBUTTONDOWN
- ON_WM_NCCALCSIZE
- ON_WM_NCLBUTTONUP
- ON_WM_NCPAINT
- ON_WM_NCMBUTTONUP
- ON_WM_NCCREATE
- ON_WM_NCACTIVATE
- ON_WM_NCMOUSEMOVE
- ON_WM_NCRBUTTONDBLCLK
- ON_WM_NCLBUTTONDBLCLK
- ON_WM_NCDESTROY
- ON_WM_NCMBUTTONDBLCLK
- ON_WM_NCRBUTTONDOWN
- ON_WM_NCRBUTTONUP
- ON_WM_NCMBUTTONDOWN
helpviewer_keywords:
- ON_WM_NCCALCSIZE [MFC]
- ON_WM_NCMBUTTONDOWN [MFC]
- ON_WM_NCRBUTTONDBLCLK [MFC]
- ON_WM_NCMBUTTONDBLCLK [MFC]
- ON_WM_NCLBUTTONDBLCLK [MFC]
- ON_WM_NCDESTROY [MFC]
- ON_WM_NCRBUTTONDOWN [MFC]
- ON_WM_NCLBUTTONDOWN [MFC]
- ON_WM_NCCREATE [MFC]
- ON_WM_NCRBUTTONUP [MFC]
- ON_WM_NCLBUTTONUP [MFC]
- ON_WM_NCPAINT [MFC]
- ON_WM_NCACTIVATE [MFC]
- ON_WM_NCHITTEST [MFC]
- ON_WM_NCMOUSEMOVE [MFC]
- ON_WM_NCMBUTTONUP [MFC]
- WM_ messages
ms.assetid: 4efd1cda-b642-4e8b-89e8-73255fa70d77
ms.openlocfilehash: 2f70bd0d019b4cdc9557c87c3ae0bb51e330723f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97218320"
---
# <a name="wm_-message-handlers-n---o"></a>Обработчики сообщений WM_ N — O

Следующие записи карт слева соответствуют прототипам функций справа:

|Запись Map|Прототип функции|
|---------------|------------------------|
|ON_WM_NCACTIVATE ()|afx_msg BOOL [оннкактивате](../../mfc/reference/cwnd-class.md#onncactivate)(bool);|
|ON_WM_NCCALCSIZE ()|afx_msg void [оннккалксизе](../../mfc/reference/cwnd-class.md#onnccalcsize)(BOOL, NCCALCSIZE_PARAMS FAR *);|
|ON_WM_NCCREATE ()|afx_msg BOOL [оннккреате](../../mfc/reference/cwnd-class.md#onnccreate)(лпкреатеструкт);|
|ON_WM_NCDESTROY ()|afx_msg void [OnNcDestroy](../../mfc/reference/cwnd-class.md#onncdestroy)();|
|ON_WM_NCHITTEST ()|afx_msg LRESULT [оннчиттест](../../mfc/reference/cwnd-class.md#onnchittest)(CPoint);|
|ON_WM_NCLBUTTONDBLCLK ()|afx_msg void [оннклбуттондблклк](../../mfc/reference/cwnd-class.md#onnclbuttondblclk)(uint, CPoint);|
|ON_WM_NCLBUTTONDOWN ()|afx_msg void [оннклбуттондовн](../../mfc/reference/cwnd-class.md#onnclbuttondown)(uint, CPoint);|
|ON_WM_NCLBUTTONUP ()|afx_msg void [оннклбуттонуп](../../mfc/reference/cwnd-class.md#onnclbuttonup)(uint, CPoint);|
|ON_WM_NCMBUTTONDBLCLK ()|afx_msg void [оннкмбуттондблклк](../../mfc/reference/cwnd-class.md#onncmbuttondblclk)(uint, CPoint);|
|ON_WM_NCMBUTTONDOWN ()|afx_msg void [оннкмбуттондовн](../../mfc/reference/cwnd-class.md#onncmbuttondown)(uint, CPoint);|
|ON_WM_NCMBUTTONUP ()|afx_msg void [оннкмбуттонуп](../../mfc/reference/cwnd-class.md#onncmbuttonup)(uint, CPoint);|
|ON_WM_NCMOUSEHOVER ()|afx_msg void [оннкмаусеховер](../../mfc/reference/cwnd-class.md#onncmousehover)(uint, CPoint);|
|ON_WM_NCMOUSELEAVE ()|afx_msg void [оннкмауселеаве](../../mfc/reference/cwnd-class.md#onncmouseleave)();|
|ON_WM_NCMOUSEMOVE ()|afx_msg void [оннкмаусемове](../../mfc/reference/cwnd-class.md#onncmousemove)(uint, CPoint);|
|ON_WM_NCPAINT ()|afx_msg void [оннкпаинт](../../mfc/reference/cwnd-class.md#onncpaint)();|
|ON_WM_NCRBUTTONDBLCLK ()|afx_msg void [оннкрбуттондблклк](../../mfc/reference/cwnd-class.md#onncrbuttondblclk)(uint, CPoint);|
|ON_WM_NCRBUTTONDOWN ()|afx_msg void [оннкрбуттондовн](../../mfc/reference/cwnd-class.md#onncrbuttondown)(uint, CPoint);|
|ON_WM_NCRBUTTONUP ()|afx_msg void [оннкрбуттонуп](../../mfc/reference/cwnd-class.md#onncrbuttonup)(uint, CPoint);|
|ON_WM_NCXBUTTONDBLCLK ()|void [оннкксбуттондблклк](../../mfc/reference/cwnd-class.md#onncxbuttondblclk)(Short, uint, CPoint);|
|ON_WM_NCXBUTTONDOWN ()|afx_msg void [оннкксбуттондовн](../../mfc/reference/cwnd-class.md#onncxbuttondown)(Short, uint, CPoint);|
|ON_WM_NCXBUTTONUP ()|afx_msg void [оннкксбуттонуп](../../mfc/reference/cwnd-class.md#onncxbuttonup)(Short, uint, CPoint);|
|ON_WM_NEXTMENU ()|afx_msg void [оннекстмену](../../mfc/reference/cwnd-class.md#onnextmenu)(uint, лпмдинекстмену);|
|ON_WM_NOTIFYFORMAT ()|afx_msg UINT [оннотифиформат](../../mfc/reference/cwnd-class.md#onnotifyformat)(CWnd *, uint);|

## <a name="see-also"></a>См. также раздел

[Схемы сообщений](../../mfc/reference/message-maps-mfc.md)<br/>
[Обработчики для сообщений WM_](../../mfc/reference/handlers-for-wm-messages.md)
