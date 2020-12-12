---
description: 'Дополнительные сведения о: использование команды Abort'
title: Использование функции abort
ms.date: 11/04/2016
helpviewer_keywords:
- abort function
ms.assetid: 3ba39b78-ef74-4a8d-8dee-2d62442de174
ms.openlocfilehash: 16c1df7a7b3a26be444d9b17d370366b1a41ea1f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97116864"
---
# <a name="using-abort"></a>Использование функции abort

Вызов функции [Abort](../c-runtime-library/reference/abort.md) приводит к немедленному завершению работы. Выполняется обход нормального процесса удаления для инициализированных глобальных статических объектов. Также осуществляется обход всей специальной обработки, которая была задана с помощью функции `atexit`.

## <a name="see-also"></a>См. также раздел

[Дополнительные сведения о завершении](../cpp/additional-termination-considerations.md)
