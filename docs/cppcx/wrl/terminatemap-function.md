---
description: Дополнительные сведения о функции Терминатемап
title: Функция TerminateMap
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::TerminateMap
helpviewer_keywords:
- TerminateMap function
ms.assetid: 1c314a61-da5d-49bb-ac44-c34ee3c23b66
ms.openlocfilehash: 919759d0b4b7f67cf3aff83c3e83678860d0badc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97135067"
---
# <a name="terminatemap-function"></a>Функция TerminateMap

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
inline bool TerminateMap(
   _In_ ModuleBase *module,
   _In_opt_z_ const wchar_t *serverName,
    bool forceTerminate) throw()
```

### <a name="parameters"></a>Параметры

*модуль*<br/>
[Модуль](module-class.md).

*serverName*<br/>
Имя подмножества фабрик класса в модуле, заданном *модулем* параметров.

*форцетерминате*<br/>
**`true`** для завершения фабрик классов, независимо от того, активны они, **`false`** значение, чтобы не завершать фабрики класса, если активна какая-либо фабрика.

## <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если все фабрики класса были завершены; в противном случае — **`false`** .

## <a name="remarks"></a>Комментарии

Завершает работу фабрик классов в указанном модуле.

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL::D состояния](microsoft-wrl-details-namespace.md)
