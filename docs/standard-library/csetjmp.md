---
description: 'Дополнительные сведения о: &lt; ксетжмп&gt;'
title: '&lt;csetjmp&gt;'
ms.date: 11/04/2016
f1_keywords:
- <csetjmp>
helpviewer_keywords:
- csetjmp header
ms.assetid: 8f21fddd-5e9b-4219-a848-581cdd3569d9
ms.openlocfilehash: ebd3acefbdf96c8dd2b0cba569e7cd2ffc128d31
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324778"
---
# <a name="ltcsetjmpgt"></a>&lt;csetjmp&gt;

Включает заголовок стандартной библиотеки C \<setjmp.h> и добавляет связанные имена в `std` пространство имен.

## <a name="syntax"></a>Синтаксис

```cpp
#include <csetjmp>

using jmp_buf = see below;
```

## <a name="functions"></a>Функции

```cpp
[[noreturn]] void longjmp(jmp_buf env, int val);
```

## <a name="macros"></a>Макросы

```cpp
#define setjmp(env)
```

## <a name="remarks"></a>Комментарии

Включение этого заголовка гарантирует, что имена, объявленные с помощью внешней компоновки в заголовке стандартной библиотеки C, объявляются в пространстве имен `std`.

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](../standard-library/cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
