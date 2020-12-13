---
description: 'Дополнительные сведения о: Структура BoolStruct'
title: BoolStruct - структура
ms.date: 09/21/2018
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::BoolStruct
- internal/Microsoft::WRL::Details::BoolStruct::Member
helpviewer_keywords:
- Microsoft::WRL::Details::BoolStruct structure
- Microsoft::WRL::Details::BoolStruct::Member data member
ms.assetid: 666eae78-e81d-4fb7-a9e4-1ba617d6d4cd
ms.openlocfilehash: d0c30f554cf2f7ebc3bfaf825b43dc28329f697e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338804"
---
# <a name="boolstruct-structure"></a>BoolStruct - структура

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
struct BoolStruct;
```

## <a name="remarks"></a>Remarks

`BoolStruct`Структура определяет, управляет ли `ComPtr` объект временем существования объекта в интерфейсе. `BoolStruct` используется внутри оператором [BoolType ()](comptr-class.md#operator-microsoft-wrl-details-booltype) .

## <a name="members"></a>Элементы

### <a name="public-data-members"></a>Открытые члены данных

Имя                          | Описание
----------------------------- | ------------------------------------------------------------------------------------------------------------------
[BoolStruct:: Member](#member) | Указывает, что [ComPtr](comptr-class.md) имеет значение, или не управляет временем существования объекта в интерфейсе.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`BoolStruct`

## <a name="requirements"></a>Требования

**Заголовок:** internal. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="boolstructmember"></a><a name="member"></a> BoolStruct:: Member

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
int Member;
```

### <a name="remarks"></a>Комментарии

Указывает, что [ComPtr](comptr-class.md) имеет значение, или не управляет временем существования объекта в интерфейсе.
