---
description: 'Дополнительные сведения: __writedr'
title: __writedr
ms.date: 09/02/2019
f1_keywords:
- __writedr
helpviewer_keywords:
- __writedr intrinsic
ms.assetid: ac55c1ee-df2f-41d4-a429-6f369d2a934d
ms.openlocfilehash: 3a52b8985a28268c430cbb1bfb7b2494e9004820
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331874"
---
# <a name="__writedr"></a>__writedr

**Блок, относящийся только к системам Microsoft**

Записывает указанное значение в указанный регистр отладки.

## <a name="syntax"></a>Синтаксис

```C
void __writedr(unsigned DebugRegister, unsigned DebugValue); /* x86 */
void __writedr(unsigned DebugRegister, unsigned __int64 DebugValue); /* x64 */
```

### <a name="parameters"></a>Параметры

*дебугрегистер*\
окне Число от 0 до 7, идентифицирующее регистр отладки.

*дебугвалуе*\
окне Значение, записываемое в регистр отладки.

## <a name="remarks"></a>Комментарии

Эти встроенные функции доступны только в режиме ядра, а подпрограммы доступны только в виде встроенных функций.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__writedr`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__readdr](../intrinsics/readdr.md)
