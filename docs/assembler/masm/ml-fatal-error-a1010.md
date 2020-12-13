---
description: 'Дополнительные сведения: Неустранимая ошибка машинного обучения A1010'
title: Неустранимая ошибка ML A1010
ms.date: 12/17/2019
ms.custom: error-reference
f1_keywords:
- A1010
helpviewer_keywords:
- A1010
ms.assetid: 9e0b5241-67f4-4740-8701-3b2d2d1ad9e4
ms.openlocfilehash: 4a00d9594c71c8a22942e869d109bf51176394c9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97129510"
---
# <a name="ml-fatal-error-a1010"></a>Неустранимая ошибка ML A1010

**непарное вложение блоков:**

Начало блока не имеет соответствующего конца, или у конца блока нет соответствующего начала. Может потребоваться одна из следующих факторов.

- Общая директива, например [. Если](dot-if.md), [. Повторите](dot-repeat.md)или [. WHILE](dot-while.md).

- Директива условной сборки, например [If](if-masm.md), [Repeat](repeat.md)или **while**.

- Определение структуры или объединения.

- Определение процедуры.

- Определение сегмента.

- Директива [попконтекст](popcontext.md) .

- Директива условной сборки, например [else](else-masm.md), [ELSEIF](elseif-masm.md)или **endif** без соответствующего [If](if-masm.md).

## <a name="see-also"></a>См. также раздел

[Сообщения об ошибках ML](ml-error-messages.md)
