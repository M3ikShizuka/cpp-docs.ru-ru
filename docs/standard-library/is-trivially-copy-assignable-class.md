---
description: 'Дополнительные сведения о: is_trivially_copy_assignable классе'
title: Класс is_trivially_copy_assignable
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_trivially_copy_assignable
helpviewer_keywords:
- is_trivially_copy_assignable
ms.assetid: 7410133e-f367-493f-92a7-e34e3ec5e879
ms.openlocfilehash: 010e820db570f594568cb60f4edae83b91a997c4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97271243"
---
# <a name="is_trivially_copy_assignable-class"></a>Класс is_trivially_copy_assignable

Проверяет, есть ли у типа тривиальный оператор присваивания копии.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Ty>
struct is_trivially_copy_assignable;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *T* является классом, имеющим тривиальный оператор присваивания копии, в противном случае — значение false.

Конструктор присваивания для класса *t* является тривиальным, если он неявно предоставляется, *у класса* *t* нет виртуальных функций, а классы всех нестатических элементов данных типа класса имеют тривиальные операторы присваивания, а классы всех нестатических элементов данных массива типов имеют тривиальные операторы присваивания.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
