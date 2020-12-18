---
description: 'Подробнее о следующем: Преобразования присваиваний'
title: Преобразования присваиваний
ms.date: 11/04/2016
helpviewer_keywords:
- conversions, assignment
- assignment conversions
ms.assetid: 4ee01013-de32-4aae-b12e-0051d0cde927
ms.openlocfilehash: b9889214f160c981c57fc3174b542396d71458bd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97279966"
---
# <a name="assignment-conversions"></a>Преобразования присваиваний

В операциях присваивания тип присваиваемого значения преобразуется в тип переменной, которой присваивается значение. C позволяет при присваивании выполнять преобразования между целочисленными типами и типами с плавающей запятой даже в случае потери данных при преобразовании. Используемый метод преобразования зависит от того, какие типы участвуют в операции присваивания, как описано в статье [Обычные арифметические преобразования](../c-language/usual-arithmetic-conversions.md) и в следующих статьях.

- [Преобразования из целочисленных типов со знаком](../c-language/conversions-from-signed-integral-types.md)

- [Преобразования из целочисленных типов без знака](../c-language/conversions-from-unsigned-integral-types.md)

- [Преобразования типов с плавающей запятой](../c-language/conversions-from-floating-point-types.md)

- [Преобразования в типы указателей и из типов указателей](../c-language/conversions-to-and-from-pointer-types.md)

- [Преобразования из других типов](../c-language/conversions-from-other-types.md)

Квалификаторы типа не влияют на допустимость преобразования, но в левой части операции присваивания нельзя использовать l-значение **`const`** .

## <a name="see-also"></a>См. также

[Преобразования типов](../c-language/type-conversions-c.md)
