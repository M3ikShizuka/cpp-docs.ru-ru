---
description: 'Дополнительные сведения: указание библиотек DLL для задержки загрузки'
title: Задание библиотек DLL с отложенной загрузкой
ms.date: 11/04/2016
helpviewer_keywords:
- DELAYLOAD linker option
- delayed loading of DLLs
- delayed loading of DLLs, specifying
- /DELAYLOAD linker option
ms.assetid: 94cbecfe-7a42-40d1-a618-9f2786bac0d8
ms.openlocfilehash: ece96ea6f818c7e0bc6b6e032ce523e96a9f4ecb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97224548"
---
# <a name="specifying-dlls-to-delay-load"></a>Задание библиотек DLL с отложенной загрузкой

Можно указать, какие DLL следует отложить загрузку с помощью параметра [параметр/DELAYLOAD](delayload-delay-load-import.md): `dllname` компоновщика. Если вы не планируете использовать собственную версию вспомогательной функции, необходимо также связать программу с библиотекой delayimp.lib (для классических приложений) или dloadhelper.lib (для приложений Магазина).

Ниже приведен простой пример задержки загрузки библиотеки DLL.

```
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

Создание ОТЛАДОЧНОЙ версии проекта. Просмотрите код, используя отладчик, и обратите внимание, что файл user32.dll загружается только при вызове `MessageBox`.

## <a name="see-also"></a>См. также раздел

[Поддержка компоновщика для Delay-Loadedных библиотек DLL](linker-support-for-delay-loaded-dlls.md)
