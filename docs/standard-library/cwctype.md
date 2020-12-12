---
description: 'Дополнительные сведения о: &lt; cwctype&gt;'
title: '&lt;cwctype&gt;'
ms.date: 11/04/2016
f1_keywords:
- <cwctype>
helpviewer_keywords:
- cwctype header
ms.assetid: 46476f95-b8c3-4ab2-a172-9a1be91124b7
ms.openlocfilehash: 604cffe5acb61a90fc36e7733db01f2f92aa6155
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324618"
---
# <a name="ltcwctypegt"></a>&lt;cwctype&gt;

Включает заголовок стандартной библиотеки C \<wctype.h> и добавляет связанные имена в `std` пространство имен.

## <a name="syntax"></a>Синтаксис

```cpp
#include <cwctype>
```

## <a name="remarks"></a>Remarks

Включение этого заголовка гарантирует, что имена, объявленные с помощью внешней компоновки в заголовке стандартной библиотеки C, объявляются в пространстве имен `std`.

## <a name="constants"></a>Константы

```cpp
namespace std {
    using wint_t = see below ;
    using wctrans_t = see below ;
    using wctype_t = see below ;
}

#define WEOF see below
```

## <a name="functions"></a>Функции

```cpp
int iswalnum(wint_t wc);
int iswalpha(wint_t wc);
int iswblank(wint_t wc);
int iswcntrl(wint_t wc);
int iswdigit(wint_t wc);
int iswgraph(wint_t wc);
int iswlower(wint_t wc);
int iswprint(wint_t wc);
int iswpunct(wint_t wc);
int iswspace(wint_t wc);
int iswupper(wint_t wc);
int iswxdigit(wint_t wc);
int iswctype(wint_t wc, wctype_t desc);
wctype_t wctype(const char* property);
wint_t towlower(wint_t wc);
wint_t towupper(wint_t wc);
wint_t towctrans(wint_t wc, wctrans_t desc);
wctrans_t wctrans(const char* property);
```

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](../standard-library/cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
