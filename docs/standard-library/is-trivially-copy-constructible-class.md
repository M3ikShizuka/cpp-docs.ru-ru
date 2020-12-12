---
description: 'Дополнительные сведения о: is_trivially_copy_constructible классе'
title: Класс is_trivially_copy_constructible
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_trivially_copy_constructible
helpviewer_keywords:
- is_trivially_copy_constructible
ms.assetid: 4274cef5-afdd-4f2d-bc83-7562e7944ddf
ms.openlocfilehash: c247e81f52ad98e546a840bb38938fe15bc9b302
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97118528"
---
# <a name="is_trivially_copy_constructible-class"></a>Класс is_trivially_copy_constructible

Проверяет, есть ли у типа тривиальный конструктор копии.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct is_trivially_copy_constructible;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *T* является классом с тривиальным конструктором копии, в противном случае — значение false.

Конструктор копии для класса *T* является тривиальным, если он неявно объявлен, у класса *t* нет виртуальных функций или виртуальных базовых баз, все прямые базы класса *T* имеют тривиальные конструкторы копий, классы всех нестатических элементов данных класса Type имеют тривиальные конструкторы копий, а классы всех нестатических элементов данных массива типов класса имеют тривиальные конструкторы копий.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
