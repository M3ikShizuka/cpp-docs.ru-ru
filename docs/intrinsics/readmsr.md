---
description: 'Дополнительные сведения: __readmsr'
title: __readmsr
ms.date: 09/02/2019
f1_keywords:
- __readmsr
helpviewer_keywords:
- Read Model Specific Register
- rdmsr instruction
- __readmsr intrinsic
ms.assetid: 7ab1f8e8-72cb-4ce4-817d-3e728a3c9716
ms.openlocfilehash: 1a8acae272a450cb4470744e434277576cc8b9c4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97271919"
---
# <a name="__readmsr"></a>__readmsr

**Блок, относящийся только к системам Microsoft**

Формирует `rdmsr` инструкцию, которая считывает регистр, зависящий от модели, **`register`** и возвращает его значение.

## <a name="syntax"></a>Синтаксис

```C
__int64 __readmsr(
   int register
);
```

### <a name="parameters"></a>Параметры

*зарегистрировать*\
окне Зависящий от модели регистр для чтения.

## <a name="return-value"></a>Возвращаемое значение

Значение в указанном регистре.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__readmsr`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта функция доступна только в режиме ядра, и подпрограммы доступны только в качестве встроенных.

Дополнительные сведения см. в документации по AMD.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
