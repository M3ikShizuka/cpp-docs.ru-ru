---
description: Дополнительные сведения см. в статье рекомендации по выбору между ATL и MFC.
title: Рекомендации по выбору между ATL и MFC
ms.date: 11/04/2016
helpviewer_keywords:
- MFC, ATL support
- ATL, vs. MFC
ms.assetid: 269325bb-11a8-4330-ad2b-a14a2458679e
ms.openlocfilehash: 506df04ebbd3bc9079e1d40cf14773d9d9a6bd1a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97159158"
---
# <a name="recommendations-for-choosing-between-atl-and-mfc"></a>Рекомендации по выбору между ATL и MFC

При разработке компонентов и приложений можно выбрать один из двух подходов — ATL и MFC (библиотека Microsoft Foundation Class).

## <a name="using-atl"></a>Использование ATL

ATL — это быстрый и простой способ создания COM-компонента на C++ и сохранения небольшого объема. Используйте библиотеку ATL для создания элемента управления, если вам не нужны все встроенные функции, предоставляемые MFC автоматически.

## <a name="using-mfc"></a>Использование MFC

MFC позволяет создавать полные приложения, элементы управления ActiveX и активные документы. Если вы уже создали элемент управления с MFC, может потребоваться продолжить разработку в MFC. При создании нового элемента управления рассмотрите возможность использования ATL, если вам не нужны все встроенные функции MFC.

## <a name="using-atl-in-an-mfc-project"></a>Использование ATL в проекте MFC

Можно добавить поддержку использования ATL в существующем проекте MFC, запустив мастер. Дополнительные сведения см. [в разделе Добавление поддержки ATL в проект MFC](../mfc/reference/adding-atl-support-to-your-mfc-project.md).

## <a name="see-also"></a>См. также раздел

[Введение в ATL](../atl/introduction-to-atl.md)
