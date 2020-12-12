---
description: 'Дополнительные сведения о: allocator_fixed_size классе'
title: Класс allocator_fixed_size
ms.date: 11/04/2016
f1_keywords:
- allocators/stdext::allocators::allocator_fixed_size
- allocators/stdext::allocator_fixed_size
- stdext::allocators::allocator_fixed_size
helpviewer_keywords:
- stdext::allocators [C++], allocator_fixed_size
- stdext::allocator_fixed_size
ms.assetid: 138f3ef8-b0b3-49c3-9486-58f2213c172f
ms.openlocfilehash: b4b3452a611734dd2731bdb9c43e4bf7a7ce6744
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97163604"
---
# <a name="allocator_fixed_size-class"></a>Класс allocator_fixed_size

Описывает объект, управляющий выделением и освобождением памяти для объектов типа *Type* , использующих кэш типа [cache_freelist](cache-freelist-class.md) с длиной, управляемой [max_fixed_size](max-fixed-size-class.md).

## <a name="syntax"></a>Синтаксис

```cpp
template <class Type>
class allocator_fixed_size;
```

### <a name="parameters"></a>Параметры

*Тип*\
Тип элементов, распределяемых распределителем.

## <a name="remarks"></a>Комментарии

Макрос [ALLOCATOR_DECL](allocators-functions.md#allocator_decl) передает этот класс в качестве параметра *Name* в следующей инструкции: `ALLOCATOR_DECL(CACHE_FREELIST(stdext::allocators::max_fixed_size<10>), SYNC_DEFAULT, allocator_fixed_size);`

## <a name="requirements"></a>Требования

**Заголовок:**\<allocators>

**Пространство имен:** stdext

## <a name="see-also"></a>См. также раздел

[\<allocators>](allocators-header.md)
