---
description: 'Дополнительные сведения: WM_ обработчики сообщений: A-C'
title: Обработчики сообщений WM_ A — C
ms.date: 11/04/2016
f1_keywords:
- ON_WM_CREATE
- ON_WM_COMPACTING
- ON_WM_CHARTOITEM
- ON_WM_ASKCBFORMATNAME
- ON_WM_CTLCOLOR
- ON_WM_COMPAREITEM
- ON_WM_CHILDACTIVATE
- ON_WM_CONTEXTMENU
- ON_WM_ACTIVATE
- ON_WM_CANCELMODE
- ON_WM_CLOSE
- ON_WM_CAPTURECHANGED
- ON_WM_ACTIVATEAPP
- ON_WM_CHAR
- ON_WM_CHANGECBCHAIN
helpviewer_keywords:
- ON_WM_COMPACTING [MFC]
- ON_WM_COMPAREITEM [MFC]
- ON_WM_CLOSE [MFC]
- ON_WM_CTLCOLOR [MFC]
- ON_WM_CHAR [MFC]
- ON_WM_CAPTURECHANGED [MFC]
- ON_WM_CHARTOITEM [MFC]
- ON_WM_CREATE [MFC]
- ON_WM_ACTIVATE [MFC]
- ON_WM_CONTEXTMENU [MFC]
- ON_WM_CANCELMODE [MFC]
- ON_WM_ASKCBFORMATNAME [MFC]
- ON_WM_CHILDACTIVATE [MFC]
- WM_ messages [MFC]
- ON_WM_ACTIVATEAPP [MFC]
- ON_WM_CHANGECBCHAIN
ms.assetid: 4e315896-d646-4b87-b0ab-41a4a753b045
ms.openlocfilehash: 898635961e3fc1ad3df571e813bcfef629318446
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97218450"
---
# <a name="wm_-message-handlers-a---c"></a>Обработчики сообщений WM_ A — C

Следующие записи карт слева соответствуют прототипам функций справа:

|Запись Map|Прототип функции|
|---------------|------------------------|
|ON_WM_ACTIVATE ()|afx_msg void [OnActivate](../../mfc/reference/cwnd-class.md#onactivate)(uint, CWnd \* , bool);|
|ON_WM_ACTIVATEAPP ()|afx_msg void [OnActivateApp](../../mfc/reference/cwnd-class.md#onactivateapp)(bool, DWORD);|
|ON_WM_APPCOMMAND ()|afx_msg void [онаппкомманд](../../mfc/reference/cwnd-class.md#onappcommand)(CWnd \* , uint, uint, uint);|
|ON_WM_ASKCBFORMATNAME ()|afx_msg void [онасккбформатнаме](../../mfc/reference/cwnd-class.md#onaskcbformatname)(uint, LPSTR);|
|ON_WM_CANCELMODE ()|afx_msg void [онканцелмоде](../../mfc/reference/cwnd-class.md#oncancelmode)();|
|ON_WM_CAPTURECHANGED ()|afx_msg void [онкаптуречанжед](../../mfc/reference/cwnd-class.md#oncapturechanged)(CWnd \* );|
|ON_WM_CHANGECBCHAIN ()|afx_msg void [ончанжекбчаин](../../mfc/reference/cwnd-class.md#onchangecbchain)(HWND, HWND);|
|ON_WM_CHAR ()|afx_msg void [OnChar](../../mfc/reference/cwnd-class.md#onchar)(UINT, UINT, uint);|
|ON_WM_CHARTOITEM ()|afx_msg int [ончартоитем](../../mfc/reference/cwnd-class.md#onchartoitem)(uint, CWnd \* , uint);|
|ON_WM_CHILDACTIVATE ()|afx_msg void [ончилдактивате](../../mfc/reference/cwnd-class.md#onchildactivate)();|
|ON_WM_CLIPBOARDUPDATE ()|afx_msg void [онклипбоардупдате](../../mfc/reference/cwnd-class.md#onclipboardupdate)();|
|ON_WM_CLOSE ()|afx_msg void [OnClose](../../mfc/reference/cwnd-class.md#onclose)();|
|ON_WM_COMPACTING ()|afx_msg void для [сжатия](../../mfc/reference/cwnd-class.md#oncompacting)(UINT);|
|ON_WM_COMPAREITEM ()|afx_msg int [онкомпареитем](../../mfc/reference/cwnd-class.md#oncompareitem)(лпкомпареитемструкт);|
|ON_WM_CONTEXTMENU ()|afx_msg void [oncontextmenu](../../mfc/reference/cwnd-class.md#oncontextmenu)(CWnd \* , CPoint);|
|ON_WM_COPYDATA ()|afx_msg BOOL [онкопидата](../../mfc/reference/cwnd-class.md#oncopydata)(CWnd \* приводится, копидатаструкт \* пкопидатаструкт);|
|ON_WM_CREATE ()|afx_msg int [OnCreate](../../mfc/reference/cwnd-class.md#oncreate)(лпкреатеструкт);|
|ON_WM_CTLCOLOR ()|afx_msg ХБРУШ [онктлколор](../../mfc/reference/cwnd-class.md#onctlcolor)(CDC \* , CWnd \* , uint);|

## <a name="see-also"></a>См. также раздел

[Схемы сообщений](../../mfc/reference/message-maps-mfc.md)<br/>
[Обработчики для сообщений WM_](../../mfc/reference/handlers-for-wm-messages.md)
