---
description: 'Дополнительные сведения о: task_continuation_context классе'
title: Класс task_continuation_context
ms.date: 11/04/2016
f1_keywords:
- task_continuation_context
- PPLTASKS/concurrency::task_continuation_context
- PPLTASKS/concurrency::task_continuation_context::get_current_winrt_context
- PPLTASKS/concurrency::task_continuation_context::use_arbitrary
- PPLTASKS/concurrency::task_continuation_context::use_current
- PPLTASKS/concurrency::task_continuation_context::use_default
- PPLTASKS/concurrency::task_continuation_context::use_synchronous_execution
helpviewer_keywords:
- task_continuation_context class
ms.assetid: 1fb5a76a-3682-45c2-a615-8b6b527741f0
ms.openlocfilehash: ff843a84dd3e0bdaeee9df99e91b1708116191d3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188304"
---
# <a name="task_continuation_context-class"></a>Класс task_continuation_context

Класс `task_continuation_context` позволяет указать место продолжения выполнения задачи. Этот класс рекомендуется использовать только из приложения среда выполнения Windows. Для приложений, не относящихся к среда выполнения Windows, контекст выполнения продолжения задачи определяется средой выполнения и не настраивается.

## <a name="syntax"></a>Синтаксис

```cpp
class task_continuation_context : public details::_ContextCallback;
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[get_current_winrt_context](#get_current_winrt_context)|Возвращает объект контекста продолжения задачи, представляющий текущий контекст потока WinRT.|
|[use_arbitrary](#use_arbitrary)|Создает контекст продолжения выполнения задачи, который позволяет среде выполнения возможность выбора контекста для продолжения.|
|[use_current](#use_current)|Возвращает объект контекста продолжения задачи, представляющий контекст текущего выполнения.|
|[use_default](#use_default)|Создает контекст продолжения задачи по умолчанию.|
|[use_synchronous_execution](#use_synchronous_execution)|Возвращает объект контекста продолжения задачи, представляющий контекст синхронного выполнения.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`_ContextCallback`

`task_continuation_context`

## <a name="requirements"></a>Требования

**Заголовок:** из ppltasks. h

**Пространство имен:** параллелизм

## <a name="get_current_winrt_context"></a><a name="get_current_winrt_context"></a> get_current_winrt_context

Возвращает объект контекста продолжения задачи, представляющий текущий контекст потока WinRT.

### <a name="syntax"></a>Синтаксис

```cpp
static task_continuation_context get_current_winrt_context();
```

### <a name="return-value"></a>Возвращаемое значение

Текущий контекст потока среда выполнения Windows. Возвращает пустой task_continuation_context, если вызывается из контекста, не являющегося среда выполнения Windows.

### <a name="remarks"></a>Комментарии

`get_current_winrt_context`Метод захватывает контекст потока среда выполнения Windows вызывающего объекта. Он возвращает пустой контекст для вызывающих объектов, не являющихся среда выполнения Windows.

Значение, возвращаемое, `get_current_winrt_context` можно использовать, чтобы указать среде выполнения, что продолжение должно выполняться в модели подразделений перехваченного контекста (STA VS MTA), независимо от того, учитывается ли предшествующая задача подразделением. Задача, учитывающая подразделение, — это задача, которая распаковывает `IAsyncInfo` интерфейс Среда выполнения Windows или задачу, которая в то же самое относится к этой задаче.

Этот метод аналогичен  `use_current` методу, но он также доступен для машинного кода c++ без поддержки расширения C++/CX. Он предназначен для использования опытными пользователями, пишущими код библиотеки C++/ККС-агностик для машинных и среда выполнения Windowsных вызовов. Если эта функция не нужна, рекомендуется использовать `use_current` метод, который доступен только для клиентов C++/CX.

## <a name="use_arbitrary"></a><a name="use_arbitrary"></a> use_arbitrary

Создает контекст продолжения выполнения задачи, который позволяет среде выполнения возможность выбора контекста для продолжения.

### <a name="syntax"></a>Синтаксис

```cpp
static task_continuation_context use_arbitrary();
```

### <a name="return-value"></a>Возвращаемое значение

Контекст продолжения задачи, представляющий произвольное расположение.

### <a name="remarks"></a>Комментарии

При использовании этого контекста продолжения продолжение будет выполняться в контексте, который выбирается средой выполнения, даже если задача предшествующей задачи является подразделением.

`use_arbitrary` можно использовать для отключения поведения по умолчанию для продолжения в задаче, учитывающей подразделение, созданной в STA.

Этот метод доступен только для среда выполнения Windows приложений.

## <a name="use_current"></a><a name="use_current"></a> use_current

Возвращает объект контекста продолжения задачи, представляющий контекст текущего выполнения.

```cpp
static task_continuation_context use_current();
```

### <a name="return-value"></a>Возвращаемое значение

Указывает текущий контекст выполнения.

### <a name="remarks"></a>Комментарии

Этот метод захватывает контекст среда выполнения Windows вызывающего объекта, чтобы продолжения могли выполняться в правильном апартаменте.

Значение, возвращаемое, `use_current` можно использовать, чтобы указать среде выполнения, что продолжение должно выполняться в перехваченном контексте (STA VS MTA) независимо от того, учитывается ли предшествующая задача подразделением. Задача, учитывающая подразделение, — это задача, которая распаковывает `IAsyncInfo` интерфейс Среда выполнения Windows или задачу, которая в то же самое относится к этой задаче.

Этот метод доступен только для среда выполнения Windows приложений.

## <a name="use_default"></a><a name="use_default"></a> use_default

Создает контекст продолжения задачи по умолчанию.

```cpp
static task_continuation_context use_default();
```

### <a name="return-value"></a>Возвращаемое значение

Контекст продолжения по умолчанию.

### <a name="remarks"></a>Комментарии

Контекст по умолчанию используется, если не задан контекст продолжения при вызове `then` метода. В приложениях Windows для Windows 7 и ниже, а также настольных приложениях в Windows 8 и более поздних версиях среда выполнения определяет, где будут выполняться продолжения задачи. Однако в среда выполнения Windowsном приложении контекст продолжения по умолчанию для продолжения в задаче с подразделением подразделений — это апартамент, в котором `then` вызывается.

Задача, учитывающая подразделение, — это задача, которая распаковывает `IAsyncInfo` интерфейс Среда выполнения Windows или задачу, которая в то же самое относится к этой задаче. Таким образом, если вы запланируете продолжение задачи с подразделением апартамента в среда выполнения Windows STA, продолжение будет выполняться в этом STA.

Продолжение в задаче, не учитывающем апартамент, будет выполняться в контексте, который выбирает среда выполнения.

## <a name="task_continuation_contextuse_synchronous_execution"></a><a name="use_synchronous_execution"></a> task_continuation_context:: use_synchronous_execution

Возвращает объект контекста продолжения задачи, представляющий контекст синхронного выполнения.

### <a name="syntax"></a>Синтаксис

```cpp
static task_continuation_context use_synchronous_execution();
```

### <a name="return-value"></a>Возвращаемое значение

Синхронный контекст выполнения.

### <a name="remarks"></a>Комментарии

`use_synchronous_execution`Метод заставляет задачу продолжения выполняться синхронно в контексте, что приводит к завершению предшествующей задачи.

Если предшествующая задача уже выполнена при присоединении продолжения, продолжение выполняется синхронно в контексте, который прикрепляет продолжение.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
