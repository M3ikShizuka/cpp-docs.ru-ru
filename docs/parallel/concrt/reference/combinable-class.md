---
description: 'Дополнительные сведения: класс combinable'
title: Класс combinable
ms.date: 11/04/2016
f1_keywords:
- combinable
- PPL/concurrency::combinable
- PPL/concurrency::combinable::combinable
- PPL/concurrency::combinable::clear
- PPL/concurrency::combinable::combine
- PPL/concurrency::combinable::combine_each
- PPL/concurrency::combinable::local
helpviewer_keywords:
- combinable class
ms.assetid: fe0bfbf6-6250-47da-b8d0-f75369f0b5be
ms.openlocfilehash: 117441be8ff7a54543adb419a1cb908d2eb9bec7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331320"
---
# <a name="combinable-class"></a>Класс combinable

Объект `combinable<T>` предназначен для предоставления частной для потока копии данных для выполнения локальных для потока вложенных вычислений без блокировки потока в параллельных алгоритмах. В конце выполнения параллельной операции частные для потока вложенные вычисления можно объединить для получения общего результата. Этот класс можно использовать вместо общей переменной, что может позволить улучшить производительность в случае возникновения большого числа конфликтов доступа к этой общей переменной.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename T>
class combinable;
```

### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных итогового Объединенного результата. Тип должен иметь конструктор копии и конструктор по умолчанию.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[combinable](#ctor)|Перегружен. Создает новый объект `combinable`.|
|[некомбинированный деструктор](#dtor)|Уничтожает объект `combinable` .|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[пусто](#clear)|Удаляет все промежуточные вычислительные результаты из предыдущего использования.|
|[состоят](#combine)|Вычисляет конечное значение из набора локальных подвычислений потока, вызывая предоставленное сочетание функтор.|
|[combine_each](#combine_each)|Вычисляет конечное значение из набора локальных подвычислений потока, вызывая предоставленное сочетание функтор один раз для локального подвычисления потока. Окончательный результат накапливается по объекту функции.|
|[Языковые](#local)|Перегружен. Возвращает ссылку на частное вычисление потока.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Оператор =](#operator_eq)|Присваивает `combinable` объекту объект из другого `combinable` объекта.|

## <a name="remarks"></a>Комментарии

Дополнительные сведения см. в разделе [Parallel Containers and Objects](../../../parallel/concrt/parallel-containers-and-objects.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`combinable`

## <a name="requirements"></a>Требования

**Заголовок:** PPL. h

**Пространство имен:** параллелизм

## <a name="clear"></a><a name="clear"></a> открытым

Удаляет все промежуточные вычислительные результаты из предыдущего использования.

```cpp
void clear();
```

## <a name="combinable"></a><a name="ctor"></a> combinable

Создает новый объект `combinable`.

```cpp
combinable();

template <typename _Function>
explicit combinable(_Function _FnInitialize);

combinable(const combinable& _Copy);
```

### <a name="parameters"></a>Параметры

*_Function*<br/>
Тип объекта функтор инициализации.

*_FnInitialize*<br/>
Функция, которая будет вызываться для инициализации каждого нового закрытого значения потока типа `T` . Он должен поддерживать оператор вызова функции с сигнатурой `T ()` .

*_Copy*<br/>
Существующий `combinable` объект, который будет скопирован в этот экземпляр.

### <a name="remarks"></a>Комментарии

Первый конструктор инициализирует новые элементы с помощью конструктора по умолчанию для типа `T` .

Второй конструктор инициализирует новые элементы с помощью функтор инициализации, переданного в качестве `_FnInitialize` параметра.

Третий конструктор является конструктором копий.

## <a name="combinable"></a><a name="dtor"></a> ~ combinable

Уничтожает объект `combinable` .

```cpp
~combinable();
```

## <a name="combine"></a><a name="combine"></a> состоят

Вычисляет конечное значение из набора локальных подвычислений потока, вызывая предоставленное сочетание функтор.

```cpp
template<typename _Function>
T combine(_Function _FnCombine) const;
```

### <a name="parameters"></a>Параметры

*_Function*<br/>
Тип объекта функции, который будет вызываться для объединения двух локальных подвычислений потока.

*_FnCombine*<br/>
Функтор, используемый для объединения подвычислений. Его сигнатура — `T (T, T)` или `T (const T&, const T&)` , и она должна быть ассоциативной и коммутативной.

### <a name="return-value"></a>Возвращаемое значение

Окончательный результат объединения всех закрытых промежуточных вычислений потока.

## <a name="combine_each"></a><a name="combine_each"></a> combine_each

Вычисляет конечное значение из набора локальных подвычислений потока, вызывая предоставленное сочетание функтор один раз для локального подвычисления потока. Окончательный результат накапливается по объекту функции.

```cpp
template<typename _Function>
void combine_each(_Function _FnCombine) const;
```

### <a name="parameters"></a>Параметры

*_Function*<br/>
Тип объекта функции, который будет вызываться для объединения одного локального подвычисления потока.

*_FnCombine*<br/>
Функтор, используемый для объединения одного подвычисления. Его сигнатура — `void (T)` или `void (const T&)` , и должны быть ассоциативными и коммутативной.

## <a name="local"></a><a name="local"></a> Языковые

Возвращает ссылку на частное вычисление потока.

```cpp
T& local();

T& local(bool& _Exists);
```

### <a name="parameters"></a>Параметры

*_Exists*<br/>
Ссылка на логическое значение. Логическое значение, на которое ссылается этот аргумент, будет иметь значение, **`true`** если подвычисление уже существовало в этом потоке, и значение, **`false`** если это был первый подрасчет в этом потоке.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на частное вычисление закрытого потока.

## <a name="operator"></a><a name="operator_eq"></a> Оператор =

Присваивает `combinable` объекту объект из другого `combinable` объекта.

```cpp
combinable& operator= (const combinable& _Copy);
```

### <a name="parameters"></a>Параметры

*_Copy*<br/>
Существующий `combinable` объект, который будет скопирован в этот экземпляр.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на этот `combinable` объект.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
