---
description: Дополнительные сведения см. в статье обработчики окна списка
title: Обработчики списков
ms.date: 11/04/2016
f1_keywords:
- ON_LBN_DBLCLK
- ON_LBN_ERRSPACE
- ON_LBN_SETFOCUS
- ON_LBN_SELCHANGE
- ON_LBN_KILLFOCUS
helpviewer_keywords:
- list boxes [MFC], list box handlers
- ON_LBN_KILLFOCUS
- ON_LBN_ERRSPACE
- ON_LBN_SELCHANGE
- ON_LBN_SETFOCUS
- ON_LBN_DBLCLK
ms.assetid: e4e54412-2167-436a-883b-5dcad01820b8
ms.openlocfilehash: 190833fed725009729a5895f3b302da4c897fb51
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97219425"
---
# <a name="list-box-handlers"></a>Обработчики списков

Следующие записи карт имеют соответствующий прототип функции.

|Запись Map|Прототип функции|
|---------------|------------------------|
|ON_LBN_DBLCLK ( \<id> , \<memberFxn> )|afx_msg void Мемберфксн ();|
|ON_LBN_ERRSPACE ( \<id> , \<memberFxn> )|afx_msg void Мемберфксн ();|
|ON_LBN_KILLFOCUS ( \<id> , \<memberFxn> )|afx_msg void Мемберфксн ();|
|ON_LBN_SELCHANGE ( \<id> , \<memberFxn> )|afx_msg void Мемберфксн ();|
|ON_LBN_SETFOCUS ( \<id> , \<memberFxn> )|afx_msg void Мемберфксн ();|

## <a name="see-also"></a>См. также раздел

[Схемы сообщений](../../mfc/reference/message-maps-mfc.md)
