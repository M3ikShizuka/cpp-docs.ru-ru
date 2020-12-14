---
description: 'Дополнительные сведения см. в статье Управление памятью: изменяемые блоки памяти'
title: Управление памятью. Изменяемые блоки памяти
ms.date: 11/04/2016
helpviewer_keywords:
- memory blocks [MFC], resizable
- memory [MFC], corruption
- memory allocation [MFC], memory block size
- memory blocks [MFC], allocating
- blocks [MFC], memory allocation
- resizable memory blocks [MFC]
ms.assetid: f0efe6f4-a3ed-4541-9195-51ec1291967a
ms.openlocfilehash: bcca5617a0d59a7dd5c6a1f9c9f82cb5876f1ef5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97248883"
---
# <a name="memory-management-resizable-memory-blocks"></a>Управление памятью. Изменяемые блоки памяти

**`new`** Операторы и **`delete`** , описанные в статье [Управление памятью: примеры](memory-management-examples.md), хорошо подходят для выделения и освобождения блоков памяти и объектов фиксированного размера. Иногда приложению может потребоваться изменение размеров блоков памяти. Для управления блоками памяти с изменяемыми размерами в куче необходимо использовать стандартные функции библиотеки времени выполнения C: [malloc](../c-runtime-library/reference/malloc.md), [realloc](../c-runtime-library/reference/realloc.md)и [Free](../c-runtime-library/reference/free.md) .

> [!IMPORTANT]
> Смешивание **`new`** операторов и **`delete`** с изменяемыми функциями выделения памяти в одном блоке памяти приведет к повреждению памяти в отладочной версии MFC. Не следует использовать перераспределение для блока памяти, выделенного **с помощью** **`new`** . Аналогично, не следует выделять блок памяти **`new`** оператором и удалять его с помощью **Free** или использовать **`delete`** оператор для блока памяти, выделенного с помощью функции **malloc**.

## <a name="see-also"></a>См. также раздел

[Управление памятью: выделение кучи](memory-management-heap-allocation.md)
