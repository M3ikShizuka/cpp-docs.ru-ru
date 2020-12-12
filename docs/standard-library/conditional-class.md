---
description: 'Дополнительные сведения о: условный класс'
title: Класс conditional
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::conditional
helpviewer_keywords:
- conditional class
- conditional
ms.assetid: ece9f539-fb28-4e26-a79f-3264bc984493
ms.openlocfilehash: f8edbd7341598957ecbe8b0822a832973f0e06a4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324975"
---
# <a name="conditional-class"></a>Класс conditional

Выделяет один из 2 типов в зависимости от указанного условия.

## <a name="syntax"></a>Синтаксис

```cpp
template <bool B, class T1, class T2>
struct conditional;

template <bool _Test, class _T1, class _T2>
using conditional_t = typename conditional<_Test, _T1, _T2>::type;
```

### <a name="parameters"></a>Параметры

*&*\
Значение, определяющее выбранный тип.

*T1*\
Результат типа, если B — true.

*T2*\
Результат типа, если B — false.

## <a name="remarks"></a>Комментарии

Typedef элемента шаблона `conditional<B, T1, T2>::type` принимает значение *T1* , если *b* принимает значение **`true`** , и при вычислении *b* принимает значение *T2* **`false`** .

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
