---
description: 'Дополнительные сведения: __readcr2'
title: __readcr2
ms.date: 09/02/2019
f1_keywords:
- __readcr2
helpviewer_keywords:
- __readcr2 intrinsic
ms.assetid: d02c97d8-1953-46e7-a79e-a781e2c5bf27
ms.openlocfilehash: dd862f88716fd2d385622c5100f91fdf47061543
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257359"
---
# <a name="__readcr2"></a>__readcr2

**Блок, относящийся только к системам Microsoft**

Считывает регистр CR2 и возвращает его значение.

## <a name="syntax"></a>Синтаксис

```C
unsigned __int64 __readcr2(void);
```

## <a name="return-value"></a>Возвращаемое значение

Значение в регистре CR2.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__readcr2`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Встроенная функция доступна только в режиме ядра, и подпрограммы доступны только в качестве встроенных.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
