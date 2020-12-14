---
description: 'Дополнительные сведения о: структура TOOLTIPTEXT'
title: Структура TOOLTIPTEXT
ms.date: 11/04/2016
f1_keywords:
- TOOLTIPTEXT
helpviewer_keywords:
- TOOLTIPTEXT structure [MFC]
- tool tips [MFC], notifications
ms.assetid: 547591bf-80f5-400e-a2a7-0708cfffbb5d
ms.openlocfilehash: 077d4c27392b626a0e9665851eadf227245029b6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97264301"
---
# <a name="tooltiptext-structure"></a>Структура TOOLTIPTEXT

При написании [обработчика уведомлений с помощью всплывающей подсказки](../mfc/handling-ttn-needtext-notification-for-tool-tips.md)необходимо использовать структуру **ToolTipText** . Элементы структуры **ToolTipText** :

```cpp
typedef struct {
    NMHDR     hdr;        // required for all WM_NOTIFY messages
    LPTSTR    lpszText;   // see below
    TCHAR     szText[80]; // buffer for tool tip text
    HINSTANCE hinst;      // see below
    UINT      uflags;     // flag indicating how to interpret the
                          // idFrom member of the NMHDR structure
                          // that is included in the structure
} TOOLTIPTEXT, FAR *LPTOOLTIPTEXT;
```

*hdr*<br/>
Определяет средство, которому требуется текст. Единственным элементом этой структуры может потребоваться идентификатор команды элемента управления. Идентификатор команды элемента управления будет находиться в элементе *идфром* структуры **NMHDR** , к которому можно получить доступ с помощью синтаксиса `hdr.idFrom` . Описание членов структуры **NMHDR** см. в разделе [NMHDR](/windows/win32/api/richedit/ns-richedit-nmhdr) .

*lpszText*<br/>
Адрес строки для получения текста инструмента.

*сзтекст*<br/>
Буфер, который получает текст подсказки. Приложение может скопировать текст в этот буфер в качестве альтернативы указанию строкового адреса.

*хинст*<br/>
Маркер экземпляра, который содержит строку, используемую в качестве текста подсказки для инструмента. Если *лпсзтекст* является адресом текста подсказки, этот элемент имеет значение null.

При обработке `TTN_NEEDTEXT` сообщения уведомления укажите строку, которая будет отображаться одним из следующих способов.

- Скопируйте текст в буфер, указанный элементом *сзтекст* .

- Скопируйте адрес буфера, который содержит текст, в элемент *лпсзтекст* .

- Скопируйте идентификатор строкового ресурса в элемент *лпсзтекст* и скопируйте Маркер экземпляра, который содержит ресурс, в элемент *хинст* .

## <a name="see-also"></a>См. также раздел

[Всплывающие подсказки в Windows, не являющиеся производными от CFrameWnd](../mfc/tool-tips-in-windows-not-derived-from-cframewnd.md)
