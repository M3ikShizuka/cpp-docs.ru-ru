---
description: 'Дополнительные сведения: __inwordstring'
title: __inwordstring
ms.date: 09/02/2019
f1_keywords:
- __inwordstring
- __inwordstring_cpp
helpviewer_keywords:
- __inwordstring intrinsic
- rep insw instruction
ms.assetid: 6de37939-017a-4740-9e3d-7de78a30daba
ms.openlocfilehash: d65aaedd3fc0fd51ab276abb391ed3c58047ccda
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167816"
---
# <a name="__inwordstring"></a>__inwordstring

**Блок, относящийся только к системам Microsoft**

Считывает данные из указанного порта с помощью `rep insw` инструкции.

## <a name="syntax"></a>Синтаксис

```C
void __inwordstring(
   unsigned short Port,
   unsigned short* Buffer,
   unsigned long Count
);
```

### <a name="parameters"></a>Параметры

*Порту*\
окне Порт, из которого производится чтение.

*Двойной*\
заполняет Данные, считанные с порта, записываются здесь.

*Расчета*\
окне Число слов данных для чтения.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__inwordstring`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта процедура доступна только как встроенная функция.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
