---
description: 'Дополнительные сведения о: NAME (C/C++)'
title: NAME (C/C++)
ms.date: 11/04/2016
f1_keywords:
- name
helpviewer_keywords:
- NAME .def file statement
ms.assetid: 5c9b6bd8-9275-46a5-afba-f17a5936dc26
ms.openlocfilehash: 7444aa20539b47b1f04d17a266a0b65a552af3f3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97137778"
---
# <a name="name-cc"></a>NAME (C/C++)

Задает имя основного выходного файла.

```
NAME [application][BASE=address]
```

## <a name="remarks"></a>Комментарии

Аналогичный способ указания имени выходного файла — с помощью параметра компоновщика [/out](out-output-file-name.md) , а аналогичный способ задания базового адреса — с помощью параметра компоновщика [/base](base-base-address.md) . Если указаны оба значения, то параметр/OUT переопределяет **имя**.

При построении библиотеки DLL имя будет влиять только на имя библиотеки DLL.

## <a name="see-also"></a>См. также раздел

[Правила для Module-Definitionных инструкций](rules-for-module-definition-statements.md)
