---
description: 'Дополнительные сведения: структура space_info'
title: Структура space_info
ms.date: 09/10/2018
f1_keywords:
- filesystem/std::tr2::sys::space_info
ms.assetid: f2b35b42-06ff-45bd-8617-39a0f5358a54
ms.openlocfilehash: 254866a0eb225b4ed7bcfe4e06a734c5c9d0e3ee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97153880"
---
# <a name="space_info-structure"></a>Структура space_info

Содержит сведения о томе.

## <a name="syntax"></a>Синтаксис

```cpp
struct space_info
{
    uintmax_t capacity;
    uintmax_t free;
    uintmax_t available;
};
```

## <a name="members"></a>Члены

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|`unsigned long long capacity`|Представляет общее число байтов, которое может представлять том.|
|`unsigned long long free`|Представляет число байтов, не используемых для представления данных в томе.|
|`unsigned long long available`|Представляет число байтов, доступных для представления данных в томе.|

## <a name="requirements"></a>Требования

**Заголовок:**\<filesystem>

**Пространство имен:** std::experimental::filesystem

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[\<filesystem>](../standard-library/filesystem.md)\
[Навигация по файловой системе (C++)](../standard-library/file-system-navigation.md)
