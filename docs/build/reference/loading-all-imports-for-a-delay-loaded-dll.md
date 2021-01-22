---
description: Дополнительные сведения о загрузке всех импортов для DLL с отложенной загрузкой
title: Загрузка всех импортов для DLL с отложенной загрузкой
ms.date: 01/19/2021
helpviewer_keywords:
- __HrLoadAllImportsForDll linker option
ms.openlocfilehash: b197c50d3b6b68d77dbfccda99e3c2986c515204
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98667214"
---
# <a name="load-all-imports-for-a-delay-loaded-dll"></a>Загрузка всех импортов для DLL с отложенной загрузкой

`__HrLoadAllImportsForDll`Функция, определенная в *`delayhlp.cpp`* , указывает компоновщику загрузить все импорты из библиотеки DLL, указанной с помощью [`/delayload`](delayload-delay-load-import.md) параметра компоновщика.

Загрузка всех импортов позволяет размещать обработку ошибок в одном месте в коде и не должна использовать обработку исключений вокруг фактических вызовов операций импорта. Это также позволяет избежать ситуации, когда приложение завершается неудачно с помощью процесса в результате того, что вспомогательный код не сможет загрузить импорт.

Вызов `__HrLoadAllImportsForDll` не изменяет поведение обработчиков и обработки ошибок. Дополнительные сведения см. в разделе [Обработка ошибок и уведомление](error-handling-and-notification.md).

Имя DLL, передаваемое в, `__HrLoadAllImportsForDll` сравнивается с именем, хранящимся в самой библиотеке DLL, и учитывает регистр.

В следующем примере показано, как вызвать `__HrLoadAllImportsForDll` :

```C
if (FAILED(__HrLoadAllImportsForDll("delay1.dll"))) {
   printf ( "failed on snap load, exiting\n" );
   exit(2);
}
```

## <a name="see-also"></a>См. также раздел

[Поддержка компоновщика для библиотек DLL с отложенной загрузкой](linker-support-for-delay-loaded-dlls.md)
