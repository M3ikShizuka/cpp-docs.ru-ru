---
description: 'Дополнительные сведения о: is_final классе'
title: Класс is_final
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_final
helpviewer_keywords:
- is_final
ms.assetid: 9dbad82f-6685-4909-94e8-98e4a93994b9
ms.openlocfilehash: 04660309205689e14200cb5d214ce5dc80efb88f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323745"
---
# <a name="is_final-class"></a>Класс is_final

Проверяет, является ли тип типом класса, отмеченным `final`.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct is_final;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *T* является типом класса, помеченным `final` , в противном случае — значение false. Если *T* является типом класса, он должен быть полным типом.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)\
[Окончательный описатель](../cpp/final-specifier.md)
