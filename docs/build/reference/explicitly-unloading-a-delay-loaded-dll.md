---
description: 'Дополнительные сведения: Явная выгрузка библиотеки DLL Delay-Loaded'
title: Явная выгрузка библиотеки DLL, загруженной с задержкой
ms.date: 11/04/2016
helpviewer_keywords:
- /DELAY:UNLOAD linker option
- DELAY:UNLOAD linker option
- __FUnloadDelayLoadedDLL2
- delayed loading of DLLs, unloading
ms.assetid: 1c4c5172-fd06-45d3-9e4f-f12343176b3c
ms.openlocfilehash: 03df08487acc1be05226021d6b7c1593eb0f031b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192386"
---
# <a name="explicitly-unloading-a-delay-loaded-dll"></a>Явная выгрузка библиотеки DLL, загруженной с задержкой

Параметр компоновщика [/delay](delay-delay-load-import-settings.md): unload позволяет выгрузить библиотеку DLL, которая была загружена с задержкой. По умолчанию, когда код выгружает библиотеку DLL (с использованием/Delay: Load и **__FUnloadDelayLoadedDLL2**), импортированные с задержкой импорты остаются в таблице адресов импорта (IAT). Однако при использовании параметра/delay: unload в командной строке компоновщика вспомогательная функция будет поддерживать явную выгрузку библиотеки DLL, перестроив IAT на исходную форму. Теперь недопустимые указатели будут перезаписаны. IAT — это поле в [имгделайдескр](calling-conventions-parameters-and-return-type.md) , содержащее адрес копии исходной IAT (если она существует).

## <a name="example"></a>Пример

### <a name="code"></a>Код

```
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

- Реализацию функции **__FUnloadDelayLoadedDLL2** можно найти в файле \VC7\INCLUDE\DELAYHLP. CPP.

- Параметр Name функции **__FUnloadDelayLoadedDLL2** должен точно совпадать (включая регистр), что содержится в библиотеке импорта (эта строка также находится в таблице импорта на изображении). Содержимое библиотеки импорта можно просмотреть с помощью [dumpbin/депендентс](dependents.md). Если требуется совпадение строк без учета регистра, можно обновить **__FUnloadDelayLoadedDLL2** , чтобы использовать одну из СТРОКОВЫХ функций CRT или вызов Windows API.

Дополнительные сведения см. [в разделе Выгрузка Delay-Loaded DLL](unloading-a-delay-loaded-dll.md) .

## <a name="see-also"></a>См. также раздел

[Поддержка компоновщика для Delay-Loadedных библиотек DLL](linker-support-for-delay-loaded-dlls.md)
