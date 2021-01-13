---
description: 'Дополнительные сведения о: &lt; CTime&gt;'
title: '&lt;ctime&gt;'
ms.date: 11/04/2016
f1_keywords:
- <ctime>
helpviewer_keywords:
- ctime header
ms.assetid: c1f7d4a4-4bfe-4e35-92cb-f63dbd3c39a8
ms.openlocfilehash: 3ebf4849f990f7e0ae835fca88a6b38a8ca1838d
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126706"
---
# <a name="ltctimegt"></a>&lt;ctime&gt;

Включает заголовок стандартной библиотеки C \<time.h> и добавляет связанные имена в `std` пространство имен.

## <a name="syntax"></a>Синтаксис

```cpp
#include <ctime>
```

## <a name="remarks"></a>Remarks

Включение этого заголовка гарантирует, что имена, объявленные с помощью внешней компоновки в заголовке стандартной библиотеки C, объявляются в пространстве имен `std`.

## <a name="constants"></a>Константы

```cpp
#define NULL
#define CLOCKS_PER_SEC
#define TIME_UTC

namespace std {
    using size_t = see below;
    using clock_t = see below ;
    using time_t = see below ;
}
```

## <a name="structures"></a>Структуры

```cpp
struct timespec;
struct tm;
```

## <a name="functions"></a>Функции

```cpp
clock_t clock();
double difftime(time_t time1, time_t time0);
time_t mktime(struct tm* timeptr);
time_t time(time_t* timer);
int timespec_get(timespec* ts, int base);
char* asctime(const struct tm* timeptr);
char* ctime(const time_t* timer);
struct tm* gmtime(const time_t* timer);
struct tm* localtime(const time_t* timer);
size_t strftime(char* s, size_t maxsize, const char* format, const struct tm* timeptr);
```

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](../standard-library/cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
