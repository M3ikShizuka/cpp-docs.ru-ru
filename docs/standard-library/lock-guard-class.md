---
description: 'Дополнительные сведения о: lock_guard классе'
title: Класс lock_guard
ms.date: 11/04/2016
f1_keywords:
- mutex/std::lock_guard
- mutex/std::lock_guard::lock_guard
ms.assetid: 57121f0d-9c50-481c-b971-54e64df864e0
ms.openlocfilehash: d8965f1e781d99f0b84c58dcc3288a4532e4351c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97277730"
---
# <a name="lock_guard-class"></a>Класс lock_guard

Представляет шаблон, для которого можно создать экземпляры и объект, деструктор которого разблокирует `mutex`.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Mutex>
class lock_guard;
```

## <a name="remarks"></a>Remarks

В аргументе шаблона `Mutex` должно быть указано имя *типа мьютекс*.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`lock_guard::mutex_type`|Синоним для аргумента шаблона `Mutex`.|

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[lock_guard](#lock_guard)|Формирует объект `lock_guard`.|
|[Деструктор lock_guard::~lock_guard](#dtorlock_guard_destructor)|Снимает блокировку `mutex`, переданного в конструктор.|

## <a name="requirements"></a>Требования

**Заголовок:**\<mutex>

**Пространство имен:** std

## <a name="lock_guardlock_guard-constructor"></a><a name="lock_guard"></a> Конструктор lock_guard:: lock_guard

Формирует объект `lock_guard`.

```cpp
explicit lock_guard(mutex_type& Mtx);

lock_guard(mutex_type& Mtx, adopt_lock_t);
```

### <a name="parameters"></a>Параметры

*MTX*\
Объект *типа мьютекс*.

### <a name="remarks"></a>Комментарии

Первый конструктор конструирует объект типа `lock_guard` и блокирует *MTX*. Если *MTX* не является рекурсивным мьютексом, он должен быть разблокирован при вызове этого конструктора.

Второй конструктор не блокирует *MTX*. *MTX* должен быть заблокирован при вызове этого конструктора. Конструктор не выдает никаких исключений.

## <a name="lock_guardlock_guard-destructor"></a><a name="dtorlock_guard_destructor"></a> Деструктор lock_guard:: ~ lock_guard

Снимает блокировку `mutex`, переданного в конструктор.

```cpp
~lock_guard() noexcept;
```

### <a name="remarks"></a>Комментарии

Если `mutex` не существует при выполнении деструктора, поведение не определено.

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[\<mutex>](../standard-library/mutex.md)
