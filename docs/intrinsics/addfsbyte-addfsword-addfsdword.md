---
description: 'Дополнительные сведения: __addfsbyte, __addfsword, __addfsdword'
title: __addfsbyte, __addfsword, __addfsdword
ms.date: 09/02/2019
f1_keywords:
- __addfsbyte_cpp
- __addfsdword
- __addfsword_cpp
- __addfsbyte
- __addfsword
- __addfsdword_cpp
helpviewer_keywords:
- __addfsdword intrinsic
- __addfsword intrinsic
- __addfsbyte intrinsic
ms.assetid: 706c70df-6b52-4401-9268-2977ed8ad715
ms.openlocfilehash: 414327e93ac2d342842f161148453505d49dcce8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97222519"
---
# <a name="__addfsbyte-__addfsword-__addfsdword"></a>__addfsbyte, __addfsword, __addfsdword

**Блок, относящийся только к системам Microsoft**

Добавьте значение в место в памяти, заданное смещением относительно начала `FS` сегмента.

## <a name="syntax"></a>Синтаксис

```C
void __addfsbyte(
   unsigned long Offset,
   unsigned char Data
);
void __addfsword(
   unsigned long Offset,
   unsigned short Data
);
void __addfsdword(
   unsigned long Offset,
   unsigned long Data
);
```

### <a name="parameters"></a>Параметры

*Собой*\
окне Смещение от начала `FS` .

*Данные*\
окне Значение, добавляемое в область памяти.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__addfsbyte`|x86|
|`__addfsword`|x86|
|`__addfsdword`|x86|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эти подпрограммы доступны только в виде встроенных функций.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[__incfsbyte, \_ _incfsword \_ _incfsdword](../intrinsics/incfsbyte-incfsword-incfsdword.md)\
[__readfsbyte, \_ _readfsdword, \_ _readfsqword, \_ _readfsword](../intrinsics/readfsbyte-readfsdword-readfsqword-readfsword.md)\
[__writefsbyte, \_ _writefsdword, \_ _writefsqword, \_ _writefsword](../intrinsics/writefsbyte-writefsdword-writefsqword-writefsword.md)\
[Встроенные объекты компилятора](../intrinsics/compiler-intrinsics.md)
