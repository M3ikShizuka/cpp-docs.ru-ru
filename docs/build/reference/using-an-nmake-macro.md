---
description: 'Дополнительные сведения о: использование макроса NMAKE'
title: Использование макроса NMAKE
ms.date: 11/04/2016
helpviewer_keywords:
- macros, NMAKE
- NMAKE macros, using
ms.assetid: 95c87fbc-76e6-48c0-8536-9bfe179f328e
ms.openlocfilehash: 14a1856b411bf7608b94caacb1b0b078dd1f5577
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97247011"
---
# <a name="using-an-nmake-macro"></a>Использование макроса NMAKE

Чтобы использовать макрос, заключите его имя в круглые скобки, перед которыми следует знак доллара ($), как показано ниже.

## <a name="syntax"></a>Синтаксис

```
$(macroname)
```

## <a name="remarks"></a>Remarks

Пробелы не допускаются. Круглые скобки необязательны, если *имяМакроса* — одиночный символ. Строка определения заменяет $ (*имяМакроса*); неопределенный макрос заменяется пустой строкой.

## <a name="what-do-you-want-to-know-more-about"></a>Дополнительные сведения

[Макроподстановка](macro-substitution.md)

## <a name="see-also"></a>См. также раздел

[Макросы и программа NMAKE](macros-and-nmake.md)
