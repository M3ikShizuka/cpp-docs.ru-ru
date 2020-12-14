---
description: Дополнительные сведения о:/ЛИНКЕРМЕМБЕР
title: /LINKERMEMBER
ms.date: 11/04/2016
f1_keywords:
- /linkermember
helpviewer_keywords:
- /LINKERMEMBER dumpbin option
- LINKERMEMBER dumpbin option
- -LINKERMEMBER dumpbin option
ms.assetid: c96868c1-d70e-4651-ae36-c55b58b16406
ms.openlocfilehash: 76c842bcc2299b4245847e7d4e9a64656e88d2d9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199393"
---
# <a name="linkermember"></a>/LINKERMEMBER

```
/LINKERMEMBER[:{1|2}]
```

## <a name="remarks"></a>Комментарии

Этот параметр отображает открытые символы, определенные в библиотеке. Укажите аргумент 1, чтобы отображать символы в порядке объектов, а также их смещения. Укажите аргумент 2, чтобы отображать смещения и номера индексов объектов, а затем перечислите символы в алфавитном порядке вместе с индексом объекта для каждого из них. Чтобы получить оба выхода, укажите/ЛИНКЕРМЕМБЕР без аргумента number.

С файлами, созданными с использованием параметра компилятора [/GL](gl-whole-program-optimization.md), можно использовать только параметр DUMPBIN [/HEADERS](headers.md).

## <a name="see-also"></a>См. также раздел

[Параметры DUMPBIN](dumpbin-options.md)
