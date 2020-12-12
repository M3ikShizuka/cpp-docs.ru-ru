---
description: 'Дополнительные сведения: WM_ обработчики сообщений: F-K'
title: Обработчики сообщений WM_ F — K
ms.date: 11/27/2018
f1_keywords:
- ON_WM_FONTCHANGE
- ON_WM_ICONERASEBKGND
- ON_WM_KEYDOWN
- ON_WM_GETMINMAXINFO
- ON_WM_KEYUP
- ON_WM_HSCROLL
- ON_WM_KILLFOCUS
- ON_WM_HSCROLLCLIPBOARD
- ON_WM_GETDLGCODE
- ON_WM_HELPINFO
- ON_WM_INITMENUPOPUP
- ON_WM_INITMENU
helpviewer_keywords:
- ON_WM_HELPINFO [MFC]
- ON_WM_KILLFOCUS [MFC]
- ON_WM_GETMINMAXINFO [MFC]
- ON_WM_KEYUP [MFC]
- ON_WM_HSCROLL [MFC]
- ON_WM_INITMENUPOPUP [MFC]
- ON_WM_FONTCHANGE [MFC]
- ON_WM_ICONERASEBKGND [MFC]
- ON_WM_GETDLGCODE [MFC]
- ON_WM_HSCROLLCLIPBOARD [MFC]
- ON_WM_INITMENU [MFC]
- WM_ messages [MFC]
- ON_WM_KEYDOWN [MFC]
ms.assetid: 0e7de191-1499-499f-859c-62742797808e
ms.openlocfilehash: 91fb2448862dd70a852191f021244571813b0102
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97218346"
---
# <a name="wm_-message-handlers-f---k"></a>Обработчики сообщений WM_ F — K

Следующие записи карт слева соответствуют прототипам функций справа:

|Запись Map|Прототип функции|
|---------------|------------------------|
|ON_WM_FONTCHANGE ()|afx_msg void [онфонтчанже](../../mfc/reference/cwnd-class.md#onfontchange)();|
|ON_WM_GETDLGCODE ()|afx_msg UINT [онжетдлгкоде](../../mfc/reference/cwnd-class.md#ongetdlgcode)();|
|ON_WM_GETMINMAXINFO ()|afx_msg void [онжетминмаксинфо](../../mfc/reference/cwnd-class.md#ongetminmaxinfo)(минмаксинфо *);|
|ON_WM_HELPINFO ()|afx_msg BOOL [онхелпинфо](../../mfc/reference/cwnd-class.md#onhelpinfo)(HELPINFO *);|
|ON_WM_HOTKEY ()|afx_msg void [onhotkey](../../mfc/reference/cwnd-class.md#onhotkey)(UINT, UINT, uint);|
|ON_WM_HSCROLL ()|afx_msg void [онхскролл](../../mfc/reference/cwnd-class.md#onhscroll)(UINT, uint, CWnd *);|
|ON_WM_HSCROLLCLIPBOARD ()|afx_msg void [онхскроллклипбоард](../../mfc/reference/cwnd-class.md#onhscrollclipboard)(CWnd *, UINT, uint);|
|ON_WM_ICONERASEBKGND ()|afx_msg void [ониконерасебкгнд](../../mfc/reference/cwnd-class.md#oniconerasebkgnd)(CDC *);|
|ON_WM_INITMENU ()|afx_msg void [онинитмену](../../mfc/reference/cwnd-class.md#oninitmenu)(кмену *);|
|ON_WM_INITMENUPOPUP ()|afx_msg void [онинитменупопуп](../../mfc/reference/cwnd-class.md#oninitmenupopup)(кмену *, uint, bool);|
|ON_WM_INPUT ()|afx_msg void [онравинпут](../../mfc/reference/cwnd-class.md#onrawinput)(uint, хравинпут);|
|ON_WM_INPUT_DEVICE_CHANGE ()|afx_msg void [онинпутдевицечанже](../../mfc/reference/cwnd-class.md#oninputdevicechange)(неподписанный короткий);|
|ON_WM_INPUTLANGCHANGE ()|afx_msg void [онинпутлангчанже](../../mfc/reference/cwnd-class.md#oninputlangchange)(Byte, uint);|
|ON_WM_INPUTLANGCHANGEREQUEST ()|afx_msg void [онинпутлангчанжерекуест](../../mfc/reference/cwnd-class.md#oninputlangchangerequest)(uint, HKL);|
|ON_WM_KEYDOWN ()|afx_msg void [OnKeyDown](../../mfc/reference/cwnd-class.md#onkeydown)(UINT, UINT, uint);|
|ON_WM_KEYUP ()|afx_msg void [онкэйуп](../../mfc/reference/cwnd-class.md#onkeyup)(UINT, UINT, uint);|
|ON_WM_KILLFOCUS ()|afx_msg void [онкиллфокус](../../mfc/reference/cwnd-class.md#onkillfocus)(CWnd *);|

## <a name="see-also"></a>См. также раздел

[Схемы сообщений](../../mfc/reference/message-maps-mfc.md)<br/>
[Обработчики для сообщений WM_](../../mfc/reference/handlers-for-wm-messages.md)
