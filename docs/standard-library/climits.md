---
description: 'Дополнительные сведения о: &lt; климитс&gt;'
title: '&lt;climits&gt;'
ms.date: 11/04/2016
f1_keywords:
- <climits>
helpviewer_keywords:
- climits header
ms.assetid: 7ca8a539-aa45-4ac3-86e8-74513be3f07e
ms.openlocfilehash: 97c5f6f9822656c2b25b85dab6fb668a8a8eebbf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97234089"
---
# <a name="ltclimitsgt"></a>&lt;climits&gt;

Включает заголовок стандартной библиотеки C \<limits.h> и добавляет связанные имена в `std` пространство имен. Включение этого заголовка гарантирует, что имена, объявленные с помощью внешней компоновки в заголовке стандартной библиотеки C, объявляются в `std` пространстве имен.

## <a name="syntax"></a>Синтаксис

```cpp
#include <climits>
```

## <a name="macros"></a>Макросы

```cpp
#define CHAR_BIT
#define SCHAR_MIN
#define SCHAR_MAX
#define UCHAR_MAX
#define CHAR_MIN
#define CHAR_MAX
#define MB_LEN_MAX
#define SHRT_MIN
#define SHRT_MAX
#define USHRT_MAX
#define INT_MIN
#define INT_MAX
#define UINT_MAX
#define LONG_MIN
#define LONG_MAX
#define ULONG_MAX
#define LLONG_MIN
#define LLONG_MAX
#define ULLONG_MAX
```

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](../standard-library/cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
