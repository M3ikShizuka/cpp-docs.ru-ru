---
description: 'Дополнительные сведения: __outbytestring'
title: __outbytestring
ms.date: 09/02/2019
f1_keywords:
- __outbytestring
helpviewer_keywords:
- rep outsb instruction
- __outbytestring intrinsic
- outsb instruction
ms.assetid: c9150661-9c18-427f-bae8-710bba6ed78c
ms.openlocfilehash: feadb0b4275e370de88bfc04c8a10f90c41d0844
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97222428"
---
# <a name="__outbytestring"></a>__outbytestring

**Блок, относящийся только к системам Microsoft**

Формирует `rep outsb` инструкцию, которая отправляет первые `Count` байты данных, на которые указывает, `Buffer` на порт, указанный параметром `Port` .

## <a name="syntax"></a>Синтаксис

```C
void __outbytestring(
   unsigned short Port,
   unsigned char* Buffer,
   unsigned long Count
);
```

### <a name="parameters"></a>Параметры

*Порту*\
окне Порт, в который отправляются данные.

*Двойной*\
окне Данные, которые должны быть отправлены по указанному порту.

*Расчета*\
окне Число байтов данных для отправки.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__outbytestring`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта процедура доступна только как встроенная функция.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
