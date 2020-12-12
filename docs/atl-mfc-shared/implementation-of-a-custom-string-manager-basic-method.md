---
description: 'Дополнительные сведения: реализация пользовательского диспетчера строк (базовый метод)'
title: Реализация пользовательского диспетчера строк (базовый метод)
ms.date: 11/04/2016
helpviewer_keywords:
- IAtlStringMgr class, using
ms.assetid: eac5d13e-cbb4-4e82-b01e-f5f2dbcb962a
ms.openlocfilehash: e532312edff16229b6b91eef1d95ae764b70eb5e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97166958"
---
# <a name="implementation-of-a-custom-string-manager-basic-method"></a>Реализация пользовательского диспетчера строк (базовый метод)

Самый простой способ настроить схему выделения памяти для строковых данных — использовать предоставленный ATL `CAtlStringMgr` класс, но предоставить собственные подпрограммы выделения памяти. Конструктор для `CAtlStringMgr` принимает один параметр: указатель на `IAtlMemMgr` объект. `IAtlMemMgr` является абстрактным базовым классом, предоставляющим универсальный интерфейс для кучи. Используя `IAtlMemMgr` интерфейс, `CAtlStringMgr` выделяет, перераспределяет и освобождает память, используемую для хранения строковых данных. Можно либо реализовать `IAtlMemMgr` интерфейс самостоятельно, либо использовать один из пяти классов диспетчера памяти, предоставленных библиотекой ATL. Диспетчеры памяти, предоставляемые библиотекой ATL, просто заключают существующие средства выделения памяти:

- [Ккрсеап](../atl/reference/ccrtheap-class.md) Заключает в оболочку стандартные функции кучи CRT ([malloc](../c-runtime-library/reference/malloc.md), [Free](../c-runtime-library/reference/free.md)и [realloc](../c-runtime-library/reference/realloc.md))

- [CWin32Heap](../atl/reference/cwin32heap-class.md) Создает оболочку для маркера кучи Win32 с помощью [хеапаллок](/windows/win32/api/heapapi/nf-heapapi-heapalloc), [хеапфри](/windows/win32/api/heapapi/nf-heapapi-heapfree)и [хеапреаллок](/windows/win32/api/heapapi/nf-heapapi-heaprealloc)

- [CLocalHeap](../atl/reference/clocalheap-class.md) Создает оболочку для API-интерфейсов Win32: [локалаллок](/windows/win32/api/winbase/nf-winbase-localalloc), [функции LocalFree](/windows/win32/api/winbase/nf-winbase-localfree)и [локалреаллок](/windows/win32/api/winbase/nf-winbase-localrealloc)

- [CCRTHeap](../atl/reference/cglobalheap-class.md) Создает оболочку для API-интерфейсов Win32: [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc), [GlobalFree](/windows/win32/api/winbase/nf-winbase-globalfree)и [LocalLock](/windows/win32/api/winbase/nf-winbase-globalrealloc).

- [Ккомхеап](../atl/reference/ccomheap-class.md) Создает оболочку для API-интерфейсов распределителя задач COM: [CoTaskMemAlloc](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc), [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)и [котаскмемреаллок](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemrealloc)

В целях управления памятью строк наиболее полезным классом является то, `CWin32Heap` что он позволяет создавать несколько независимых куч. Например, если вы хотите использовать отдельную кучу только для строк, можно сделать следующее:

[!code-cpp[NVC_ATLMFC_Utilities#180](../atl-mfc-shared/codesnippet/cpp/implementation-of-a-custom-string-manager-basic-method_1.cpp)]

Чтобы использовать этот диспетчер закрытых строк для управления памятью для `CString` переменной, передайте указатель на диспетчер в качестве параметра в `CString` конструктор переменной:

[!code-cpp[NVC_ATLMFC_Utilities#181](../atl-mfc-shared/codesnippet/cpp/implementation-of-a-custom-string-manager-basic-method_2.cpp)]

## <a name="see-also"></a>См. также раздел

[Управление памятью с помощью CStringT](../atl-mfc-shared/memory-management-with-cstringt.md)
