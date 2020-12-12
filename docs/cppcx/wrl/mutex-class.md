---
description: Дополнительные сведения о классе семафора
title: Класс Mutex
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::Mutex
- corewrappers/Microsoft::WRL::Wrappers::Mutex::Lock
- corewrappers/Microsoft::WRL::Wrappers::Mutex::Mutex
- corewrappers/Microsoft::WRL::Wrappers::Mutex::operator=
helpviewer_keywords:
- Microsoft::WRL::Wrappers::Mutex class
- Microsoft::WRL::Wrappers::Mutex::Lock method
- Microsoft::WRL::Wrappers::Mutex::Mutex, constructor
- Microsoft::WRL::Wrappers::Mutex::operator= operator
ms.assetid: 682a0963-721c-46a2-8871-000e9997505b
ms.openlocfilehash: f69c14014a2283fe56ef8e7f705bebe5a5f6dc9d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330841"
---
# <a name="mutex-class"></a>Класс Mutex

Представляет объект синхронизации, который исключительно управляет общим ресурсом.

## <a name="syntax"></a>Синтаксис

```cpp
class Mutex : public HandleT<HandleTraits::MutexTraits>;
```

## <a name="members"></a>Члены

### <a name="public-typedefs"></a>Общедоступные определения типов

Имя       | Описание
---------- | ------------------------------------------------------
`SyncLock` | Синоним для класса, поддерживающего синхронные блокировки.

### <a name="public-constructor"></a>Открытый конструктор

Имя                   | Описание
---------------------- | ------------------------------------------------
[Мьютекс:: Mutex](#mutex) | Инициализирует новый экземпляр класса `Mutex`.

### <a name="public-members"></a>Открытые члены

Имя                 | Описание
-------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------
[Мьютекс:: Lock](#lock) | Ожидает, пока текущий объект или `Mutex` объект, связанный с указанным дескриптором, не истечет из-за истечения мьютекса или указанного интервала времени ожидания.

### <a name="public-operator"></a>Public, оператор

Имя                                 | Описание
------------------------------------ | ---------------------------------------------------------------------------
[Мьютекс:: operator =](#operator-assign) | Присваивает указанный `Mutex` объект текущему объекту (перемещает) `Mutex` .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`Mutex`

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Программы Microsoft:: WRL:: оболочки

## <a name="mutexlock"></a><a name="lock"></a> Мьютекс:: Lock

Ожидает, пока текущий объект или `Mutex` объект, связанный с указанным дескриптором, не истечет из-за истечения мьютекса или указанного интервала времени ожидания.

```cpp
SyncLock Lock(
   DWORD milliseconds = INFINITE
);

static SyncLock Lock(
   HANDLE h,
   DWORD milliseconds = INFINITE
);
```

### <a name="parameters"></a>Параметры

*milliseconds*<br/>
Интервал времени ожидания в миллисекундах. Значение по умолчанию равно INFINITE, что означает неограниченное время ожидания.

*h*<br/>
Маркер `Mutex` объекта.

### <a name="return-value"></a>Возвращаемое значение

## <a name="mutexmutex"></a><a name="mutex"></a> Мьютекс:: Mutex

Инициализирует новый экземпляр класса `Mutex`.

```cpp
explicit Mutex(
   HANDLE h
);

Mutex(
   _Inout_ Mutex&& h
);
```

### <a name="parameters"></a>Параметры

*h*<br/>
Маркер или ссылка rvalue на указатель на `Mutex` объект.

### <a name="remarks"></a>Комментарии

Первый конструктор инициализирует `Mutex` объект из указанного маркера. Второй конструктор инициализирует `Mutex` объект из указанного маркера, а затем перемещает владение мьютексом на текущий `Mutex` объект.

## <a name="mutexoperator"></a><a name="operator-assign"></a> Мьютекс:: operator =

Присваивает указанный `Mutex` объект текущему объекту (перемещает) `Mutex` .

```cpp
Mutex& operator=(
   _Inout_ Mutex&& h
);
```

### <a name="parameters"></a>Параметры

*h*<br/>
Ссылка rvalue на `Mutex` объект.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на текущий `Mutex` объект.

### <a name="remarks"></a>Комментарии

Дополнительные сведения см. в разделе **семантика перемещения** в [деклараторе ссылки rvalue:  &&](../../cpp/rvalue-reference-declarator-amp-amp.md).
