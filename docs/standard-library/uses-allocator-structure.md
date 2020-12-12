---
description: 'Дополнительные сведения: структура uses_allocator'
title: Структура uses_allocator
ms.date: 11/04/2016
f1_keywords:
- future/std::uses_allocator
ms.assetid: c418f002-62e9-4806-b70c-41c663cae583
ms.openlocfilehash: 3ece99d12443af2ec28b52e2a0dae72d8af4cc91
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97153620"
---
# <a name="uses_allocator-structure"></a>Структура uses_allocator

Специализации, которые всегда содержат значение true.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty, class Alloc>
struct uses_allocator<promise<Ty>, Alloc> : true_type;
template <class Ty, class Alloc>
struct uses_allocator<packaged_task<Ty>, Alloc> : true_type;
```

## <a name="requirements"></a>Требования

**Заголовок:**\<future>

**Пространство имен:** std

## <a name="specializations"></a>Специализации

### <a name="tuple"></a><a name="tuple"></a> \<tuple>

```cpp
template <class... Types, class Alloc>
struct uses_allocator<tuple<Types...>, Alloc>;
```

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[\<future>](../standard-library/future.md)
