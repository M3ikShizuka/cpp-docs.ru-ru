---
description: 'Дополнительные сведения: управление памятью: выделение кучи'
title: Управление памятью. Выделение кучи
ms.date: 11/04/2016
helpviewer_keywords:
- memory [MFC], detecting leaks
- delete operator [MFC], using with debug MFC
- heap allocation [MFC], described
- memory allocation [MFC], heap memory
- memory leaks [MFC], detecting
- new operator [MFC], using with debug MFC
- heap allocation [MFC]
- detecting memory leaks [MFC]
ms.assetid: a5d949c6-1b79-476e-9c66-513a558203d9
ms.openlocfilehash: bb9035d1346f1d3bbff53a03da9b4cf1d946a7ba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97259660"
---
# <a name="memory-management-heap-allocation"></a>Управление памятью. Выделение кучи

Куча резервируется для потребностей в выделении памяти для программы. Это область, расположенная отдельно от программного кода и стека. Обычные программы на языке C используют функции **malloc** и Free для выделения и **освобождения** памяти кучи. Отладочная версия MFC предоставляет измененные версии встроенных операторов C++ **`new`** , а **`delete`** также выделяет и освобождает объекты в памяти кучи.

При использовании **`new`** и **`delete`** вместо **malloc** и **Free** вы можете воспользоваться усовершенствованиями отладки управления памятью библиотеки классов, которые могут быть полезны при обнаружении утечек памяти. При создании программы с использованием окончательной версии MFC стандартные версии **`new`** **`delete`** операторов и предоставляют эффективный способ выделения и освобождения памяти (окончательная версия MFC не предоставляет измененные версии этих операторов).

Обратите внимание, что общий размер объектов, выделенных в куче, ограничен только доступной виртуальной памятью вашей системы.

## <a name="see-also"></a>См. также раздел

[Управление памятью](memory-management.md)
