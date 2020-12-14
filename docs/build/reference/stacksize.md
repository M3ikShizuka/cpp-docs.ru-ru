---
description: 'Дополнительные сведения о: STACKSIZE'
title: STACKSIZE
ms.date: 11/04/2016
f1_keywords:
- STACKSIZE
helpviewer_keywords:
- STACKSIZE .def file statement
ms.assetid: 4d8c79bd-1cb4-4e4d-90f2-b5a7a4d20e7a
ms.openlocfilehash: b5d52bccc09979084b9023d380e86fe90e4def32
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230345"
---
# <a name="stacksize"></a>STACKSIZE

Задает размер стека (в байтах).

```
STACKSIZE reserve[,commit]
```

## <a name="remarks"></a>Комментарии

Аналогичный способ установки стека — с помощью параметра [распределения стека](stack-stack-allocations.md) (/stack). Дополнительные сведения о *резервировании* и аргументах см. в документации по этому параметру `commit` .

Этот параметр не влияет на библиотеки DLL.

## <a name="see-also"></a>См. также раздел

[Правила для Module-Definitionных инструкций](rules-for-module-definition-statements.md)
