---
description: 'Подробнее: глобальные функции обработки событий'
title: Глобальные функции обработки событий
ms.date: 11/04/2016
f1_keywords:
- atlbase/ATL::AtlWaitWithMessageLoop
helpviewer_keywords:
- event handling, global functions
- global functions, event handling
ms.assetid: fd674470-3def-47c3-be1c-894fa85f13e8
ms.openlocfilehash: 89e5ec38ff8884f5b99592541df6e397e2dd7116
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139858"
---
# <a name="event-handling-global-functions"></a>Глобальные функции обработки событий

Эта функция предоставляет обработчик событий.

> [!IMPORTANT]
> Функция, указанная в следующей таблице, не может использоваться в приложениях, выполняемых в среда выполнения Windows.

|Имя|Описание|
|-|-|
|[AtlWaitWithMessageLoop](#atlwaitwithmessageloop)|Ожидает сигнала объекта, в то же время исправляет сообщения окна по мере необходимости.|

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="atlwaitwithmessageloop"></a><a name="atlwaitwithmessageloop"></a> атлваитвисмессажелуп

Ожидает объекта, о котором требуется сигнализировать; во время ожидания производит требуемую диспетчеризацию сообщений.

> [!IMPORTANT]
> Эта функция не может использоваться в приложениях, выполняемых в среда выполнения Windows.

```
BOOL AtlWaitWithMessageLoop(HANDLE hEvent);
```

### <a name="parameters"></a>Параметры

*хевент*<br/>
окне Маркер объекта, который необходимо дождаться.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если объект был сигнальным.

### <a name="remarks"></a>Комментарии

Это полезно, если требуется дождаться события объекта и получать уведомления о нем, но разрешить сообщения окон в ожидании.

## <a name="see-also"></a>См. также

[Функции](../../atl/reference/atl-functions.md)
