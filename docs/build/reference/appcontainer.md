---
description: Дополнительные сведения о:/APPCONTAINER
title: /APPCONTAINER
ms.date: 11/04/2016
f1_keywords:
- /APPCONTAINER
helpviewer_keywords:
- APPCONTAINER editbin option
- -APPCONTAINER editbin option
- /APPCONTAINER editbin option
ms.assetid: 0ca4f1ec-c8de-4a37-b3e2-deda7af0bb88
ms.openlocfilehash: f9ea7ff8cac45e45626f15745f77d2230afc1d4b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97187173"
---
# <a name="appcontainer"></a>/APPCONTAINER

Помечает исполняемый файл, который должен выполняться в контейнере приложения, например Microsoft Store или универсальное приложение Windows.

```

/APPCONTAINER[:NO]
```

## <a name="remarks"></a>Комментарии

Исполняемый файл, для которого задан параметр **/APPCONTAINER** , может выполняться только в контейнере приложения, то есть в среде изоляции процессов, которая была введена в Windows 8. Для Microsoft Store и универсальных приложений Windows этот параметр должен быть установлен.

## <a name="see-also"></a>См. также раздел

[Параметры EDITBIN](editbin-options.md)<br/>
[Что такое универсальное приложение Windows?](/windows/uwp/get-started/universal-application-platform-guide)
