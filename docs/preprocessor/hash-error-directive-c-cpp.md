---
description: 'Дополнительные сведения о директиве: #error (C/C++)'
title: '#Директива error (C/C++)'
ms.date: 08/29/2019
f1_keywords:
- '#error'
helpviewer_keywords:
- '#error directive'
- preprocessor, directives
- error directive (#error directive)
ms.assetid: d550a802-ff19-4347-9597-688935d23b2b
ms.openlocfilehash: fd6503de9590893ee0ec53cbbfa59429a0cfdcfe
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97261155"
---
# <a name="error-directive-cc"></a>Директива #error (C/C++)

Директива **#error** выдает указанное пользователем сообщение об ошибке во время компиляции, а затем завершает компиляцию.

## <a name="syntax"></a>Синтаксис

>  *строка токена* #error

## <a name="remarks"></a>Комментарии

Сообщение об ошибке, которое выдается этой директивой, включает параметр *строки токена* . Параметр *строки токена* не подлежит раскрытию макросов. Эта директива наиболее полезна во время предварительной обработки, чтобы уведомить разработчика о несогласованности программы или нарушение ограничения. В следующем примере демонстрируется обработка ошибки во время предварительной обработки.

```cpp
#if !defined(__cplusplus)
#error C++ compiler required.
#endif
```

## <a name="see-also"></a>См. также раздел

[Директивы препроцессора](../preprocessor/preprocessor-directives.md)
