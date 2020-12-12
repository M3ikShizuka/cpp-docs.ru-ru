---
description: 'Дополнительные сведения: __outbyte'
title: __outbyte
ms.date: 09/02/2019
f1_keywords:
- __outbyte
helpviewer_keywords:
- out instruction
- __outbyte intrinsic
ms.assetid: c4cd1a34-8a02-4e37-993d-3201bc17901a
ms.openlocfilehash: e062d561719cbcdb32ab980efde9eb568defeadb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97222480"
---
# <a name="__outbyte"></a>__outbyte

**Блок, относящийся только к системам Microsoft**

Формирует `out` инструкцию, которая отправляет 1 байт, указанный `Data` портом ввода-вывода, указанным в параметре `Port` .

## <a name="syntax"></a>Синтаксис

```C
void __outbyte(
   unsigned short Port,
   unsigned char Data
);
```

### <a name="parameters"></a>Параметры

*Порту*\
окне Порт, в который отправляются данные.

*Данные*\
окне Байт, отправляемый с указанного порта.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__outbyte`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта процедура доступна только как встроенная функция.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
