---
description: 'Дополнительные сведения об исключениях: исключениях в конструкторах'
title: Исключения. Исключения в конструкторах
ms.date: 11/04/2016
helpviewer_keywords:
- constructors [MFC], exceptions
- throwing exceptions [MFC], in constructors
- exceptions [MFC], in constructors
ms.assetid: a78eae5a-5821-4b27-9478-1436320ed1e1
ms.openlocfilehash: 69393cc6a5cf709d359ccbdb572406e91c6788ec
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97290600"
---
# <a name="exceptions-exceptions-in-constructors"></a>Исключения. Исключения в конструкторах

При возникновении исключения в конструкторе очистите все объекты и выделения памяти, сделанные до создания исключения, как описано в [исключениях: создание исключений из собственных функций](exceptions-throwing-exceptions-from-your-own-functions.md).

При возникновении исключения в конструкторе память для самого объекта уже была выделена на момент вызова конструктора. Таким образом, компилятор автоматически освобождает память, занятую объектом, после возникновения исключения.

Дополнительные сведения см. [в разделе исключения: освобождение объектов в исключениях](exceptions-freeing-objects-in-exceptions.md).

## <a name="see-also"></a>См. также раздел

[Обработка исключений](exception-handling-in-mfc.md)
