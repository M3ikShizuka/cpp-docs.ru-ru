---
description: 'Дополнительные сведения о: &lt; кстдарг&gt;'
title: '&lt;cstdarg&gt;'
ms.date: 11/04/2016
f1_keywords:
- <cstdarg>
helpviewer_keywords:
- cstdarg header
ms.assetid: 639b4ef7-8408-4640-9343-41631f0ab663
ms.openlocfilehash: 4f009535cdcfec5d9e461aad4857335ddb86e1ba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97233257"
---
# <a name="ltcstdarggt"></a>&lt;cstdarg&gt;

Включает заголовок стандартной библиотеки C \<stdarg.h> и добавляет связанные имена в `std` пространство имен. Включение этого заголовка гарантирует, что имена, объявленные с помощью внешней компоновки в заголовке стандартной библиотеки C, объявляются в `std` пространстве имен.

## <a name="syntax"></a>Синтаксис

```cpp
#include <cstdarg>
```

## <a name="namespace-and-macros"></a>Пространство имен и макросы

```cpp
namespace std {
    using va_list = see below;
}

#define va_arg(V, P)
#define va_copy(VDST, VSRC)
#define va_end(V)
#define va_start(V, P)
```

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](../standard-library/cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
