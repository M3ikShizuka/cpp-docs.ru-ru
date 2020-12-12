---
description: Дополнительные сведения о:/IMPORTS (DUMPBIN)
title: /IMPORTS (DUMPBIN)
ms.date: 11/04/2016
f1_keywords:
- /imports
helpviewer_keywords:
- IMPORTS dumpbin option
- /IMPORTS dumpbin option
- -IMPORTS dumpbin option
ms.assetid: 6a296216-2b1b-40f8-8736-cd4553a22456
ms.openlocfilehash: 86c428280bbca3a4957f7d7a0a640482607547de
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199796"
---
# <a name="imports-dumpbin"></a>/IMPORTS (DUMPBIN)

```
/IMPORTS[:file]
```

Этот параметр отображает список библиотек DLL (как статические, так и с [загрузкой](linker-support-for-delay-loaded-dlls.md)), которые импортируются в исполняемый файл или библиотеку DLL, и все индивидуальные операции импорта из каждой из этих библиотек DLL.

Необязательная `file` Спецификация позволяет указать, что будут отображаться только операции импорта для этой библиотеки DLL. Пример:

```
dumpbin /IMPORTS:msvcrt.dll
```

## <a name="remarks"></a>Remarks

Выходные данные, отображаемые этим параметром, похожи на выходные данные [/EXPORTS](dash-exports.md) .

С файлами, созданными с использованием параметра компилятора [/GL](gl-whole-program-optimization.md), можно использовать только параметр DUMPBIN [/HEADERS](headers.md).

## <a name="see-also"></a>См. также раздел

[Параметры DUMPBIN](dumpbin-options.md)
