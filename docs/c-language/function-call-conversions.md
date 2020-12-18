---
description: 'Подробнее о следующем: Преобразования вызова функции'
title: Преобразования вызова функции
ms.date: 11/04/2016
helpviewer_keywords:
- function calls, converting
- function calls, argument type conversions
- functions [C], argument conversions
ms.assetid: 04ea0f81-509a-4913-8b12-0937a81babcf
ms.openlocfilehash: f37cf2ef6c35cb8e7c856e1ab722a1efda2da61d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97195961"
---
# <a name="function-call-conversions"></a>Преобразования вызова функции

Тип преобразования, выполняемого над аргументами в вызове функции, зависит от того, имеется ли для вызываемой функции прототип функции (предварительное объявление) с объявленными типами аргументов.

Если существует прототип функции и в нем объявлены типы аргументов, то компилятор выполняет проверку типа (см. статью [Функции](../c-language/functions-c.md)).

Если прототипа нет, то над аргументами в вызове функции выполняются только обычные арифметические преобразования. Для каждого аргумента в вызове они выполняются отдельно. Иными словами, значение типа **`float`** преобразуется в **`double`** ; значение типа **`char`** или **`short`**  — в **`int`** ; а **`unsigned char`** или **`unsigned short`**  — в **`unsigned int`** .

## <a name="see-also"></a>См. также

[Преобразования типов](../c-language/type-conversions-c.md)
