---
description: 'Дополнительные сведения о: метод deferrableeventargs Class'
title: Класс DeferrableEventArgs
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::DeferrableEventArgs
- event/Microsoft::WRL::DeferrableEventArgs::GetDeferral
- event/Microsoft::WRL::DeferrableEventArgs::InvokeAllFinished
helpviewer_keywords:
- Microsoft::WRL::DeferrableEventArgs class
- Microsoft::WRL::DeferrableEventArgs::GetDeferral method
- Microsoft::WRL::DeferrableEventArgs::InvokeAllFinished method
ms.assetid: ece89267-7b72-40e1-8185-550c865b070a
ms.openlocfilehash: 23dae7fef88ff7978790e79a0486a83815467f5b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97272933"
---
# <a name="deferrableeventargs-class"></a>Класс DeferrableEventArgs

Класс шаблона, используемый для типов аргументов событий для задержек.

## <a name="syntax"></a>Синтаксис

```cpp
template <typename TEventArgsInterface, typename TEventArgsClass>
class DeferrableEventArgs : public TEventArgsInterface;
```

### <a name="parameters"></a>Параметры

*тевентаргсинтерфаце*<br/>
Тип интерфейса, который объявляет аргументы для отложенного события.

*тевентаргскласс*<br/>
Класс, реализующий *тевентаргсинтерфаце*.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

| name | Описание |
|--|--|
| [Метод deferrableeventargs::/расход](#getdeferral) | Возвращает ссылку на объект [РБП](/uwp/api/windows.foundation.deferral) , представляющий отложенное событие. |
| [Метод deferrableeventargs:: Инвокеаллфинишед](#invokeallfinished) | Вызывается, чтобы указать, что вся обработка для отложенного события завершена. |

## <a name="remarks"></a>Комментарии

Экземпляры этого класса передаются в обработчики событий для отложенных событий. Параметры шаблона представляют интерфейс, определяющий подробные сведения об аргументах событий для конкретного типа отложенного события, а также класс, реализующий этот интерфейс.

Класс отображается как первый аргумент обработчика событий для отложенного события. Можно вызвать метод [откладывания](#getdeferral) , чтобы получить объект [РБП](/uwp/api/windows.foundation.deferral) , из которого можно получить все сведения о отложенном событии. После завершения обработки событий необходимо вызвать завершение в объекте «Задержка». Затем следует вызвать [инвокеаллфинишед](#invokeallfinished) в конце метода обработчика событий, который обеспечивает правильную передачу всех отложенных событий.

## <a name="requirements"></a>Требования

**Заголовок:** Event. h

**Пространство имен:** Microsoft::WRL

## <a name="deferrableeventargsgetdeferral"></a><a name="getdeferral"></a> Метод deferrableeventargs::/расход

Возвращает ссылку на объект [РБП](/uwp/api/windows.foundation.deferral) , представляющий отложенное событие.

```cpp
HRESULT GetDeferral([out, retval] Windows::Foundation::IDeferral** result)
```

### <a name="parameters"></a>Параметры

*result*<br/>
Указатель, который будет ссылаться на объект [РБП](/uwp/api/windows.foundation.deferral) по завершении вызова.

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

## <a name="deferrableeventargsinvokeallfinished"></a><a name="invokeallfinished"></a> Метод deferrableeventargs:: Инвокеаллфинишед

Вызывается, чтобы указать, что вся обработка для отложенного события завершена.

```cpp
void InvokeAllFinished()
```

### <a name="remarks"></a>Комментарии

Этот метод следует вызывать после того, как источник события вызовет [InvokeAll](eventsource-class.md#invokeall). Вызов этого метода предотвращает ввод последующих задержек и вызывает принудительное выполнение обработчика завершения, если задержки отсутствовали.
