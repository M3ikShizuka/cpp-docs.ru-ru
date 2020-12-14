---
description: 'Дополнительные сведения: Загрузка всех импортов для Delay-Loaded DLL'
title: Загрузка всех импортов для библиотеки DLL с отложенной загрузкой
ms.date: 11/04/2016
helpviewer_keywords:
- __HrLoadAllImportsForDll linker option
ms.assetid: 975fcd97-1a56-4a16-9698-e1a249d2d592
ms.openlocfilehash: 0f1334f30568e4722bd97579145ddcae9851b901
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190929"
---
# <a name="loading-all-imports-for-a-delay-loaded-dll"></a>Загрузка всех импортов для библиотеки DLL с отложенной загрузкой

Функция **__HrLoadAllImportsForDll** , которая определена в делайхлп. cpp, указывает компоновщику загрузить все импорты из библиотеки DLL, указанной в параметре компоновщика [параметр/DELAYLOAD](delayload-delay-load-import.md) .

Загрузка всех импортов позволяет размещать обработку ошибок в одном месте в коде и не должна использовать обработку исключений вокруг фактических вызовов операций импорта. Это также позволяет избежать ситуации, когда приложение завершается с ошибкой частично через процесс в результате того, что вспомогательный код не сможет загрузить импорт.

Вызов **__HrLoadAllImportsForDll** не изменяет поведение обработчиков и обработки ошибок. Дополнительные сведения см. в разделе [обработка и уведомление об ошибках](error-handling-and-notification.md) .

Имя DLL, передаваемое в **__HrLoadAllImportsForDll** , сравнивается с именем, хранящимся в самой библиотеке DLL и с учетом регистра.

В следующем примере показано, как вызвать **__HrLoadAllImportsForDll**:

```
if (FAILED(__HrLoadAllImportsForDll("delay1.dll"))) {
   printf ( "failed on snap load, exiting\n" );
   exit(2);
}
```

## <a name="see-also"></a>См. также раздел

[Поддержка компоновщика для Delay-Loadedных библиотек DLL](linker-support-for-delay-loaded-dlls.md)
