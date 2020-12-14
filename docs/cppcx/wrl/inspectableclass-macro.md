---
description: 'Дополнительные сведения о: макрос InspectableClass'
title: Макрос InspectableClass
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::InspectableClass
ms.assetid: ff390b26-58cc-424f-87ac-1fe3cc692b59
ms.openlocfilehash: cb19db7f35e7bda351cd84fa4dcf1f6a2b2ea2ba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97229006"
---
# <a name="inspectableclass-macro"></a>Макрос InspectableClass

Задает имя класса среды выполнения и уровень доверия.

## <a name="syntax"></a>Синтаксис

```cpp
InspectableClass(
   runtimeClassName,
   trustLevel)
```

### <a name="parameters"></a>Параметры

*рунтимекласснаме*<br/>
Полное текстовое имя класса среды выполнения.

*trustLevel*<br/>
Одно из перечисляемых значений [TrustLevel](/windows/win32/api/inspectable/ne-inspectable-trustlevel) .

## <a name="remarks"></a>Комментарии

Макрос **InspectableClass** можно использовать только с типами среда выполнения Windows.

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft::WRL

## <a name="see-also"></a>См. также раздел

[Класс RuntimeClass](runtimeclass-class.md)
