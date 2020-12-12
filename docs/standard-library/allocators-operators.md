---
description: 'Дополнительные сведения о: &lt; Операторы распределителя &gt;'
title: Операторы &lt;allocator&gt;
ms.date: 11/04/2016
f1_keywords:
- allocators/std::operator!=
- allocators/std::operator==
ms.assetid: b55d67cb-3c69-46bf-ad40-e845fb096c4e
ms.openlocfilehash: a0289ca7b76aaddb2e6c8ed20a58a61d1be40998
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97163474"
---
# <a name="ltallocatorsgt-operators"></a>Операторы &lt;allocator&gt;

Это функции операторов глобального шаблона, определенные в &lt; распределительах &gt; . Функции оператора члена класса см. в документации по классу.

[operator! =](#op_neq)\
[Оператор = =](#op_eq_eq)

## <a name="operator"></a><a name="op_neq"></a> operator! =

Проверяет на неравенство между объектами распределителя указанного класса.

```cpp
template <class Type, class Sync>
bool operator!=(
    const allocator_base<Type, Sync>& left,
    const allocator_base<Type, Sync>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Один из объектов allocator для проверки на неравенство.

*Правильно*\
Один из объектов allocator для проверки на неравенство.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если объекты распределителя не равны; значение **`false`** , если объекты распределителя равны.

### <a name="remarks"></a>Комментарии

Оператор-шаблон возвращает `!(left == right)`.

## <a name="operator"></a><a name="op_eq_eq"></a> Оператор = =

Проверяет на равенство объекты распределителя указанного класса.

```cpp
template <class Type, class Sync>
bool operator==(
    const allocator_base<Type, Sync>& left,
    const allocator_base<Type, Sync>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Один из объектов allocator для проверки на равенство.

*Правильно*\
Один из объектов allocator для проверки на равенство.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если объекты распределителя равны; значение **`false`** , если объекты распределителя не равны.

### <a name="remarks"></a>Комментарии

Этот оператор шаблона возвращает `left.equals(right)`.

## <a name="see-also"></a>См. также раздел

[\<allocators>](allocators-header.md)
