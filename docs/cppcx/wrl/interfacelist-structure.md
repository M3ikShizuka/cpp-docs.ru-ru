---
description: 'Дополнительные сведения о: структура Интерфацелист'
title: InterfaceList - структура
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::InterfaceList
helpviewer_keywords:
- InterfaceList structure
ms.assetid: 6ec3228d-eb3e-4b7e-aef1-7dcf17bdf61a
ms.openlocfilehash: 660ae5137b7ff41129ce3866f0d289045f7dee9c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97124583"
---
# <a name="interfacelist-structure"></a>InterfaceList - структура

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template <typename T, typename U>
struct InterfaceList;
```

### <a name="parameters"></a>Параметры

*T*<br/>
Имя интерфейса; Первый интерфейс в рекурсивном списке.

*U*<br/>
Имя интерфейса; остальные интерфейсы в рекурсивном списке.

## <a name="remarks"></a>Комментарии

Используется для создания рекурсивного списка интерфейсов.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`FirstT`|Синоним для параметра шаблона *T*.|
|`RestT`|Синоним для параметра шаблона *U*.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`InterfaceList`

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL::D состояния](microsoft-wrl-details-namespace.md)
