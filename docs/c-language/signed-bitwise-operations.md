---
description: 'Подробнее о следующем: Битовые операции со знаком'
title: Битовые операции со знаком
ms.date: 11/04/2016
helpviewer_keywords:
- bitwise operations
- signed bitwise operations
ms.assetid: 1e5cf65b-ee32-41a0-a5c2-82c1854091f6
ms.openlocfilehash: 98cca4d7450e0b65301ba3d2ad65f0cb3aca81ea
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97292654"
---
# <a name="signed-bitwise-operations"></a>Битовые операции со знаком

**ANSI 3.3** Результаты выполнения побитовых операций над знаковыми целочисленными значениями

Побитовые операции над знаковыми целочисленными значениями работают так же, как и над беззнаковыми. Например, значение `-16 & 99` можно представить в двоичном виде следующим образом:

```
  11111111 11110000
& 00000000 01100011
  _________________
  00000000 01100000
```

Результат выполнения побитовой операции И будет равен 96.

## <a name="see-also"></a>См. также

[Целые числа](../c-language/integers.md)
