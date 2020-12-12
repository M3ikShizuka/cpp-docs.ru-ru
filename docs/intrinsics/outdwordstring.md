---
description: 'Дополнительные сведения: __outdwordstring'
title: __outdwordstring
ms.date: 09/02/2019
f1_keywords:
- __outdwordstring
helpviewer_keywords:
- outsd instruction
- __outdwordstring intrinsic
- rep outsd instruction
ms.assetid: 55b31a65-aab7-4b5c-b61d-d9e2fb0c497a
ms.openlocfilehash: 3fbba7dd128666b591305326695e656befd9cada
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97180398"
---
# <a name="__outdwordstring"></a>__outdwordstring

**Блок, относящийся только к системам Microsoft**

Формирует `rep outsd` инструкцию, которая отправляет `Count` даублевордс, начиная с `Buffer` порта ввода-вывода, заданного параметром `Port` .

## <a name="syntax"></a>Синтаксис

```C
void __outdwordstring(
   unsigned short Port,
   unsigned long* Buffer,
   unsigned long Count
);
```

### <a name="parameters"></a>Параметры

*Порту*\
окне Порт, в который отправляются данные.

*Двойной*\
окне Указатель на данные, которые должны быть отправлены по указанному порту.

*Расчета*\
окне Число даублевордс для отправки.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__outdwordstring`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта процедура доступна только как встроенная функция.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
