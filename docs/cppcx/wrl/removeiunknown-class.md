---
description: 'Дополнительные сведения о: RemoveIUnknown Class'
title: Класс RemoveIUnknown
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::Details::RemoveIUnknown
ms.assetid: 998e711a-7d1a-44c6-a016-e6167aa40863
ms.openlocfilehash: 0ef00ee9859a27252550aaeec6fb9b4f9ef2d5b8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97278731"
---
# <a name="removeiunknown-class"></a>Класс RemoveIUnknown

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template <typename T>
struct RemoveIUnknown;

template <typename T>
class RemoveIUnknown : public T;
```

### <a name="parameters"></a>Параметры

*T*<br/>
Класс.

## <a name="remarks"></a>Комментарии

Создает тип, эквивалентный базовому типу `IUnknown`, но имеющий невиртуальные функции-члены `QueryInterface`, `AddRef` и `Release`.

По умолчанию методы COM предоставляют виртуальные `QueryInterface` `AddRef` методы, и `Release` . Однако для `ComPtr` не требуется нагрузка, связанная с виртуальными методами. Интерфейс `RemoveIUnknown` исключает эту нагрузку, предоставляя закрытые невиртуальные методы `QueryInterface`, `AddRef` и `Release`.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`ReturnType`|Синоним для типа, эквивалентный параметру-шаблону *T* , но имеющий невиртуальные `IUnknown` элементы.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`T`

`RemoveIUnknown`

## <a name="requirements"></a>Требования

**Заголовок:** client.h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL::D состояния](microsoft-wrl-details-namespace.md)
