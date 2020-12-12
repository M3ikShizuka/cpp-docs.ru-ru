---
description: 'Дополнительные сведения: __readcr3'
title: __readcr3
ms.date: 09/02/2019
f1_keywords:
- __readcr3
helpviewer_keywords:
- __readcr3 intrinsic
ms.assetid: e24392c3-cad7-4788-8f31-94bf2e9e0053
ms.openlocfilehash: f430694af6a54dde4839292a10a5267c000ccb86
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257346"
---
# <a name="__readcr3"></a>__readcr3

**Блок, относящийся только к системам Microsoft**

Считывает регистр CR3 и возвращает его значение.

## <a name="syntax"></a>Синтаксис

```C
unsigned __int64 __readcr3(void);
```

## <a name="return-value"></a>Возвращаемое значение

Значение в регистре CR3.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__readcr3`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Встроенная функция доступна только в режиме ядра, и подпрограммы доступны только в качестве встроенных.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
