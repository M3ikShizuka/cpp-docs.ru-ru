---
description: 'Дополнительные сведения о: EventTargetArray Class'
title: Класс EventTargetArray
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::Details::EventTargetArray
- event/Microsoft::WRL::Details::EventTargetArray::AddTail
- event/Microsoft::WRL::Details::EventTargetArray::Begin
- event/Microsoft::WRL::Details::EventTargetArray::End
- event/Microsoft::WRL::Details::EventTargetArray::EventTargetArray
- event/Microsoft::WRL::Details::EventTargetArray::Length
- event/Microsoft::WRL::Details::EventTargetArray::~EventTargetArray
helpviewer_keywords:
- Microsoft::WRL::Details::EventTargetArray class
- Microsoft::WRL::Details::EventTargetArray::AddTail method
- Microsoft::WRL::Details::EventTargetArray::Begin method
- Microsoft::WRL::Details::EventTargetArray::End method
- Microsoft::WRL::Details::EventTargetArray::EventTargetArray, constructor
- Microsoft::WRL::Details::EventTargetArray::Length method
- Microsoft::WRL::Details::EventTargetArray::~EventTargetArray, destructor
ms.assetid: e3cadb7c-2160-4cbb-a2f8-c28733d1e96d
ms.openlocfilehash: ac3199d2374a47e94705f8f51672bfedd0b7bf20
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97198587"
---
# <a name="eventtargetarray-class"></a>Класс EventTargetArray

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
class EventTargetArray :
    public Microsoft::WRL::RuntimeClass<
        Microsoft::WRL::RuntimeClassFlags<ClassicCom>,
        IUnknown
    >;
```

## <a name="remarks"></a>Remarks

Представляет массив обработчиков событий.

Обработчики событий, связанные с объектом [EventSource](eventsource-class.md) , хранятся в защищенном `EventTargetArray` члене данных.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

name                                                           | Описание
-------------------------------------------------------------- | -----------------------------------------------------------
[EventTargetArray:: EventTargetArray](#eventtargetarray)        | Инициализирует новый экземпляр класса `EventTargetArray`.
[EventTargetArray:: ~ EventTargetArray](#tilde-eventtargetarray) | Выполняет деинициализацию текущего `EventTargetArray` класса.

### <a name="public-methods"></a>Открытые методы

name                                  | Описание
------------------------------------- | ---------------------------------------------------------------------------------------
[EventTargetArray:: AddTail](#addtail) | Добавляет указанный обработчик событий в конец внутреннего массива обработчиков событий.
[EventTargetArray:: Begin](#begin)     | Возвращает адрес первого элемента во внутреннем массиве обработчиков событий.
[EventTargetArray:: end](#end)         | Возвращает адрес последнего элемента во внутреннем массиве обработчиков событий.
[EventTargetArray:: Length](#length)   | Возвращает текущее количество элементов во внутреннем массиве обработчиков событий.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`EventTargetArray`

## <a name="requirements"></a>Требования

**Заголовок:** Event. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="eventtargetarrayeventtargetarray"></a><a name="tilde-eventtargetarray"></a> EventTargetArray:: ~ EventTargetArray

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
~EventTargetArray();
```

### <a name="remarks"></a>Комментарии

Выполняет деинициализацию текущего `EventTargetArray` класса.

## <a name="eventtargetarrayaddtail"></a><a name="addtail"></a> EventTargetArray:: AddTail

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
void AddTail(
   _In_ IUnknown* element
);
```

### <a name="parameters"></a>Параметры

*дерев*<br/>
Указатель на обработчик событий для добавления.

### <a name="remarks"></a>Комментарии

Добавляет указанный обработчик событий в конец внутреннего массива обработчиков событий.

`AddTail()` предназначен для внутреннего использования только `EventSource` классом.

## <a name="eventtargetarraybegin"></a><a name="begin"></a> EventTargetArray:: Begin

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
ComPtr<IUnknown>* Begin();
```

### <a name="return-value"></a>Возвращаемое значение

Адрес первого элемента во внутреннем массиве обработчиков событий.

### <a name="remarks"></a>Комментарии

Возвращает адрес первого элемента во внутреннем массиве обработчиков событий.

## <a name="eventtargetarrayend"></a><a name="end"></a> EventTargetArray:: end

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
ComPtr<IUnknown>* End();
```

### <a name="return-value"></a>Возвращаемое значение

Адрес последнего элемента во внутреннем массиве обработчиков событий.

### <a name="remarks"></a>Комментарии

Возвращает адрес последнего элемента во внутреннем массиве обработчиков событий.

## <a name="eventtargetarrayeventtargetarray"></a><a name="eventtargetarray"></a> EventTargetArray:: EventTargetArray

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
EventTargetArray(
   _Out_ HRESULT* hr,
   size_t items
);
```

### <a name="parameters"></a>Параметры

*ч*<br/>
После выполнения этой операции конструктора параметр *HR* указывает, успешно ли выполнено выделение массива. В следующем списке приведены возможные значения для *HR*.

- S_OK<br/>
  Операция успешно выполнена.

- E_OUTOFMEMORY<br/>
  Не удалось выделить память для массива.

- S_FALSE<br/>
  *Элементы* параметров меньше или равны нулю.

*items*<br/>
Число выделяемых элементов массива.

### <a name="remarks"></a>Комментарии

Инициализирует новый экземпляр класса `EventTargetArray`.

`EventTargetArray` используется для сохранения массива обработчиков событий в `EventSource` объекте.

## <a name="eventtargetarraylength"></a><a name="length"></a> EventTargetArray:: Length

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
size_t Length();
```

### <a name="return-value"></a>Возвращаемое значение

Текущее число элементов во внутреннем массиве обработчиков событий.

### <a name="remarks"></a>Комментарии

Возвращает текущее количество элементов во внутреннем массиве обработчиков событий.
