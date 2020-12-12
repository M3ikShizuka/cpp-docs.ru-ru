---
description: 'Дополнительные сведения о: allocator_variable_size классе'
title: Класс allocator_variable_size
ms.date: 11/04/2016
f1_keywords:
- allocators/stdext::allocator_variable_size
- allocators/stdext::allocators::allocator_variable_size
- stdext::allocators::allocator_variable_size
helpviewer_keywords:
- stdext::allocator_variable_size
- stdext::allocators [C++], allocator_variable_size
ms.assetid: c3aa4105-ae45-4385-bbbe-9f23060478cb
ms.openlocfilehash: 9a6f9b6316daefbf436d4718a92312ceb8d55aa4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97163539"
---
# <a name="allocator_variable_size-class"></a>Класс allocator_variable_size

Описывает объект, управляющий выделением и освобождением памяти для объектов типа *Type* , использующих кэш типа [cache_freelist](cache-freelist-class.md) с длиной, управляемой [max_variable_size](max-variable-size-class.md).

## <a name="syntax"></a>Синтаксис

```cpp
template <class Type>
class allocator_variable_size;
```

### <a name="parameters"></a>Параметры

*Тип*\
Тип элементов, распределяемых распределителем.

## <a name="remarks"></a>Комментарии

Макрос [ALLOCATOR_DECL](allocators-functions.md#allocator_decl) передает этот класс в качестве параметра *Name* в следующей инструкции: `ALLOCATOR_DECL(CACHE_FREELIST(stdext::allocators::max_variable_size), SYNC_DEFAULT, allocator_variable_size);`

## <a name="requirements"></a>Требования

**Заголовок:**\<allocators>

**Пространство имен:** stdext

## <a name="see-also"></a>См. также раздел

[\<allocators>](allocators-header.md)
