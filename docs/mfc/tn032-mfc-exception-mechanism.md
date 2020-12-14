---
description: 'Дополнительные сведения о: TN032: механизм исключения MFC'
title: TN032. Механизм исключений MFC
ms.date: 11/04/2016
helpviewer_keywords:
- TN032
- MFC, exceptions
- CException class [MFC], using
ms.assetid: 0271f0aa-82cb-47a2-b7ea-e88126fc7e43
ms.openlocfilehash: 847d78762aaf5e04c8a0c1eb2170e951d0b867bc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97215538"
---
# <a name="tn032-mfc-exception-mechanism"></a>TN032. Механизм исключений MFC

Предыдущие версии Visual C++ не поддерживали стандартный механизм исключений C++ и предоставляли **макросы, которые** использовались вместо них. Эта версия Visual C++ полностью поддерживает исключения C++. В этом заметке рассматриваются некоторые дополнительные сведения о реализации предыдущих макросов, включая автоматическое удаление объектов на основе стека. Поскольку исключения C++ поддерживают очистку стека по умолчанию, это техническое примечание больше не требуется.

Дополнительные сведения о различиях между макросами MFC и новыми ключевыми словами C++ см. в разделе [исключения. Использование макросов MFC и исключений c++](../mfc/exceptions-using-mfc-macros-and-cpp-exceptions.md) .

## <a name="see-also"></a>См. также раздел

[Технические примечания по номеру](../mfc/technical-notes-by-number.md)<br/>
[Технические примечания по категориям](../mfc/technical-notes-by-category.md)
