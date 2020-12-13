---
description: Дополнительные сведения см. в статье как загрузить ресурс ленты из приложения MFC.
title: Практическое руководство. Загрузка ресурса ленты из приложения MFC
ms.date: 11/04/2016
helpviewer_keywords:
- ribbon resource [MFC], loading
ms.assetid: 1c76bb8f-6345-414a-9f3f-128815ceadc5
ms.openlocfilehash: 231acbd475bf84b2623eb44f9a3500ab94145d06
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330189"
---
# <a name="how-to-load-a-ribbon-resource-from-an-mfc-application"></a>Практическое руководство. Загрузка ресурса ленты из приложения MFC

Чтобы использовать в приложении ресурс ленты, измените приложение, чтобы загрузить ресурс ленты.

### <a name="to-load-a-ribbon-resource"></a>Загрузка ресурса ленты

1. Объявите `Ribbon Control` объект в `CMainFrame` классе.

```
    CMFCRibbonBar m_wndRibbonBar;
```

1. В `CMainFrame::OnCreate` Создайте и инициализируйте элемент управления Ribbon.

```
    if (!m_wndRibbonBar.Create (this))
{
    return -1;
}

    if (!m_wndRibbonBar.LoadFromResource(IDR_RIBBON))
{
    return -1;
}
```

## <a name="see-also"></a>См. также раздел

[Конструктор лент (MFC)](ribbon-designer-mfc.md)
