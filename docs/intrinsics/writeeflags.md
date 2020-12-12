---
description: 'Дополнительные сведения: __writeeflags'
title: __writeeflags
ms.date: 09/02/2019
f1_keywords:
- __writeeflags
helpviewer_keywords:
- __writeeflags intrinsics
ms.assetid: a62a522c-d7fa-4f10-a620-a3b32bdf3f17
ms.openlocfilehash: 9c439194782f52b474ec6c6365705ebd8756c6b2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331866"
---
# <a name="__writeeflags"></a>__writeeflags

**Блок, относящийся только к системам Microsoft**

Записывает указанное значение в Регистр состояния программы и контроль (ЕФЛАГС).

## <a name="syntax"></a>Синтаксис

```C
void __writeeflags(unsigned Value); /* x86 */
void __writeeflags(unsigned __int64 Value); /* x64 */
```

### <a name="parameters"></a>Параметры

*Значение*\
окне Значение, записываемое в ЕФЛАГС регистр. `Value`Параметр имеет длину 32 бит/с для 32-разрядной платформы и 64 разрядов для 64-разрядной платформы.

## <a name="remarks"></a>Комментарии

Эти подпрограммы доступны только в виде встроенных функций.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__writeeflags`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__readeflags](../intrinsics/readeflags.md)
