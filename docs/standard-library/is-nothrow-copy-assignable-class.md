---
description: 'Дополнительные сведения о: is_nothrow_copy_assignable классе'
title: Класс is_nothrow_copy_assignable
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_nothrow_copy_assignable
helpviewer_keywords:
- is_nothrow_copy_assignable
ms.assetid: baa8abd6-4f53-489f-abba-8d5d5c53bbbc
ms.openlocfilehash: 43618158e33a393012a9f7a4a3ad14c816e3cd6d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230813"
---
# <a name="is_nothrow_copy_assignable-class"></a>Класс is_nothrow_copy_assignable

Проверяет, имеет ли тип оператор назначения копии, который известен компилятору как не отбрасываемый.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct is_nothrow_copy_assignable;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true для ссылочного типа *T* , где `is_nothrow_assignable<T&, const T&>` имеет значение true; в противном случае — значение false.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)\
[Класс is_nothrow_assignable](../standard-library/is-nothrow-assignable-class.md)
