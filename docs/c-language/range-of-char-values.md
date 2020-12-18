---
description: 'Подробнее о следующем: Диапазон значений типа char'
title: Диапазон значений типа char
ms.date: 11/04/2016
ms.assetid: 15ae9781-ec21-4333-bba8-6d2383bbf7f1
ms.openlocfilehash: 4897dd2b6433b148ea0c739118dea14f81f1e2bc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97309164"
---
# <a name="range-of-char-values"></a>Диапазон значений типа char

**ANSI 3.2.1.1** Имеет ли "простой" тип **`char`** тот же диапазон значений, что и **`signed char`** или **`unsigned char`**

Все знаковые значения char находятся в диапазоне от –128 до 127. Все беззнаковые значения char находятся в диапазоне от 0 до 255.

Параметр компилятора [`/J`](../build/reference/j-default-char-type-is-unsigned.md) указывает, что для **`char`** по умолчанию вместо **`signed char`** будет использоваться **`unsigned char`** .

## <a name="see-also"></a>См. также

[Символы](../c-language/characters.md)
