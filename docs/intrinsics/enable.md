---
description: 'Дополнительные сведения: _enable'
title: _enable
ms.date: 09/02/2019
f1_keywords:
- _enable
- _enable_cpp
helpviewer_keywords:
- enable intrinsic
- _enable intrinsic
- ssm instruction
ms.assetid: 8bee669b-6bd8-4e25-9383-bb7d57295b4d
ms.openlocfilehash: b9c84a31869dd356d5ee6ebd4eae5bd579cf319e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337044"
---
# <a name="_enable"></a>_enable

**Блок, относящийся только к системам Microsoft**

Позволяет прерывания.

## <a name="syntax"></a>Синтаксис

```C
void _enable(void);
```

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`_enable`|x86, ARM, x64, ARM64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

`_enable` указывает процессору установить флаг прерывания. На платформе x86 систем, эта функция создает инструкцию установить флаг прерывания (`sti`) .

Эта функция доступна только в режиме ядра. При использовании в пользовательском режиме, исключение привилегированной инструкции отбрасывается.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
