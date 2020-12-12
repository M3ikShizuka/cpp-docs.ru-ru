---
description: 'Дополнительные сведения: __writecr3'
title: __writecr3
ms.date: 09/02/2019
f1_keywords:
- _writecr3
helpviewer_keywords:
- _writecr3 intrinsic
ms.assetid: 959d49fa-69d5-47cf-88d2-7688367fe38f
ms.openlocfilehash: fa4555b2fe4a67dcb3669f8ae20ea0e2d76c8984
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97313116"
---
# <a name="__writecr3"></a>__writecr3

**Блок, относящийся только к системам Microsoft**

Записывает значение `Data` в регистр Cr3.

## <a name="syntax"></a>Синтаксис

```C
void writecr3(
   unsigned __int64 Data
);
```

### <a name="parameters"></a>Параметры

*Данные*\
окне Значение, записываемое в CR3 регистр.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__writecr3`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта встроенная функция доступна только в режиме ядра и процедура доступна только как встроенная.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
