---
description: Дополнительные сведения о:/ЛИНЕНУМБЕРС
title: /LINENUMBERS
ms.date: 11/04/2016
f1_keywords:
- /linenumbers
helpviewer_keywords:
- LINENUMBERS dumpbin option
- line numbers
- -LINENUMBERS dumpbin option
- /LINENUMBERS dumpbin option
ms.assetid: 1681d582-2c2f-484e-9920-109959549055
ms.openlocfilehash: 9df3d88476a82466f86ec23147c9f8f35f9b3f1d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97191021"
---
# <a name="linenumbers"></a>/LINENUMBERS

```
/LINENUMBERS
```

## <a name="remarks"></a>Комментарии

Этот параметр отображает номера строк в формате COFF. Номера строк существуют в объектном файле, если он был скомпилирован с базой данных программы (/Zi), C7 Compatible (/Z7) или только с номерами строк (/ZD). Исполняемый файл или DLL содержит номера строк COFF, если они были связаны с созданием отладочной информации (/DEBUG).

С файлами, созданными с использованием параметра компилятора [/GL](gl-whole-program-optimization.md), можно использовать только параметр DUMPBIN [/HEADERS](headers.md).

## <a name="see-also"></a>См. также раздел

[Параметры DUMPBIN](dumpbin-options.md)
