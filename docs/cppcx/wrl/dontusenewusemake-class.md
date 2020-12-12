---
description: 'Дополнительные сведения о: DontUseNewUseMake Class'
title: DontUseNewUseMake - класс
ms.date: 09/21/2018
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::DontUseNewUseMake
- implements/Microsoft::WRL::Details::DontUseNewUseMake::operator new
helpviewer_keywords:
- Microsoft::WRL::Details::DontUseNewUseMake class
- Microsoft::WRL::Details::DontUseNewUseMake::operator new operator
ms.assetid: 8b38d07b-fc14-4cea-afb9-4c1a7dde0093
ms.openlocfilehash: f6b6740e472123e59565e3bad16e4a535a4e17fb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97272907"
---
# <a name="dontusenewusemake-class"></a>DontUseNewUseMake - класс

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
class DontUseNewUseMake;
```

## <a name="remarks"></a>Remarks

Предотвращает использование оператора `new` в `RuntimeClass` . Следовательно, вместо этого следует использовать [функцию make](make-function.md) .

## <a name="members"></a>Элементы

### <a name="public-operators"></a>Открытые операторы

Имя                                             | Описание
------------------------------------------------ | ---------------------------------------------------------------------------
[DontUseNewUseMake:: оператор New](#operator-new) | Перегружает оператор `new` и предотвращает его использование в `RuntimeClass` .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`DontUseNewUseMake`

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="dontusenewusemakeoperator-new"></a><a name="operator-new"></a> DontUseNewUseMake:: оператор New

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
void* operator new(
   size_t,
   _In_ void* placement
);
```

### <a name="parameters"></a>Параметры

*__unnamed0*<br/>
Неименованный параметр, который определяет количество байт памяти для выделения.

*размещаем*<br/>
Выделяемый тип.

### <a name="return-value"></a>Возвращаемое значение

Предоставляет способ передачи дополнительных аргументов при перегрузке оператора `new`.

### <a name="remarks"></a>Комментарии

Перегружает оператор `new` и предотвращает его использование в `RuntimeClass` .
