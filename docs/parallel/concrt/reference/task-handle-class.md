---
description: 'Дополнительные сведения о: task_handle классе'
title: Класс task_handle
ms.date: 03/27/2019
f1_keywords:
- task_handle
- PPL/concurrency::task_handle
- PPL/concurrency::task_handle::task_handle
helpviewer_keywords:
- task_handle class
ms.assetid: 74a34b15-708b-4231-a509-947874292b13
ms.openlocfilehash: 21fa2a1782fad200061deb1e85bf052613354a34
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188226"
---
# <a name="task_handle-class"></a>Класс task_handle

Класс `task_handle` представляет отдельный параллельный рабочий элемент. Он инкапсулирует инструкции и данные, необходимые для выполнения части работы.

## <a name="syntax"></a>Синтаксис

```cpp
template<
    typename _Function
>
class task_handle : public ::Concurrency::details::_UnrealizedChore;
```

### <a name="parameters"></a>Параметры

*_Function*<br/>
Тип объекта функции, который будет вызываться для выполнения работы, представленной `task_handle` объектом.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[task_handle](#task_handle)|Создает новый объект `task_handle`. Работа задачи выполняется путем вызова функции, указанной в качестве параметра конструктора.|
|[Деструктор ~ task_handle](#dtor)|Уничтожает `task_handle` объект.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[оператор ()](#task_handle__operator_call)|Оператор вызова функции, который вызывается средой выполнения для выполнения работы обработчика задачи.|

## <a name="remarks"></a>Комментарии

`task_handle` объекты можно использовать в сочетании с `structured_task_group` или более общим `task_group` объектом для разложения работы в параллельные задачи. Дополнительные сведения см. в разделе [параллелизм задач](../../../parallel/concrt/task-parallelism-concurrency-runtime.md).

Обратите внимание, что создатель `task_handle` объекта отвечает за поддержание времени существования созданного `task_handle` объекта, пока он больше не требуется для Среда выполнения с параллелизмом. Как правило, это означает, что `task_handle` объект не должен уничтожения до тех пор, пока не будет `wait` `run_and_wait` вызван метод или, `task_group` `structured_task_group` в котором он находится в очереди.

`task_handle` объекты обычно используются в сочетании с лямбда-выражениями C++. Так как неизвестный тип лямбда-выражения незнаком, функция [make_task](concurrency-namespace-functions.md#make_task) обычно используется для создания `task_handle` объекта.

Среда выполнения создает копию рабочей функции, передаваемая в `task_handle` объект. Таким образом, любые изменения состояния, происходящие в объекте функции, который передается в `task_handle` объект, не будут отображаться в копии этого объекта функции.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`task_handle`

## <a name="requirements"></a>Требования

**Заголовок:** PPL. h

**Пространство имен:** параллелизм

## <a name="operator"></a><a name="task_handle__operator_call"></a> оператор ()

Оператор вызова функции, который вызывается средой выполнения для выполнения работы обработчика задачи.

```cpp
void operator()() const;
```

## <a name="task_handle"></a><a name="task_handle"></a> task_handle

Создает новый объект `task_handle`. Работа задачи выполняется путем вызова функции, указанной в качестве параметра конструктора.

```cpp
task_handle(const _Function& _Func);
```

### <a name="parameters"></a>Параметры

*_Func*<br/>
Функция, которая будет вызываться для выполнения работы, представленной `task_handle` объектом. Это может быть лямбда-функтор, указатель на функцию или любой объект, который поддерживает версию оператора вызова функции с сигнатурой `void operator()()` .

### <a name="remarks"></a>Комментарии

Среда выполнения создает копию рабочей функции, которая передается в конструктор. Таким образом, любые изменения состояния, происходящие в объекте функции, который передается в `task_handle` объект, не будут отображаться в копии этого объекта функции.

## <a name="task_handle"></a><a name="dtor"></a> ~ task_handle

Уничтожает `task_handle` объект.

```cpp
~task_handle();
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс task_group](task-group-class.md)<br/>
[Класс structured_task_group](structured-task-group-class.md)
