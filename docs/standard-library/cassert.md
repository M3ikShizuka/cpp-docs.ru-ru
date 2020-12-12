---
description: 'Дополнительные сведения о: &lt; кассерт&gt;'
title: '&lt;cassert&gt;'
ms.date: 11/04/2016
f1_keywords:
- <cassert>
helpviewer_keywords:
- cassert header
ms.assetid: 6ead15a3-ac45-4075-be8e-350bca995c26
ms.openlocfilehash: e2b515fe492e6847c4d0cc5841dc43a2d879dd99
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97325360"
---
# <a name="ltcassertgt"></a>&lt;cassert&gt;

Включает заголовок стандартной библиотеки C \<assert.h> и добавляет связанные имена в `std` пространство имен. Включение этого заголовка гарантирует, что имена, объявленные с помощью внешней компоновки в заголовке стандартной библиотеки C, объявляются в `std` пространстве имен.

> [!NOTE]
> \<assert.h> не определяет **`static_assert`** макрос.

## <a name="syntax"></a>Синтаксис

```cpp
#include <cassert>
```

## <a name="macros"></a>Макросы

```cpp
#define assert(E)
```

### <a name="remarks"></a>Комментарии

`assert(E)` является константой, только если NDEBUG определен `assert` , где является последним определением или переопределением, или *E* , преобразованное в bool, вычисляется как **`true`** .

## <a name="see-also"></a>См. также раздел

[Макрос assert, _assert, _wassert](../c-runtime-library/reference/assert-macro-assert-wassert.md)\
[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](../standard-library/cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
