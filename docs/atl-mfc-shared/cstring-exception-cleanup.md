---
description: 'Дополнительные сведения о: Очистка исключений CString'
title: Очистка исключений CString
ms.date: 11/04/2016
helpviewer_keywords:
- CString objects, exceptions
- exception handling, cleanup code
ms.assetid: 28b9ce70-be63-4a0d-92a8-44bbfbc95e83
ms.openlocfilehash: 9c77c9bf5d3f123315c126ce2361be63230c173b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167153"
---
# <a name="cstring-exception-cleanup"></a>Очистка исключений CString

В предыдущих версиях MFC было важно очищать объекты [CString](../atl-mfc-shared/reference/cstringt-class.md) после использования. В MFC версии 3,0 и более поздней явная очистка больше не требуется.

В механизме обработки исключений C++, который теперь используется библиотекой MFC, не нужно беспокоиться об очистке после возникновения исключения. Сведения о том, как перехватывается стек, порожденный с помощью C++ "Unwind" после исключения, см. [в инструкциях try, catch и Throw](../cpp/try-throw-and-catch-statements-cpp.md). Даже если вы используете макрос **try** / **catch** вместо ключевых слов C++ **`try`** и **`catch`** , MFC использует механизм исключений c++ под, поэтому вам по-прежнему не нужно явно очищать.

## <a name="see-also"></a>См. также раздел

[Строки (ATL и MFC)](../atl-mfc-shared/strings-atl-mfc.md)<br/>
[Обработка исключений](../mfc/exception-handling-in-mfc.md)
