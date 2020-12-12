---
description: 'Дополнительные сведения: _ReadBarrier'
title: _ReadBarrier
ms.date: 09/02/2019
f1_keywords:
- _ReadBarrier
helpviewer_keywords:
- _ReadBarrier intrinsic
ms.assetid: f9e54a92-61bc-4f55-8195-b8932065a796
ms.openlocfilehash: 94ade7c8f602cf279ac75a5f0a56387c344d0fb6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257500"
---
# <a name="_readbarrier"></a>_ReadBarrier

**Блок, относящийся только к системам Microsoft**

Ограничивает оптимизации компилятора, которые могут изменить порядок операций доступа к памяти для точки вызова.

> [!CAUTION]
> Встроенные функции компилятора `_ReadBarrier`, `_WriteBarrier` и `_ReadWriteBarrier`, а также макрос `MemoryBarrier` являются нерекомендуемыми, и использовать их не следует. Для обмена данными между потоками используйте такие механизмы, как [atomic_thread_fence](../standard-library/atomic-functions.md#atomic_thread_fence) и [std:: \<T> Atomic](../standard-library/atomic.md) , определенные в [стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md). Для доступа к оборудованию используйте параметр компилятора [/volatile: ISO](../build/reference/volatile-volatile-keyword-interpretation.md) вместе с ключевым словом [volatile](../cpp/volatile-cpp.md) .

## <a name="syntax"></a>Синтаксис

```C
void _ReadBarrier(void);
```

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`_ReadBarrier`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Встроенная функция `_ReadBarrier` ограничивает оптимизации компилятора, которые могут удалять или изменять порядок операций доступа к памяти для точки вызова.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[Ключевые слова](../cpp/keywords-cpp.md)
