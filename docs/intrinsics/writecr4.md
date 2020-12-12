---
description: 'Дополнительные сведения: __writecr4'
title: __writecr4
ms.date: 09/02/2019
f1_keywords:
- _writecr4
helpviewer_keywords:
- _writecr4 intrinsic
ms.assetid: ab7651d7-b86b-4be7-a0a0-7263099c70fc
ms.openlocfilehash: 711a6dff42f3805886865d09b4638479173bc64e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97313090"
---
# <a name="__writecr4"></a>__writecr4

**Блок, относящийся только к системам Microsoft**

Записывает значение `Data` в регистр CR4.

## <a name="syntax"></a>Синтаксис

```C
void writecr4(
   unsigned __int64 Data
);
```

### <a name="parameters"></a>Параметры

*Данные*\
окне Значение, записываемое в CR4 регистр.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__writecr4`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта встроенная функция доступна только в режиме ядра и процедура доступна только как встроенная.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
