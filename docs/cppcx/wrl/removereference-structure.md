---
description: 'Дополнительные сведения о: структура Ремовереференце'
title: RemoveReference - структура
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::RemoveReference
helpviewer_keywords:
- RemoveReference structure
ms.assetid: 43ff91bb-815a-440e-b9fb-7dcbb7c863af
ms.openlocfilehash: 0bcf3685e44b756ce324adc8301d7afb5b4b3f40
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332495"
---
# <a name="removereference-structure"></a>RemoveReference - структура

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template<class T>
struct RemoveReference;

template<class T>
struct RemoveReference<T&>;

template<class T>
struct RemoveReference<T&&>;
```

### <a name="parameters"></a>Параметры

*T*<br/>
Класс.

## <a name="remarks"></a>Комментарии

Отделяет ссылку или признак rvalue-reference от указанного параметра шаблона класса.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`Type`|Синоним для параметра шаблона класса.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`RemoveReference`

## <a name="requirements"></a>Требования

**Заголовок:** internal. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL::D состояния](microsoft-wrl-details-namespace.md)
