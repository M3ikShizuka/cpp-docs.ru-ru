---
description: Дополнительные сведения о классе семафора
title: Класс Semaphore
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::Semaphore
- corewrappers/Microsoft::WRL::Wrappers::Semaphore::Lock
- corewrappers/Microsoft::WRL::Wrappers::Semaphore::operator=
- corewrappers/Microsoft::WRL::Wrappers::Semaphore::Semaphore
helpviewer_keywords:
- Microsoft::WRL::Wrappers::Semaphore class
- Microsoft::WRL::Wrappers::Semaphore::Lock method
- Microsoft::WRL::Wrappers::Semaphore::operator= operator
- Microsoft::WRL::Wrappers::Semaphore::Semaphore, constructor
ms.assetid: ded53526-17b4-4381-9c60-ea5e77363db6
ms.openlocfilehash: 0cf99ff0a0e5263b3ed924ec5ac69b7edb0bd1f7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97186237"
---
# <a name="semaphore-class"></a>Класс Semaphore

Представляет объект синхронизации, который управляет общим ресурсом и поддерживает ограниченное число пользователей.

## <a name="syntax"></a>Синтаксис

```cpp
class Semaphore : public HandleT<HandleTraits::SemaphoreTraits>;
```

## <a name="members"></a>Члены

### <a name="public-typedefs"></a>Общедоступные определения типов

Имя       | Описание
---------- | ------------------------------------------------------
`SyncLock` | Синоним для класса, поддерживающего синхронные блокировки.

### <a name="public-constructors"></a>Открытые конструкторы

name                               | Описание
---------------------------------- | ----------------------------------------------------
[Семафор:: семафор](#semaphore) | Инициализирует новый экземпляр класса `Semaphore`.

### <a name="public-methods"></a>Открытые методы

name                     | Описание
------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------
[Семафор:: Lock](#lock) | Ожидает, пока текущий объект или объект, связанный с указанным дескриптором, находится в сигнальном состоянии или истечет указанный интервал времени ожидания.

### <a name="public-operators"></a>Открытые операторы

Имя                                     | Описание
---------------------------------------- | ---------------------------------------------------------------------------------------
[Семафор:: оператор =](#operator-assign) | Перемещает указанный маркер из `Semaphore` объекта в текущий `Semaphore` объект.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`Semaphore`

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Программы Microsoft:: WRL:: оболочки

## <a name="semaphorelock"></a><a name="lock"></a> Семафор:: Lock

Ожидает, пока текущий объект или `Semaphore` объект, связанный с указанным дескриптором, находится в сигнальном состоянии или истечет указанный интервал времени ожидания.

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
Маркер `Semaphore` объекта.

### <a name="return-value"></a>Возвращаемое значение

`Details::SyncLockWithStatusT<HandleTraits::SemaphoreTraits>`

## <a name="semaphoreoperator"></a><a name="operator-assign"></a> Семафор:: оператор =

Перемещает указанный маркер из `Semaphore` объекта в текущий `Semaphore` объект.

```cpp
Semaphore& operator=(
   _Inout_ Semaphore&& h
);
```

### <a name="parameters"></a>Параметры

*h*<br/>
Rvalue — ссылка на `Semaphore` объект.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на текущий `Semaphore` объект.

## <a name="semaphoresemaphore"></a><a name="semaphore"></a> Семафор:: семафор

Инициализирует новый экземпляр класса `Semaphore`.

```cpp
explicit Semaphore(
   HANDLE h
);

WRL_NOTHROW Semaphore(
   _Inout_ Semaphore&& h
);
```

### <a name="parameters"></a>Параметры

*h*<br/>
Указатель или ссылка rvalue на `Semaphore` объект.
