---
description: 'Дополнительные сведения о: sync_per_container классе'
title: Класс sync_per_container
ms.date: 11/04/2016
f1_keywords:
- allocators/stdext::sync_per_container
- allocators/stdext::sync_per_container::equals
helpviewer_keywords:
- sync_per_container class
ms.assetid: 0b4b2904-b668-4d94-a422-d4f919cbffab
ms.openlocfilehash: 83dc2f3d874fdc1910a3da4fdc34fb18c432cc25
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97183316"
---
# <a name="sync_per_container-class"></a>Класс sync_per_container

Описывает [фильтр синхронизации](../standard-library/allocators-header.md) , который предоставляет отдельный объект кэша для каждого объекта распределителя.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Cache>
class sync_per_container
    : public Cache
```

### <a name="parameters"></a>Параметры

*Мбайта*\
Тип кэша, связанный с фильтром синхронизации. Это может быть [`cache_chunklist`](../standard-library/cache-chunklist-class.md) , [`cache_freelist`](../standard-library/cache-freelist-class.md) или [`cache_suballoc`](../standard-library/cache-suballoc-class.md) .

### <a name="member-functions"></a>Функции элементов

|Функция-член|Описание|
|-|-|
|[equals](#equals)|Сравнивает два кэша на равенство.|

## <a name="requirements"></a>Требования

**Заголовок:**\<allocators>

**Пространство имен:** stdext

## <a name="sync_per_containerequals"></a><a name="equals"></a> sync_per_container:: Equals

Сравнивает два кэша на равенство.

```cpp
bool equals(const sync_per_container<Cache>& Other) const;
```

### <a name="parameters"></a>Параметры

*Мбайта*\
Объект кэша фильтра синхронизации.

*Иной*\
Объект кэша для сравнения на равенство.

### <a name="return-value"></a>Возвращаемое значение

Функция – член всегда возвращает значение **`false`** .

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[\<allocators>](../standard-library/allocators-header.md)
