---
description: 'Дополнительные сведения: __inword'
title: __inword
ms.date: 09/02/2019
f1_keywords:
- __inword_cpp
- __inword
helpviewer_keywords:
- in instruction
- __inword intrinsic
ms.assetid: 5c617edd-6709-40a1-aad2-40d5e39283c6
ms.openlocfilehash: 8e2d698437cdb27a472872cfe24d7d0ab0a3c768
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167881"
---
# <a name="__inword"></a>__inword

**Блок, относящийся только к системам Microsoft**

Считывает данные из указанного порта с помощью `in` инструкции.

## <a name="syntax"></a>Синтаксис

```C
unsigned short __inword(
   unsigned short Port
);
```

### <a name="parameters"></a>Параметры

*Порту*\
окне Порт, из которого производится чтение.

## <a name="return-value"></a>Возвращаемое значение

Слово прочитанных данных.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__inword`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта процедура доступна только как встроенная функция.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
