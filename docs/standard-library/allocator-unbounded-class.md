---
description: 'Дополнительные сведения о: allocator_unbounded классе'
title: Класс allocator_unbounded
ms.date: 11/04/2016
f1_keywords:
- allocators/stdext::allocator_unbounded
- allocators/stdext::allocators::allocator_unbounded
helpviewer_keywords:
- allocator_unbounded class
ms.assetid: facbaea1-b320-4d99-96da-039b2642f352
ms.openlocfilehash: 6d046aa08ddd366c7e7009d1d93c36a365d98170
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97163552"
---
# <a name="allocator_unbounded-class"></a>Класс allocator_unbounded

Описывает объект, управляющий выделением и освобождением памяти для объектов типа *Type* , использующих кэш типа [cache_freelist](cache-freelist-class.md) с длиной, управляемой [max_unbounded](max-unbounded-class.md).

## <a name="syntax"></a>Синтаксис

```cpp
template <class Type>
class allocator_unbounded;
```

### <a name="parameters"></a>Параметры

*Тип*\
Тип элементов, распределяемых распределителем.

## <a name="remarks"></a>Комментарии

Макрос [ALLOCATOR_DECL](allocators-functions.md#allocator_decl) передает этот класс в качестве параметра *Name* в следующей инструкции: `ALLOCATOR_DECL(CACHE_FREELIST(stdext::allocators::max_unbounded), SYNC_DEFAULT, allocator_unbounded);`

## <a name="requirements"></a>Требования

**Заголовок:**\<allocators>

**Пространство имен:** stdext

## <a name="see-also"></a>См. также раздел

[\<allocators>](allocators-header.md)
