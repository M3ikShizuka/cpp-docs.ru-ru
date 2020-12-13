---
description: 'Дополнительные сведения: __inbyte'
title: __inbyte
ms.date: 09/02/2019
f1_keywords:
- __inbyte
- __inbyte_cpp
helpviewer_keywords:
- in instruction
- __inbyte intrinsic
ms.assetid: 03b61799-2a08-474d-adc4-2cbf7c81a4d5
ms.openlocfilehash: 77cc1cfb792ffa2f6aef9879820e644372895193
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337021"
---
# <a name="__inbyte"></a>__inbyte

**Блок, относящийся только к системам Microsoft**

Формирует `in` инструкцию, возвращая один байт, считанный из порта, заданного параметром `Port` .

## <a name="syntax"></a>Синтаксис

```C
unsigned char __inbyte(
   unsigned short Port
);
```

### <a name="parameters"></a>Параметры

*Порту*\
окне Порт, из которого производится чтение.

## <a name="return-value"></a>Возвращаемое значение

Байт, считанный из указанного порта.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__inbyte`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="remarks"></a>Комментарии

Эта процедура доступна только как встроенная функция.

## <a name="see-also"></a>См. также раздел

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
