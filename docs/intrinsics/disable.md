---
description: 'Дополнительные сведения: _disable'
title: _disable
ms.date: 09/02/2019
f1_keywords:
- _disable_cpp
- _disable
helpviewer_keywords:
- _disable intrinsic
- rsm instruction
- disable intrinsic
ms.assetid: 52da3df9-815c-4524-9839-6d1742cff5c6
ms.openlocfilehash: c118315a4fea2dad401cc5c6f3621a8ec3b1794c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337102"
---
# <a name="_disable"></a>_disable

**Блок, относящийся только к системам Microsoft**

Отключение прерываний.

## <a name="syntax"></a>Синтаксис

```C
void _disable(void);
```

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`_disable`|x86, ARM, x64, ARM64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

`_disable` Указывает, что процессор должен снять флаг прерывания. На платформе x86 систем, эта функция создает инструкцию снятия флага прерывания (`cli`) .

Эта функция доступна только в режиме ядра. При использовании в пользовательском режиме, исключение привилегированной инструкции во время выполнения отбрасывается.

На платформах ARM и ARM64 эта подпрограммы доступна только как встроенная функция.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
