---
description: 'Дополнительные сведения: Неустранимая ошибка машинного обучения A1007'
title: Неустранимая ошибка ML A1007
ms.date: 12/17/2019
ms.custom: error-reference
f1_keywords:
- A1007
helpviewer_keywords:
- A1007
ms.assetid: bcf9c826-beb3-4e93-91fe-1ffd34995fbf
ms.openlocfilehash: c26d5de1c1b44fb37d4a95f51b2cb9480d2ba664
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97129549"
---
# <a name="ml-fatal-error-a1007"></a>Неустранимая ошибка ML A1007

**уровень вложенности слишком глубокий**

Для ассемблера достигнуто ограничение вложенности. Ограничение составляет 20 уровней, за исключением случаев, где указано иное.

Один из следующих элементов был вложен слишком глубоким:

- Общая директива, например [. Если](dot-if.md), [. Повторите](dot-repeat.md)или [. WHILE](dot-while.md).

- Определение структуры.

- Директива условной сборки.

- Определение процедуры.

- Директива [пушконтекст](pushcontext.md) (ограничение — 10).

- Определение сегмента.

- Включаемый файл.

- Макрос.

## <a name="see-also"></a>См. также раздел

[Сообщения об ошибках ML](ml-error-messages.md)
