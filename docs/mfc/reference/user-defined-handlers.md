---
description: 'Дополнительные сведения: обработчики User-Defined'
title: Пользовательские обработчики
ms.date: 11/04/2016
helpviewer_keywords:
- ON_REGISTERED_MESSAGE macro [MFC]
- ON_MESSAGE macro [MFC]
- user-defined handlers [MFC]
ms.assetid: 99478294-bef0-4ba7-a369-25a6abdcdb62
ms.openlocfilehash: 8a3b7389d7388fb54ae39d3b1805594b64556652
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97218528"
---
# <a name="user-defined-handlers"></a>Пользовательские обработчики

Следующие записи Map соответствуют прототипам функций.

|Запись Map|Прототип функции|
|---------------|------------------------|
|ON_MESSAGE ( \<message> , \<memberFxn> )|afx_msg LRESULT Мемберфксн (WPARAM, LPARAM);|
|ON_REGISTERED_MESSAGE ( \<nMessageVariable> , \<memberFxn> )|afx_msg LRESULT Мемберфксн (WPARAM, LPARAM);|
|ON_THREAD_MESSAGE ( \<message> , \<memberFxn> )|afx_msg void Мемберфксн (WPARAM, LPARAM);|
|ON_REGISTERED_THREAD_MESSAGE ( \<nMessageVariable> , \<memberFxn> )|afx_msg void Мемберфксн (WPARAM, LPARAM);|

## <a name="see-also"></a>См. также раздел

[Схемы сообщений](../../mfc/reference/message-maps-mfc.md)<br/>
[Обработчики для сообщений WM_](../../mfc/reference/handlers-for-wm-messages.md)
