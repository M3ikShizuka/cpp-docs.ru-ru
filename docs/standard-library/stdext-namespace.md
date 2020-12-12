---
description: 'Дополнительные сведения о: stdext Namespace'
title: Пространство имен stdext
ms.date: 09/06/2017
f1_keywords:
- stdext
helpviewer_keywords:
- _DEFINE_DEPRECATED_HASH_CLASSES symbol
- stdext namespace
ms.assetid: 3e94fc89-0584-424f-bc09-081b73379545
ms.openlocfilehash: bb81dde22014ec91f7212ce4313c21a8410f30a9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97153789"
---
# <a name="stdext-namespace"></a>Пространство имен stdext

Элементы [\<hash_map>](../standard-library/hash-map.md) [\<hash_set>](../standard-library/hash-set.md) файлов заголовков и в настоящее время не являются частью стандарта ISO C++. Поэтому эти типы и члены были перемещены из пространства имен `std` в пространство имен `stdext`в целях поддержания соответствия стандарту C++.

При компиляции с параметром [/Ze](../build/reference/za-ze-disable-language-extensions.md), который является значением по умолчанию, компилятор предупреждает об использовании `std` для членов \<hash_map> \<hash_set> файлов заголовков и. Для отключения этого предупреждения используется директива pragma [warning](../preprocessor/warning.md) .

Чтобы компилятор создавал ошибку для `std` членов \<hash_map> \<hash_set> файлов заголовков и с параметром **/Ze**, добавьте следующую директиву перед `#include` всеми файлами заголовков стандартной библиотеки C++.

```cpp
#define _DEFINE_DEPRECATED_HASH_CLASSES 0
```

При компиляции с параметром **/Za** компилятор создает ошибку.

## <a name="see-also"></a>См. также раздел

[Общие сведения о стандартной библиотеке C++](../standard-library/cpp-standard-library-overview.md)
