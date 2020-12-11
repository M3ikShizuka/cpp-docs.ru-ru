---
description: 'Дополнительные сведения о: is_trivially_move_constructible классе'
title: Класс is_trivially_move_constructible
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_trivially_move_constructible
helpviewer_keywords:
- is_trivially_move_constructible
ms.assetid: 740bdec7-65e5-47b3-b94f-a2479ceac3ec
ms.openlocfilehash: 30e8be25e74aeed1eafc8fcafbece5c62e4ad999
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97154322"
---
# <a name="is_trivially_move_constructible-class"></a>Класс is_trivially_move_constructible

Проверяет, есть ли у типа тривиальный конструктор перемещения.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
struct is_trivially_move_constructible;
```

### <a name="parameters"></a>Параметры

*Ty*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *Ty* является классом с тривиальным конструктором перемещения, в противном случае — значение false.

Конструктор перемещения для класса *Ty* является тривиальным, если:

он неявно объявлен;

его типы параметров эквивалентны типам неявного объявления;

у класса *Ty* нет виртуальных функций

класс *Ty* не имеет виртуальных базовых классов

класс не содержит изменчивых нестатических элементов данных;

все прямые базовые классы класса *Ty* имеют тривиальные конструкторы перемещения

классы всех нестатических элементов данных типа класса имеют тривиальные конструкторы перемещения;

классы всех нестатических элементов данных массива типов класса имеют тривиальные конструкторы перемещения.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
