---
description: 'Дополнительные сведения: __readdr'
title: __readdr
ms.date: 09/02/2019
f1_keywords:
- __readdr
helpviewer_keywords:
- __readdr intrinsic
ms.assetid: 061b05da-c85e-4052-b392-106f14bb84f1
ms.openlocfilehash: b3b5952d940db91b278344ab45edb3e8b914c094
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97341013"
---
# <a name="__readdr"></a>__readdr

**Блок, относящийся только к системам Microsoft**

Считывает значение указанного регистра отладки.

## <a name="syntax"></a>Синтаксис

```C
unsigned         __readdr(unsigned int DebugRegister); /* x86 */
unsigned __int64 __readdr(unsigned int DebugRegister); /* x64 */
```

### <a name="parameters"></a>Параметры

*дебугрегистер*\
окне Константа от 0 до 7, определяющая регистр отладки.

## <a name="return-value"></a>Возвращаемое значение

Значение указанного регистра отладки.

## <a name="remarks"></a>Комментарии

Эти встроенные функции доступны только в режиме ядра, а подпрограммы доступны только в виде встроенных функций.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__readdr`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__readeflags](../intrinsics/readeflags.md)
