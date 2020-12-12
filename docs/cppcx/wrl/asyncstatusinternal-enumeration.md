---
description: Дополнительные сведения о перечислении Асинкстатусинтернал
title: AsyncStatusInternal - перечисление
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- async/Microsoft::WRL::Details::AsyncStatusInternal
helpviewer_keywords:
- AsyncStatusInternal enumeration
ms.assetid: b783923f-3f1c-4487-9384-be572cbc62d7
ms.openlocfilehash: 3227699a0e7b8933dc5839e65fb3489328d3b1f5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175798"
---
# <a name="asyncstatusinternal-enumeration"></a>AsyncStatusInternal - перечисление

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
enum AsyncStatusInternal;
```

## <a name="remarks"></a>Remarks

Задает сопоставление между внутренними перечислениями состояний асинхронных операций и перечислением `Windows::Foundation::AsyncStatus`.

## <a name="members"></a>Элементы

`_Created`<br/>
Эквивалентно `::Windows::Foundation::AsyncStatus::Created`.

`_Started`<br/>
Эквивалентно `::Windows::Foundation::AsyncStatus::Started`.

`_Completed`<br/>
Эквивалентно `::Windows::Foundation::AsyncStatus::Completed`.

`_Cancelled`<br/>
Эквивалентно `::Windows::Foundation::AsyncStatus::Cancelled`.

`_Error`<br/>
Эквивалентно `::Windows::Foundation::AsyncStatus::Error`.

## <a name="requirements"></a>Требования

**Заголовок:** Async. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL::D состояния](microsoft-wrl-details-namespace.md)
