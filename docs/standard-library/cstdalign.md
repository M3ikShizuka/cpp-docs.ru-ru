---
description: 'Дополнительные сведения о: &lt; cstdalign&gt;'
title: '&lt;cstdalign&gt;'
ms.date: 07/11/2019
f1_keywords:
- <cstdalign>
- __alignas_is_defined
- __alignof_is_defined
helpviewer_keywords:
- cstdalign header
- __alignas_is_defined
- __alignof_is_defined
ms.assetid: 9d570924-d299-4225-9a58-8c4c820f5903
ms.openlocfilehash: 7727f75ad0627c2a22b856631a776a2ee5426271
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126615"
---
# <a name="ltcstdaligngt"></a>&lt;cstdalign&gt;

В некоторых реализациях стандартной библиотеки C++ этот заголовок включает заголовок стандартной библиотеки C \<stdalign.h> и добавляет связанные имена в `std` пространство имен. Поскольку этот заголовок не реализован в КОМПИЛЯТОРОМ MSVC, \<cstdalign> заголовок определяет макросы совместимости `__alignas_is_defined` и `__alignof_is_defined` .

> [!NOTE]
> Так как \<stdalign.h> заголовок определяет макросы, которые являются ключевыми словами в C++, в том числе он не оказывает никакого влияния. \<stdalign.h>Заголовок является устаревшим в C++. \<cstdalign>Заголовок является устаревшим в c++ 17 и удаляется в черновом стандарте c++ 20.

## <a name="requirements"></a>Требования

**Заголовок:**\<cstdalign>

**Пространство имен:** std

## <a name="macros"></a>Макросы

| Макрос | Описание |
| - | - |
| `__alignas_is_defined` | Макрос совместимости C, который разворачивается до целочисленной константы 1. |
| `__alignof_is_defined` | Макрос совместимости C, который разворачивается до целочисленной константы 1. |

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](thread-safety-in-the-cpp-standard-library.md)
