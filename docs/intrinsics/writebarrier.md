---
description: 'Дополнительные сведения: _WriteBarrier'
title: _WriteBarrier
ms.date: 09/02/2019
f1_keywords:
- _WriteBarrier
helpviewer_keywords:
- WriteBarrier intrinsic
- _WriteBarrier intrinsic
ms.assetid: a5ffdad9-0ca1-4eb7-b2f3-0f092c4bf4b5
ms.openlocfilehash: 7fe78eaa30e7971853ff9d73d7142b8eeddb679f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97313142"
---
# <a name="_writebarrier"></a>_WriteBarrier

**Блок, относящийся только к системам Microsoft**

Ограничивает оптимизации компилятора, которые могут изменить порядок операций доступа к памяти для точки вызова.

> [!CAUTION]
> Встроенные функции компилятора `_ReadBarrier`, `_WriteBarrier` и `_ReadWriteBarrier`, а также макрос `MemoryBarrier` являются нерекомендуемыми, и использовать их не следует. Для взаимодействия между потоками используйте такие механизмы, как [atomic_thread_fence](../standard-library/atomic-functions.md#atomic_thread_fence) и [std:: Atomic \<T> ](../standard-library/atomic.md), которые определены в [стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md). Для доступа к оборудованию используйте параметр компилятора [/volatile: ISO](../build/reference/volatile-volatile-keyword-interpretation.md) вместе с ключевым словом [volatile](../cpp/volatile-cpp.md) .

## <a name="syntax"></a>Синтаксис

```C
void _WriteBarrier(void);
```

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`_WriteBarrier`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Встроенная функция `_WriteBarrier` ограничивает оптимизации компилятора, которые могут удалять или изменять порядок операций доступа к памяти для точки вызова.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[_ReadBarrier](../intrinsics/readbarrier.md)\
[_ReadWriteBarrier](../intrinsics/readwritebarrier.md)\
[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[Ключевые слова](../cpp/keywords-cpp.md)
