---
description: 'Дополнительные сведения о: is_aggregate классе'
title: Класс is_aggregate
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_aggregate
helpviewer_keywords:
- is_aggregate
ms.openlocfilehash: 6ca27e6edea42b6c0ae3f0c89749a586adac857b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97231372"
---
# <a name="is_aggregate-class"></a>Класс is_aggregate

Проверяет, является ли тип типом класса, отмеченным `aggregate`.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct is_aggregate;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *T* является типом класса, помеченным `aggregate` , в противном случае — значение false. Если *T* является типом класса, он должен быть полным типом.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
