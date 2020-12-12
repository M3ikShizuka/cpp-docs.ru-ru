---
description: 'Дополнительные сведения: __nop'
title: __nop
ms.date: 09/02/2019
f1_keywords:
- __nop
helpviewer_keywords:
- nop instruction
- __nop intrinsic
ms.assetid: 7a2a938b-87e0-476d-a348-03ea7635b6b9
ms.openlocfilehash: 55759e8324511b6ddaa2774bdfdc3554c0032c2e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97118931"
---
# <a name="__nop"></a>__nop

**Блок, относящийся только к системам Microsoft**

Создает машинный код, зависящий от платформы, который не выполняет никаких операций.

## <a name="syntax"></a>Синтаксис

```C
void __nop();
```

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__nop`|x86, ARM, x64, ARM64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="remarks"></a>Комментарии

Функция `__nop` эквивалентна инструкции компьютера `NOP` . Дополнительные сведения об архитектуре x86 и x64 см. в документе "Руководство разработчика по архитектуры Intel, том 2: Справочник по набору инструкций" на сайте корпорации [Intel](https://software.intel.com/articles/intel-sdm) .

## <a name="see-also"></a>См. также раздел

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__noop](../intrinsics/noop.md)
