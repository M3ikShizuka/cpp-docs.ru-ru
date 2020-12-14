---
description: 'Дополнительные сведения: __addgsbyte, __addgsword, __addgsdword, __addgsqword'
title: __addgsbyte, __addgsword, __addgsdword, __addgsqword
ms.date: 09/02/2019
f1_keywords:
- __addgsdword
- __addgsqword
- __addgsword_cpp
- __addgsword
- __addgsbyte_cpp
- __addgsqword_cpp
- __addgsbyte
- __addgsdword_cpp
helpviewer_keywords:
- __addgsword intrinsic
- __addgsqword intrinsic
- __addgsdword intrinsic
- __addgsbyte intrinsic
ms.assetid: 4fa03e69-d849-49ed-ba37-1d3aa23c2a21
ms.openlocfilehash: e139eb573dc8a4e21bdddff3ba8c756d572c5218
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97222506"
---
# <a name="__addgsbyte-__addgsword-__addgsdword-__addgsqword"></a>__addgsbyte, __addgsword, __addgsdword, __addgsqword

**Блок, относящийся только к системам Microsoft**

Добавьте значение в место в памяти, заданное смещением относительно начала `GS` сегмента.

## <a name="syntax"></a>Синтаксис

```C
void __addgsbyte(
   unsigned long Offset,
   unsigned char Data
);
void __addgsword(
   unsigned long Offset,
   unsigned short Data
);
void __addgsdword(
   unsigned long Offset,
   unsigned long Data
);
void __addgsqword(
   unsigned long Offset,
   unsigned __int64 Data
);
```

### <a name="parameters"></a>Параметры

*Собой*\
окне Смещение от начала `GS` .

*Данные*\
окне Значение, добавляемое в область памяти.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__addgsbyte`|X64|
|`__addgsword`|X64|
|`__addgsdword`|X64|
|`__addgsqword`|X64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эти подпрограммы доступны только в качестве встроенных.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[__incgsbyte, \_ _incgsword, \_ _incgsdword, \_ _incgsqword](../intrinsics/incgsbyte-incgsword-incgsdword-incgsqword.md)\
[__readgsbyte, \_ _readgsdword, \_ _readgsqword, \_ _readgsword](../intrinsics/readgsbyte-readgsdword-readgsqword-readgsword.md)\
[__writegsbyte, \_ _writegsdword, \_ _writegsqword, \_ _writegsword](../intrinsics/writegsbyte-writegsdword-writegsqword-writegsword.md)\
[Встроенные объекты компилятора](../intrinsics/compiler-intrinsics.md)
