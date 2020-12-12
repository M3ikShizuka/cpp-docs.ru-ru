---
description: 'Дополнительные сведения: _ReadWriteBarrier'
title: _ReadWriteBarrier
ms.date: 09/02/2019
f1_keywords:
- _ReadWriteBarrier
helpviewer_keywords:
- ReadWriteBarrier intrinsic
- _ReadWriteBarrier intrinsic
ms.assetid: dd9f58b5-8bb6-494e-bb0f-9fe184f3908d
ms.openlocfilehash: ff537d4f3b117b52ba567bf0d130e51d0062965f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97294123"
---
# <a name="_readwritebarrier"></a>_ReadWriteBarrier

**Блок, относящийся только к системам Microsoft**

Ограничивает оптимизации компилятора, которые могут изменить порядок доступа к памяти для точки вызова.

> [!CAUTION]
> Встроенные функции компилятора `_ReadBarrier`, `_WriteBarrier` и `_ReadWriteBarrier`, а также макрос `MemoryBarrier` являются нерекомендуемыми, и использовать их не следует. Для взаимодействия между потоками используйте такие механизмы, как [atomic_thread_fence](../standard-library/atomic-functions.md#atomic_thread_fence) и [std:: Atomic \<T> ](../standard-library/atomic.md), которые определены в [стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md). Для доступа к оборудованию используйте параметр компилятора [/volatile: ISO](../build/reference/volatile-volatile-keyword-interpretation.md) вместе с ключевым словом [volatile](../cpp/volatile-cpp.md) .

## <a name="syntax"></a>Синтаксис

```C
void _ReadWriteBarrier(void);
```

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`_ReadWriteBarrier`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Встроенная функция `_ReadWriteBarrier` ограничивает оптимизации компилятора, которые могут удалять или изменять порядок операций доступа к памяти для точки вызова.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[_ReadBarrier](../intrinsics/readbarrier.md)\
[_WriteBarrier](../intrinsics/writebarrier.md)\
[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[Ключевые слова](../cpp/keywords-cpp.md)
