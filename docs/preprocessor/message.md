---
description: Дополнительные сведения об pragma директиве Message в Microsoft C/C++
title: Сообщение pragma
ms.date: 01/22/2021
f1_keywords:
- message_CPP
- vc-pragma.message
helpviewer_keywords:
- message pragma
- pragma, message
no-loc:
- pragma
ms.openlocfilehash: 6f5e39896e0ba644f9d40665e80cbf7de9026223
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713497"
---
# <a name="message-no-locpragma"></a>`message` pragma

Отправляет строковый литерал в стандартный вывод, не завершая компиляцию.

## <a name="syntax"></a>Синтаксис

> **`#pragma message(`***Строка сообщения***`)`**

## <a name="remarks"></a>Примечания

Обычно используется **`message`** pragma для вывода информационных сообщений во время компиляции.

Параметр *строки сообщения* может быть макросом, который расширяется до строкового литерала, и можно объединить такие макросы с строковыми литералами в любом сочетании.

При использовании предопределенного макроса в **`message`** pragma макрос должен возвращать строку. В противном случае необходимо преобразовать выходные данные макроса в строку.

В следующем фрагменте кода используется **`message`** pragma для вывода сообщений во время компиляции:

```cpp
// pragma_directives_message1.cpp
// compile with: /LD
#if _M_IX86 >= 500
#pragma message("_M_IX86 >= 500")
#endif

#pragma message("")

#pragma message( "Compiling " __FILE__ )
#pragma message( "Last modified on " __TIMESTAMP__ )

#pragma message("")

// with line number
#define STRING2(x) #x
#define STRING(x) STRING2(x)

#pragma message (__FILE__ "[" STRING(__LINE__) "]: test")

#pragma message("")
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
