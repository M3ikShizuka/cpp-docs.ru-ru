---
description: 'Дополнительные сведения о: Platform::D класс делегата'
title: Platform::Delegate - класс
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::Delegate
helpviewer_keywords:
- Platform::Delegate Class
ms.assetid: 82b21271-768f-4193-9ca2-be68ddfd546e
ms.openlocfilehash: 58baedf595d3ee8d9cc4975e787193abf522233c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97176110"
---
# <a name="platformdelegate-class"></a>Platform::Delegate - класс

Представляет объект функции.

## <a name="syntax"></a>Синтаксис

```cpp
public delegate void delegate_name();
```

### <a name="members"></a>Члены

Класс Delegate имеет методы Equals(), GetHashCode() и ToString(), производные от [Platform::Object Class](../cppcx/platform-object-class.md).

### <a name="remarks"></a>Комментарии

Для создания делегатов используйте ключевое слово [delegate](../extensions/delegate-cpp-component-extensions.md) ; не используйте Platform::Delegate явным образом. Дополнительные сведения см. в разделе [Делегаты](../cppcx/delegates-c-cx.md). Пример создания и использования делегата см. в разделе [Creating Windows Runtime Components in C++](/windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp).

### <a name="requirements"></a>Требования

**Минимальный поддерживаемый клиент:** Windows 8

**Минимальный поддерживаемый сервер:** Windows Server 2012

**Пространство имен:** Platform

**Метаданные:** Platform. winmd

## <a name="see-also"></a>См. также раздел

[Пространство имен Platform](../cppcx/platform-namespace-c-cx.md)
