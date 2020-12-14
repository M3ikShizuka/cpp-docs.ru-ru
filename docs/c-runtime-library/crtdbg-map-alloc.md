---
description: 'Дополнительные сведения: _CRTDBG_MAP_ALLOC'
title: _CRTDBG_MAP_ALLOC
ms.date: 11/04/2016
f1_keywords:
- CRTDBG_MAP_ALLOC
- _CRTDBG_MAP_ALLOC
helpviewer_keywords:
- _CRTDBG_MAP_ALLOC macro
- memory allocation, in debug builds
- CRTDBG_MAP_ALLOC macro
ms.assetid: 435242b8-caea-4063-b765-4a608200312b
ms.openlocfilehash: e2747f6da04c019b551e68c78f6f1448c48093f1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97224274"
---
# <a name="_crtdbg_map_alloc"></a>_CRTDBG_MAP_ALLOC

Когда в отладочной версии приложения определен флаг **_CRTDBG_MAP_ALLOC**, базовые версии функций кучи напрямую сопоставляется с их отладочными версиями. Этот флаг используется в файле Crtdbg.h для выполнения сопоставления. Этот флаг доступен, только если флаг [_DEBUG](../c-runtime-library/debug.md) был определен в приложении.

Дополнительные сведения об использовании отладочной и базовой версий функции кучи см. в разделе [Использование отладочной и базовой версий](/visualstudio/debugger/debug-versions-of-heap-allocation-functions).

## <a name="see-also"></a>См. также раздел

[Управляющие флаги](../c-runtime-library/control-flags.md)
