---
description: 'Дополнительные сведения: управление памятью'
title: Управление памятью
ms.date: 11/04/2016
helpviewer_keywords:
- memory [MFC]
- MFC, memory management
- memory allocation [MFC]
- memory [MFC], managing
- memory allocation [MFC], MFC
ms.assetid: 934ac81b-d630-4232-88e5-ea74f7187987
ms.openlocfilehash: 4e274820ce82cf8b338c6a62349440e944f21f7a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97253381"
---
# <a name="memory-management"></a>Управление памятью

В этой группе статей описывается, как использовать преимущества служб общего назначения библиотека Microsoft Foundation Class (MFC), связанных с управлением памятью. Выделение памяти можно разделить на две основные категории: выделение кадров и выделение памяти в куче.

Одно основное различие между двумя методами выделения заключается в том, что при распределении кадров обычно используется собственно блок памяти, а при выделении кучи всегда указывается указатель на блок памяти. Еще одно важное различие между двумя схемами состоит в том, что объекты фрейма автоматически удаляются, а объекты кучи должны быть явно удалены программистом.

Сведения об управлении памятью в программах для Windows в не MFC см. в разделе [Управление памятью](/windows/win32/memory/memory-management) в Windows SDK.

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Выделение кадров](memory-management-frame-allocation.md)

- [Выделение кучи](memory-management-heap-allocation.md)

- [Выделение памяти для массива](memory-management-examples.md)

- [Отмена выделения памяти для массива из кучи](memory-management-examples.md)

- [Выделение памяти для структуры данных](memory-management-examples.md)

- [Выделение памяти для объекта](memory-management-examples.md)

- [Изменяемые блоки памяти](memory-management-resizable-memory-blocks.md)

## <a name="see-also"></a>См. также раздел

[Основные понятия](mfc-concepts.md)<br/>
[Общие разделы по MFC](general-mfc-topics.md)
