---
description: 'Дополнительные сведения о: SDI и MDI'
title: SDI и MDI
ms.date: 11/04/2016
helpviewer_keywords:
- frame windows [MFC], SDI applications
- frame windows [MFC], MDI applications
- MFC, windows
- single document interface (SDI) [MFC], applications
- MDI [MFC], vs. SDI
ms.assetid: bb7239d9-4759-4f63-bfff-44a04b48c067
ms.openlocfilehash: bfa54db04a657507b4b491ada6e8f08d17c2d1c9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97217787"
---
# <a name="sdi-and-mdi"></a>SDI и MDI

MFC упрощает работу с приложениями с однодокументным интерфейсом (SDI) и многодокументным интерфейсом (MDI).

Приложения SDI допускают одновременно только одно окно документа с открытым фреймом. Приложения MDI позволяют открывать несколько окон фрейма документа в одном экземпляре приложения. Приложение MDI имеет окно, в котором можно открыть несколько дочерних окон MDI, которые сами являются окнами фрейма, и каждый из которых содержит отдельный документ. В некоторых приложениях дочерние окна могут иметь различные типы, такие как окна диаграмм и окна электронных таблиц. В этом случае строка меню может измениться при активации дочерних MDI-окон различных типов.

> [!NOTE]
> В Windows 95 и более поздних версиях приложения обычно являются SDI, поскольку операционная система использует представление Document-Center.

Дополнительные сведения см. [в разделе документы, представления и платформа](../mfc/documents-views-and-the-framework.md).

## <a name="see-also"></a>См. также раздел

[Использование классов для написания приложений для Windows](../mfc/using-the-classes-to-write-applications-for-windows.md)
