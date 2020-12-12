---
description: 'Дополнительные сведения: __writecr0'
title: __writecr0
ms.date: 09/02/2019
f1_keywords:
- _writecr0
helpviewer_keywords:
- _writecr0 intrinsic
ms.assetid: a143d08d-0333-4e1b-91b4-4acb2ae91b5a
ms.openlocfilehash: 9a4cf4f30b5663b875ca27416b698eb8477938d4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97313103"
---
# <a name="__writecr0"></a>__writecr0

**Блок, относящийся только к системам Microsoft**

Записывает значение `Data` в регистр CR0.

## <a name="syntax"></a>Синтаксис

```C
void writecr0(
   unsigned __int64 Data
);
```

### <a name="parameters"></a>Параметры

*Данные*\
окне Значение, записываемое в CR0 регистр.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__writecr0`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта встроенная функция доступна только в режиме ядра и процедура доступна только как встроенная.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
