---
description: Дополнительные сведения о функции swap (WRL)
title: Функция swap (WRL)
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::Swap
ms.assetid: ed134a08-ceb7-4279-aa02-a183c3a426ea
ms.openlocfilehash: e81c9e332c6c6a69f475f53132689dc99fffdfee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97186198"
---
# <a name="swap-function-wrl"></a>Функция swap (WRL)

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
WRL_NOTHROW inline void Swap(
   _Inout_ T& left,
   _Inout_ T& right
);
```

### <a name="parameters"></a>Параметры

*слева*<br/>
Первый аргумент.

*Правильно*<br/>
Второй аргумент.

## <a name="return-value"></a>Возвращаемое значение

## <a name="remarks"></a>Комментарии

Меняет местами значения двух указанных аргументов.

## <a name="requirements"></a>Требования

**Заголовок:** internal. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL::D состояния](microsoft-wrl-details-namespace.md)
