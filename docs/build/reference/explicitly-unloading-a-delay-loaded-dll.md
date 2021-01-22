---
description: 'Дополнительные сведения: Явная выгрузка DLL с отложенной загрузкой'
title: Явная выгрузка библиотеки DLL, загруженной с задержкой
ms.date: 01/19/2021
helpviewer_keywords:
- /DELAY:UNLOAD linker option
- DELAY:UNLOAD linker option
- __FUnloadDelayLoadedDLL2
- delayed loading of DLLs, unloading
ms.openlocfilehash: b4e137f293c6497e234a7bb93bd16b5bb6887741
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98666892"
---
# <a name="explicitly-unload-a-delay-loaded-dll"></a>Явная выгрузка библиотеки DLL, загруженной с задержкой

[`/delay:unload`](delay-delay-load-import-settings.md)Параметр компоновщика позволяет коду явно выгружать БИБЛИОТЕКУ DLL, которая была загружена с задержкой. По умолчанию, когда код выгружает библиотеку DLL, импорт с отложенной загрузкой остается в таблице адресов импорта (IAT). Однако при использовании **`/delay:unload`** в командной строке компоновщика вспомогательная функция поддерживает явную выгрузку библиотеки DLL с помощью `__FUnloadDelayLoadedDLL2` вызова и СБРАСЫВАЕТ объект IAT в исходную форму. Недопустимые указатели будут перезаписаны. IAT — это поле в [`ImgDelayDescr`](calling-conventions-parameters-and-return-type.md) структуре, содержащее адрес копии ИСХОДНОЙ IAT, если она существует.

## <a name="example"></a>Пример

### <a name="code"></a>Код

```C
// link with /link /DELAYLOAD:MyDLL.dll /DELAY:UNLOAD
#include <windows.h>
#include <delayimp.h>
#include "MyDll.h"
#include <stdio.h>

#pragma comment(lib, "delayimp")
#pragma comment(lib, "MyDll")
int main()
{
    BOOL TestReturn;
    // MyDLL.DLL will load at this point
    fnMyDll();

    //MyDLL.dll will unload at this point
    TestReturn = __FUnloadDelayLoadedDLL2("MyDll.dll");

    if (TestReturn)
        printf_s("\nDLL was unloaded");
    else
        printf_s("\nDLL was not unloaded");
}
```

### <a name="comments"></a>Комментарии

Важные примечания по выгрузке библиотеки DLL с отложенной загрузкой:

- Реализацию функции можно найти `__FUnloadDelayLoadedDLL2` в файле *`delayhlp.cpp`* в *`include`* каталоге VC.

- *`name`* Параметр `__FUnloadDelayLoadedDLL2` функции должен точно соответствовать (включая регистр), который содержит библиотека импорта. (Эта строка также находится в таблице импорта в изображении.) Содержимое библиотеки импорта можно просмотреть с помощью команды [`DUMPBIN /DEPENDENTS`](dependents.md) . Если вы предпочитаете совпадение строк без учета регистра, можно обновить `__FUnloadDelayLoadedDLL2` для использования одной из строковых функций CRT без учета регистра или вызова Windows API.

Дополнительные сведения см. [в разделе выгрузка библиотеки DLL, загруженной с задержкой](unloading-a-delay-loaded-dll.md).

## <a name="see-also"></a>См. также раздел

[Поддержка компоновщика для библиотек DLL с отложенной загрузкой](linker-support-for-delay-loaded-dlls.md)
