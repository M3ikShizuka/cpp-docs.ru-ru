---
description: 'Дополнительные сведения: выделение и освобождение памяти для BSTR'
title: Выделение и освобождение памяти для BSTR
ms.date: 11/04/2016
f1_keywords:
- bstr
helpviewer_keywords:
- BSTRs, memory allocation
- memory deallocation, string memory
- memory [C++], releasing
- memory allocation, BSTRs
- memory deallocation, BSTR memory
- strings [C++], releasing
ms.assetid: 98041e29-3442-4a02-b425-7a4a13e9cc84
ms.openlocfilehash: 2b027bdc5615578bc785075ae7e8709e2b3a7ea5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142667"
---
# <a name="allocating-and-releasing-memory-for-a-bstr"></a>Выделение и освобождение памяти для BSTR

При создании `BSTR` и передаче их между объектами COM необходимо соблюдать осторожность при обработке используемой ими памяти, чтобы избежать утечек памяти. Когда элемент `BSTR` остается в интерфейсе, необходимо освободить его память по завершении. Однако, когда `BSTR` передается из интерфейса, принимающий объект отвечает за управление памятью.

Как правило, для выделения и освобождения памяти, выделенной для `BSTR` , используются следующие правила:

- При вызове функции, которая ожидает `BSTR` аргумент, необходимо выделить память для `BSTR` перед вызовом и затем освободить его. Пример:

   [!code-cpp[NVC_ATLMFC_Utilities#192](../atl-mfc-shared/codesnippet/cpp/allocating-and-releasing-memory-for-a-bstr_1.cpp)]

   [!code-cpp[NVC_ATLMFC_Utilities#193](../atl-mfc-shared/codesnippet/cpp/allocating-and-releasing-memory-for-a-bstr_2.cpp)]

- При вызове функции, возвращающей значение `BSTR` , необходимо освобождать строку самостоятельно. Пример:

   [!code-cpp[NVC_ATLMFC_Utilities#194](../atl-mfc-shared/codesnippet/cpp/allocating-and-releasing-memory-for-a-bstr_3.cpp)]

   [!code-cpp[NVC_ATLMFC_Utilities#195](../atl-mfc-shared/codesnippet/cpp/allocating-and-releasing-memory-for-a-bstr_4.cpp)]

- При реализации функции, которая возвращает `BSTR` , выделяет строку, но не освобождает ее. При получении функции освобождается память. Пример:

   [!code-cpp[NVC_ATLMFC_Utilities#196](../atl-mfc-shared/codesnippet/cpp/allocating-and-releasing-memory-for-a-bstr_5.cpp)]

## <a name="see-also"></a>См. также раздел

[Строки (ATL и MFC)](../atl-mfc-shared/strings-atl-mfc.md)<br/>
[CStringT:: Аллоксисстринг](../atl-mfc-shared/reference/cstringt-class.md#allocsysstring)<br/>
[сисаллокстринг](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)<br/>
[сисфристринг](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
