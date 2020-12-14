---
description: 'Дополнительные сведения: __wbinvd'
title: __wbinvd
ms.date: 09/02/2019
f1_keywords:
- __wbinvd
helpviewer_keywords:
- __wbinvd intrinsic
- wbinvd instruction
ms.assetid: 628d0981-39e5-49e1-bd43-706d123af121
ms.openlocfilehash: b40e1b618e49ab317a7b9cdeea647bcd58df7912
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257268"
---
# <a name="__wbinvd"></a>__wbinvd

**Блок, относящийся только к системам Microsoft**

Создает инструкцию Write назад и недействительным кэшем ( `wbinvd` ).

## <a name="syntax"></a>Синтаксис

```C
void __wbinvd(void);
```

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__wbinvd`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта функция доступна только в режиме ядра с уровнем привилегий (CPL), равным 0, и подпрограммы доступны только в качестве встроенных.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
