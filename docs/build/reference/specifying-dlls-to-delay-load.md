---
description: Дополнительные сведения об указании библиотек DLL для задержки загрузки
title: Указание библиотек DLL для задержки загрузки
ms.date: 01/19/2021
helpviewer_keywords:
- DELAYLOAD linker option
- delayed loading of DLLs
- delayed loading of DLLs, specifying
- /DELAYLOAD linker option
ms.openlocfilehash: de8c2e3cb9605cbc6dbc215a0449348c12295c17
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98667499"
---
# <a name="specify-dlls-to-delay-load"></a>Указание библиотек DLL для задержки загрузки

С помощью параметра компоновщика можно указать, какие библиотеки DLL следует отложить загрузку [`/delayload:dllname`](delayload-delay-load-import.md) . Если вы не планируете использовать собственную версию вспомогательной функции, необходимо также связать программу с *`delayimp.lib`* (для классических приложений) или *`dloadhelper.lib`* (для приложений UWP).

Ниже приведен простой пример отложенной загрузки библиотеки DLL:

```cpp
// cl t.cpp user32.lib delayimp.lib  /link /DELAYLOAD:user32.dll
#include <windows.h>
// uncomment these lines to remove .libs from command line
// #pragma comment(lib, "delayimp")
// #pragma comment(lib, "user32")

int main() {
   // user32.dll will load at this point
   MessageBox(NULL, "Hello", "Hello", MB_OK);
}
```

Создание ОТЛАДОЧНОЙ версии проекта. Пошаговое выполнение кода с помощью отладчика, и вы заметите, что *`user32.dll`* загружается только при вызове `MessageBox` .

## <a name="see-also"></a>См. также раздел

[Поддержка компоновщика для библиотек DLL с отложенной загрузкой](linker-support-for-delay-loaded-dlls.md)
