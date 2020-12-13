---
description: 'Дополнительные сведения о: Чандле Class'
title: Класс Чандле
ms.date: 07/09/2019
f1_keywords:
- CHandle
- ATLBASE/ATL::CHandle
- ATLBASE/ATL::CHandle::CHandle
- ATLBASE/ATL::CHandle::Attach
- ATLBASE/ATL::CHandle::Close
- ATLBASE/ATL::CHandle::Detach
- ATLBASE/ATL::CHandle::m_h
helpviewer_keywords:
- CHandle class
ms.assetid: 883e9db5-40ec-4e29-9c74-4dd2ddd2e35d
ms.openlocfilehash: 01c3b281daf829bc6488df35114c6cb853640ed1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141678"
---
# <a name="chandle-class"></a>Класс Чандле

Этот класс предоставляет методы для создания и использования объекта Handle.

## <a name="syntax"></a>Синтаксис

```
class CHandle
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Чандле:: Чандле](#chandle)|Конструктор.|
|[Чандле:: ~ Чандле](#dtor)|Деструктор|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Чандле:: Attach](#attach)|Вызовите этот метод, чтобы присоединить `CHandle` объект к существующему обработчику.|
|[Чандле:: Close](#close)|Вызовите этот метод, чтобы закрыть `CHandle` объект.|
|[Чандле::D етач](#detach)|Вызовите этот метод, чтобы отсоединить маркер от `CHandle` объекта.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[ОБРАБОТЧИК Чандле:: operator](#operator_handle)|Возвращает значение хранимого маркера.|
|[Чандле:: operator =](#operator_eq)|Оператор присвоения.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Чандле:: m_h](#m_h)|Переменная члена, в которой хранится маркер.|

## <a name="remarks"></a>Комментарии

`CHandle`Объект может использоваться всякий раз, когда требуется обработчик: основное различие заключается в том, что `CHandle` объект будет автоматически удален.

> [!NOTE]
> Некоторые функции API будут использовать значение NULL в качестве пустого или недопустимого маркера, тогда как другие используют INVALID_HANDLE_VALUE. `CHandle` использует только значение NULL и будет рассматривать INVALID_HANDLE_VALUE как реальный обработчик. При вызове API, который может возвращать INVALID_HANDLE_VALUE, следует проверить это значение перед вызовом [чандле:: Attach](#attach) или передать его в `CHandle` конструктор, а вместо этого передать NULL.

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="chandleattach"></a><a name="attach"></a> Чандле:: Attach

Вызовите этот метод, чтобы присоединить `CHandle` объект к существующему обработчику.

```cpp
void Attach(HANDLE h) throw();
```

### <a name="parameters"></a>Параметры

*h*<br/>
`CHandle` принимает владение маркером *h*.

### <a name="remarks"></a>Комментарии

Присваивает `CHandle` объект обработчику *h* , а затем вызывает метод **h. Detach ()**. При возникновении ошибок в сборках происходит исключение АТЛАССЕРТ, если *h* имеет значение null. Никакие другие проверки на допустимость этого маркера не выполняются.

## <a name="chandlechandle"></a><a name="chandle"></a> Чандле:: Чандле

Конструктор.

```
CHandle() throw();
CHandle(CHandle& h) throw();
explicit CHandle(HANDLE h) throw();
```

### <a name="parameters"></a>Параметры

*h*<br/>
Существующий Handle или `CHandle` .

### <a name="remarks"></a>Комментарии

Создает новый `CHandle` объект, при необходимости используя существующий обработчик или `CHandle` объект.

## <a name="chandlechandle"></a><a name="dtor"></a> Чандле:: ~ Чандле

Деструктор

```
~CHandle() throw();
```

### <a name="remarks"></a>Комментарии

Освобождает `CHandle` объект путем вызова [чандле:: Close](#close).

## <a name="chandleclose"></a><a name="close"></a> Чандле:: Close

Вызовите этот метод, чтобы закрыть `CHandle` объект.

```cpp
void Close() throw();
```

### <a name="remarks"></a>Комментарии

Закрывает открытый обработчик объекта. Если Handle имеет значение NULL, то в случае, если `Close` уже был вызван метод, в отладочных сборках будет создано исключение атлассерт.

## <a name="chandledetach"></a><a name="detach"></a> Чандле::D етач

Вызовите этот метод, чтобы отсоединить маркер от `CHandle` объекта.

```
HANDLE Detach() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает Отсоединяемый маркер.

### <a name="remarks"></a>Комментарии

Освобождает владение дескриптором.

## <a name="chandlem_h"></a><a name="m_h"></a> Чандле:: m_h

Переменная члена, в которой хранится маркер.

```
HANDLE m_h;
```

## <a name="chandleoperator-"></a><a name="operator_eq"></a> Чандле:: operator =

Оператор присваивания.

```
CHandle& operator=(CHandle& h) throw();
```

### <a name="parameters"></a>Параметры

*h*<br/>
`CHandle` принимает владение маркером *h*.

### <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку на новый `CHandle` объект.

### <a name="remarks"></a>Комментарии

Если `CHandle` объект в данный момент содержит маркер, он будет закрыт. `CHandle`Передаваемый объекту ссылка на Handle будет иметь значение null. Это гарантирует, что два `CHandle` объекта никогда не будут содержать один и тот же активный обработчик.

## <a name="chandleoperator-handle"></a><a name="operator_handle"></a> ОБРАБОТЧИК Чандле:: operator

Возвращает значение хранимого маркера.

```
operator HANDLE() const throw();
```

### <a name="remarks"></a>Комментарии

Возвращает значение, хранящееся в [чандле:: m_h](#m_h).

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
