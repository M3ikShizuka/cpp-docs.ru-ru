---
description: 'Дополнительные сведения о: структура Енаблеиф'
title: EnableIf - структура
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::EnableIf
helpviewer_keywords:
- EnableIf structure
ms.assetid: 7825b283-e6b2-4f39-a4b9-c03bcd431b8e
ms.openlocfilehash: 098dd5fdc7e37a7754d7124eba3e146575c127be
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97272855"
---
# <a name="enableif-structure"></a>EnableIf - структура

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template <bool b, typename T = void>
struct EnableIf;

template <typename T>
struct EnableIf<true, T>;
```

### <a name="parameters"></a>Параметры

*T*<br/>
Тип.

*b*<br/>
Логическое выражение.

## <a name="remarks"></a>Комментарии

Определяет элемент данных типа, указанного вторым параметром шаблона, если первый параметр шаблона имеет значение **`true`** .

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`type`|Если параметру шаблона *b* присвоено значение **`true`** , то частичная специализация определяет, что член данных имеет `type` тип `T` .|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`EnableIf`

## <a name="requirements"></a>Требования

**Заголовок:** internal. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL::D состояния](microsoft-wrl-details-namespace.md)
