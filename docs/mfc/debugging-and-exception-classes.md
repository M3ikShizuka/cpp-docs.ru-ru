---
description: 'Дополнительные сведения: Отладка и классы исключений'
title: Классы для отладки и работы с исключениями
ms.date: 11/04/2016
f1_keywords:
- vc.classes.debug
helpviewer_keywords:
- debugging [MFC], exception classes
- debugging [MFC], classes for debugging
ms.assetid: 0d158efd-2e62-452e-9d2a-d3c30dfee7f9
ms.openlocfilehash: 2c14ea8d51fd1b63427ad1495e711a906e013ea4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97291120"
---
# <a name="debugging-and-exception-classes"></a>Классы для отладки и работы с исключениями

Эти классы обеспечивают поддержку отладки выделения динамической памяти и передачи сведений об исключениях из функции, в которой исключение вызывается для функции, в которой оно перехвачено.

Используйте классы [CDumpContext](reference/cdumpcontext-class.md) и [CMemoryState](reference/cmemorystate-structure.md) во время разработки, чтобы упростить отладку, как описано в разделе [Отладка приложений MFC](/visualstudio/debugger/mfc-debugging-techniques). Используйте [крунтимекласс](reference/cruntimeclass-structure.md) , чтобы определить класс любого объекта во время выполнения, как описано в статье [доступ к Run-Time сведениям о классе](accessing-run-time-class-information.md). Платформа использует `CRuntimeClass` для динамического создания объектов определенного класса.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](class-library-overview.md)
